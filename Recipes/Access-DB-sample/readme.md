# .Net Application deployed using an Access Database which is stored in an Azure Files Container

This example Docker File does the following:
* Specifies a Long Term Servicing Channel base Windows Server 2019 Core image, i.e. mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019
* Executes a PowerShell script to install the JET dependency for working with the Access Database
* Uses APPCMD to set the application's Application Pool to run in 32-bit mode.