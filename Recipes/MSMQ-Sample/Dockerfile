#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat 

FROM mcr.microsoft.com/dotnet/framework/aspnet:3.5-windowsservercore-ltsc2019
ARG source

RUN PowerShell.exe Enable-WindowsOptionalFeature -online -FeatureName MSMQ
RUN PowerShell.exe Enable-WindowsOptionalFeature -online -FeatureName MSMQ-Services
RUN PowerShell.exe Enable-WindowsOptionalFeature -online -FeatureName MSMQ-Server

WORKDIR /inetpub/wwwroot
COPY ${source:-obj/Docker/publish} .