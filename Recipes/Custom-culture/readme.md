# .Net Application which makes use of a Custom Culture (or any MSI/EXE)

This example Docker File does the following:
* Specifies a Long Term Servicing Channel base Windows Server 2016 Core image, i.e. microsoft/aspnet:4.7.2-windowsservercore-ltsc2016
* Executes a PowerShell script to install the Custom Culture installation package into the Global Assembly Cache (GAC)
