Install azure functions core tools to use the command line utility 'func'
https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=macos%2Ccsharp%2Cbash


Step 1: Initialize the folder as azure functions folder
=======
SriRamas-MacBook-Air:azure functions sriramakusu$ func init
Select a number for worker runtime:
1. dotnet
2. node
3. python
4. powershell
Choose option: 3
python
Found Python version 3.6.8 (python3).
Writing .gitignore
Writing host.json
Writing local.settings.json
Writing /Users/sriramakusu/WFH/azure functions/.vscode/extensions.json

Step2: create the trigger function from the wide range of 12 triggers supported by azure as of writing today. I am selecting the HTTP Trigger.
======
SriRamas-MacBook-Air:azure functions sriramakusu$ func new
Select a number for template:
1. Azure Blob Storage trigger
2. Azure Cosmos DB trigger
3. Durable Functions activity (preview)
4. Durable Functions HTTP starter (preview)
5. Durable Functions orchestrator (preview)
6. Azure Event Grid trigger
7. Azure Event Hub trigger
8. HTTP trigger
9. Azure Queue Storage trigger
10. Azure Service Bus Queue trigger
11. Azure Service Bus Topic trigger
12. Timer trigger
Choose option: 8
HTTP trigger
Function name: [HttpTrigger] 
Writing /Users/sriramakusu/WFH/azure functions/HttpTrigger/__init__.py
Writing /Users/sriramakusu/WFH/azure functions/HttpTrigger/function.json
The function "HttpTrigger" was created successfully from the "HTTP trigger" template.

Once done, we will get the trigger function gets created with the template code.

Step3: Testing:
===============
You can test the function locally before actually deploying to the function app service in azure.
SriRamas-MacBook-Air:azure functions sriramakusu$ func host start
Found Python version 3.6.8 (python3).

                  %%%%%%
                 %%%%%%
            @   %%%%%%    @
          @@   %%%%%%      @@
       @@@    %%%%%%%%%%%    @@@
     @@      %%%%%%%%%%        @@
       @@         %%%%       @@
         @@      %%%       @@
           @@    %%      @@
                %%
                %

Azure Functions Core Tools (2.7.2508 Commit hash: 4da36643c32783a832094318afcd679fa9d76455)
Function Runtime Version: 2.0.13351.0
AZURE_FUNCTIONS_ENVIRONMENT: Development
[07/09/2020 05:08:56] FUNCTIONS_WORKER_RUNTIME set to python. Skipping WorkerConfig for language:java
[07/09/2020 05:08:56] FUNCTIONS_WORKER_RUNTIME set to python. Skipping WorkerConfig for language:powershell
[07/09/2020 05:08:56] FUNCTIONS_WORKER_RUNTIME set to python. Skipping WorkerConfig for language:node
[07/09/2020 05:08:56] Building host: startup suppressed: 'False', configuration suppressed: 'False', startup operation id: 'fed106ad-ffc9-41a2-9609-019367d3c836'
[07/09/2020 05:08:56] Reading host configuration file '/Users/sriramakusu/WFH/azure functions/host.json'
[07/09/2020 05:08:56] Host configuration file read:
[07/09/2020 05:08:56] {
[07/09/2020 05:08:56]   "version": "2.0",
[07/09/2020 05:08:56]   "logging": {
[07/09/2020 05:08:56]     "applicationInsights": {
[07/09/2020 05:08:56]       "samplingSettings": {
[07/09/2020 05:08:56]         "isEnabled": true,
[07/09/2020 05:08:56]         "excludedTypes": "Request"
[07/09/2020 05:08:56]       }
[07/09/2020 05:08:56]     }
[07/09/2020 05:08:56]   },
[07/09/2020 05:08:56]   "extensionBundle": {
[07/09/2020 05:08:56]     "id": "Microsoft.Azure.Functions.ExtensionBundle",
[07/09/2020 05:08:56]     "version": "[1.*, 2.0.0)"
[07/09/2020 05:08:56]   }
[07/09/2020 05:08:56] }
[07/09/2020 05:08:56] Reading functions metadata
[07/09/2020 05:08:56] 1 functions found
[07/09/2020 05:08:56] Looking for extension bundle Microsoft.Azure.Functions.ExtensionBundle at /var/folders/jv/b3x__b9n7894m5pmkqst84pc0000gn/T/Functions/ExtensionBundles/Microsoft.Azure.Functions.ExtensionBundle
[07/09/2020 05:08:56] Found a matching extension bundle at /var/folders/jv/b3x__b9n7894m5pmkqst84pc0000gn/T/Functions/ExtensionBundles/Microsoft.Azure.Functions.ExtensionBundle/1.3.2
[07/09/2020 05:08:56] Fetching information on versions of extension bundle Microsoft.Azure.Functions.ExtensionBundle available on https://functionscdn.azureedge.net/public/ExtensionBundles/Microsoft.Azure.Functions.ExtensionBundle/index.json
[07/09/2020 05:08:56] Skipping bundle download since it already exists at path /var/folders/jv/b3x__b9n7894m5pmkqst84pc0000gn/T/Functions/ExtensionBundles/Microsoft.Azure.Functions.ExtensionBundle/1.3.2
[07/09/2020 05:08:56] Loading Extention bundle from /var/folders/jv/b3x__b9n7894m5pmkqst84pc0000gn/T/Functions/ExtensionBundles/Microsoft.Azure.Functions.ExtensionBundle/1.3.2
[07/09/2020 05:08:56] FUNCTIONS_WORKER_RUNTIME set to python. Skipping WorkerConfig for language:java
[07/09/2020 05:08:56] FUNCTIONS_WORKER_RUNTIME set to python. Skipping WorkerConfig for language:powershell
[07/09/2020 05:08:56] FUNCTIONS_WORKER_RUNTIME set to python. Skipping WorkerConfig for language:node
[07/09/2020 05:08:57] Initializing Warmup Extension.
[07/09/2020 05:08:57] Initializing Host. OperationId: 'fed106ad-ffc9-41a2-9609-019367d3c836'.
[07/09/2020 05:08:57] Host initialization: ConsecutiveErrors=0, StartupCount=1, OperationId=fed106ad-ffc9-41a2-9609-019367d3c836
[07/09/2020 05:08:57] LoggerFilterOptions
[07/09/2020 05:08:57] {
[07/09/2020 05:08:57]   "MinLevel": "None",
[07/09/2020 05:08:57]   "Rules": [
[07/09/2020 05:08:57]     {
[07/09/2020 05:08:57]       "ProviderName": null,
[07/09/2020 05:08:57]       "CategoryName": null,
[07/09/2020 05:08:57]       "LogLevel": null,
[07/09/2020 05:08:57]       "Filter": "<AddFilter>b__0"
[07/09/2020 05:08:57]     },
[07/09/2020 05:08:57]     {
[07/09/2020 05:08:57]       "ProviderName": "Microsoft.Azure.WebJobs.Script.WebHost.Diagnostics.SystemLoggerProvider",
[07/09/2020 05:08:57]       "CategoryName": null,
[07/09/2020 05:08:57]       "LogLevel": "None",
[07/09/2020 05:08:57]       "Filter": null
[07/09/2020 05:08:57]     },
[07/09/2020 05:08:57]     {
[07/09/2020 05:08:57]       "ProviderName": "Microsoft.Azure.WebJobs.Script.WebHost.Diagnostics.SystemLoggerProvider",
[07/09/2020 05:08:57]       "CategoryName": null,
[07/09/2020 05:08:57]       "LogLevel": null,
[07/09/2020 05:08:57]       "Filter": "<AddFilter>b__0"
[07/09/2020 05:08:57]     }
[07/09/2020 05:08:57]   ]
[07/09/2020 05:08:57] }
[07/09/2020 05:08:57] FunctionResultAggregatorOptions
[07/09/2020 05:08:57] {
[07/09/2020 05:08:57]   "BatchSize": 1000,
[07/09/2020 05:08:57]   "FlushTimeout": "00:00:30",
[07/09/2020 05:08:57]   "IsEnabled": true
[07/09/2020 05:08:57] }
[07/09/2020 05:08:57] SingletonOptions
[07/09/2020 05:08:57] {
[07/09/2020 05:08:57]   "LockPeriod": "00:00:15",
[07/09/2020 05:08:57]   "ListenerLockPeriod": "00:00:15",
[07/09/2020 05:08:57]   "LockAcquisitionTimeout": "10675199.02:48:05.4775807",
[07/09/2020 05:08:57]   "LockAcquisitionPollingInterval": "00:00:05",
[07/09/2020 05:08:57]   "ListenerLockRecoveryPollingInterval": "00:01:00"
[07/09/2020 05:08:57] }
[07/09/2020 05:08:57] HttpOptions
[07/09/2020 05:08:57] {
[07/09/2020 05:08:57]   "DynamicThrottlesEnabled": false,
[07/09/2020 05:08:57]   "MaxConcurrentRequests": -1,
[07/09/2020 05:08:57]   "MaxOutstandingRequests": -1,
[07/09/2020 05:08:57]   "RoutePrefix": "api"
[07/09/2020 05:08:57] }
[07/09/2020 05:08:57] Starting JobHost
[07/09/2020 05:08:57] Starting Host (HostId=sriramasmacbookair-1998387937, InstanceId=369b65a5-ee39-49cd-b04f-a7e76738fcb0, Version=2.0.13351.0, ProcessId=4550, AppDomainId=1, InDebugMode=False, InDiagnosticMode=False, FunctionsExtensionVersion=(null))
[07/09/2020 05:08:57] Loading functions metadata
[07/09/2020 05:08:57] 1 functions loaded
[07/09/2020 05:08:57] Starting worker process:python3  "/usr/local/Cellar/azure-functions-core-tools/2.7.2508/workers/python/3.6/OSX/X64/worker.py" --host 127.0.0.1 --port 54077 --workerId 42ad8e2c-772d-4a7e-9f54-7bc1888619f8 --requestId b1b61cb7-0516-463c-b5d7-ae68bcccd1a2 --grpcMaxMessageLength 134217728
[07/09/2020 05:08:57] python3 process with Id=4557 started
[07/09/2020 05:08:57] Generating 1 job function(s)
[07/09/2020 05:08:57] Found the following functions:
[07/09/2020 05:08:57] Host.Functions.HttpTrigger
[07/09/2020 05:08:57] 
[07/09/2020 05:08:57] Initializing function HTTP routes
[07/09/2020 05:08:57] Mapped function route 'api/HttpTrigger' [get,post] to 'HttpTrigger'
[07/09/2020 05:08:57] 
[07/09/2020 05:08:57] Host initialized (497ms)
[07/09/2020 05:08:57] Host started (536ms)
[07/09/2020 05:08:57] Job host started
Hosting environment: Development
Content root path: /Users/sriramakusu/WFH/azure functions
Now listening on: http://0.0.0.0:7071
Application started. Press Ctrl+C to shut down.

Http Functions:

        HttpTrigger: [GET,POST] http://localhost:7071/api/HttpTrigger

[07/09/2020 05:08:58]  INFO: Starting Azure Functions Python Worker.
[07/09/2020 05:08:58]  INFO: Worker ID: 42ad8e2c-772d-4a7e-9f54-7bc1888619f8, Request ID: b1b61cb7-0516-463c-b5d7-ae68bcccd1a2, Host Address: 127.0.0.1:54077
[07/09/2020 05:08:58]  INFO: Successfully opened gRPC channel to 127.0.0.1:54077
[07/09/2020 05:08:58]  INFO: Received WorkerInitRequest, request ID b1b61cb7-0516-463c-b5d7-ae68bcccd1a2
[07/09/2020 05:08:58]  INFO: Received FunctionLoadRequest, request ID: b1b61cb7-0516-463c-b5d7-ae68bcccd1a2, function ID: dbfd5ce5-52b6-4552-b574-3d99c5024034
[07/09/2020 05:08:58]  INFO: Successfully processed FunctionLoadRequest, request ID: b1b61cb7-0516-463c-b5d7-ae68bcccd1a2, function ID: dbfd5ce5-52b6-4552-b574-3d99c5024034
[07/09/2020 05:09:02] Host lock lease acquired by instance ID '000000000000000000000000407EAB05'.


You can test the working of function using the postman locally
http://localhost:7071/api/HttpTrigger

Step 4: Deployment
=======

you can deploy the function(s) to the azure function app by running simply the following command
func azure functionapp publish with the agruments of function app name and remote build




