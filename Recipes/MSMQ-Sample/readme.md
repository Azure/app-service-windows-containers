# .Net 3.5 Applications which connects to a MSMQ Queue

This example Docker File does the following:
* Specifies a Long Term Servicing Channel base Windows Server 2019 Core image, i.e. microsoft/aspnet:3.5-windowsservercore-ltsc2019
* Installs the required Windows features to enable MSMQ workloads - MSMQ, MSMQ-Services and MSMQ-Server
