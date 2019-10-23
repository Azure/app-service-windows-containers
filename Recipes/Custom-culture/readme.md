# .Net Application which makes use of a Custom Culture (or any MSI/EXE)

This example Docker File does the following:
* Specifies a Long Term Servicing Channel base Windows Server 2019 Core image, i.e. mcr.microsoft.com/dotnet/framework/aspnet:4.8-windowsservercore-ltsc2019
* Executes a PowerShell script to install the Custom Culture installation package into the Global Assembly Cache (GAC)
