# .Net Application deployed using an Access Database which is stored in an Azure Files Container

This example Docker File does the following:
* Specifies a Long Term Servicing Channel base Windows Server 2016 Core image, i.e. microsoft/aspnet:4.7.2-windowsservercore-ltsc2016
* Executes a PowerShell script to install the JET dependency for working with the Access Database
* Uses APPCMD to set the application's Application Pool to run in 32-bit mode.