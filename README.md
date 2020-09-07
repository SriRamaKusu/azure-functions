Step 1:
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

Step2:
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