# AzureDevDocs
# Azure Durable Functions
Durable Functions are very similar to regular Azure Functions, except they are slightly more complex - utilising the ability to call other functions within the same function to create a chain. This usually involves utilising the Async/Await syntax to force code to run in a certain order and avoid causing any issues.  
They are created the same way, using Azure Functions, but the code syntax is slightly different compared to a regular function.  
There are different patterns that are used when it comes to the use of Durable Functions. It may be that you setup a function to act as a basic monitor (for example, checking the length of runtime to ensure that the function is not taking far too long to process), or you await human interaction before executing code. There are many things that can be done with Durable Functions!  
# Azure Durable Functions - Examples  
These examples are taken from Microsoft's official documentation: [here.](https://docs.microsoft.com/en-us/azure/azure-functions/durable/durable-functions-overview?tabs=javascript)  
Chaining Functions together:  
```C#
[FunctionName("Chaining")]
public static async Task<object> Run(
    [OrchestrationTrigger] IDurableOrchestrationContext context)
{
    try
    {
        var x = await context.CallActivityAsync<object>("F1", null);
        var y = await context.CallActivityAsync<object>("F2", x);
        var z = await context.CallActivityAsync<object>("F3", y);
        return  await context.CallActivityAsync<object>("F4", z);
    }
    catch (Exception)
    {
        // Error handling or compensation goes here.
    }
}
```  
In this code, the variables x, y & z are calling other functions, F1, F2, F3, & F4, in an Asynchronous fashion. This means that the line with var y will NOT execute until AFTER var x's line has been FULLY COMPLETED.  This means you could execute the code 1 million times and it will always run the code in the same order.  
Fan in/Fan out:  
```C#
[FunctionName("FanOutFanIn")]
public static async Task Run(
    [OrchestrationTrigger] IDurableOrchestrationContext context)
{
    var parallelTasks = new List<Task<int>>();

    // Get a list of N work items to process in parallel.
    object[] workBatch = await context.CallActivityAsync<object[]>("F1", null);
    for (int i = 0; i < workBatch.Length; i++)
    {
        Task<int> task = context.CallActivityAsync<int>("F2", workBatch[i]);
        parallelTasks.Add(task);
    }

    await Task.WhenAll(parallelTasks);

    // Aggregate all N outputs and send the result to F3.
    int sum = parallelTasks.Sum(t => t.Result);
    await context.CallActivityAsync("F3", sum);
}
```  
This durable function again calls functions, but they are done in a parallel fashion using a For loop. Afterwards, it awaits until ALL tasks have been completed, and then compiles the results in the end. This method allows for one function to call many, and then check the summary of all of the results.  

The key takeaway from both of these functions is one line of code, which allows you to call a separate function (within the same FunctionApp):
```C#
var returnLocation = await context.CallActivityAsync<variable>("FunctionName", returnLocation)
```
This line allows you to call a function with the FunctionName variable, with the result going into returnLocation. This can be called as many times as you want, so feel free to call your alternative function as many times as you want!  

# Summary  
In summary, Durable Functions allow us to make far more functions which are complex in nature, but also allow use of functions calling each other - which is great for creating full serverless architectures.  
And best of all, Durable Functions fall under the same billing system as they are still Azure Functions, meaning you can still get up to 1 million calls per month! Note that calling a function within a function is classed as a request, so don't make a while loop that calls the same function 1 million times, else you'll run out extremely fast!    