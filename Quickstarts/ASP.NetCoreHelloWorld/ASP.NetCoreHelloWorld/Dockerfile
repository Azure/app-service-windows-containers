#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat

FROM microsoft/dotnet:2.1-aspnetcore-runtime-nanoserver-sac2016 AS base
WORKDIR /app
EXPOSE 62070
EXPOSE 44397

FROM microsoft/dotnet:2.1-sdk-nanoserver-sac2016 AS build
WORKDIR /src
COPY ["ASP.NetCoreHelloWorld/ASP.NetCoreHelloWorld.csproj", "ASP.NetCoreHelloWorld/"]
RUN dotnet restore "ASP.NetCoreHelloWorld/ASP.NetCoreHelloWorld.csproj"
COPY . .
WORKDIR "/src/ASP.NetCoreHelloWorld"
RUN dotnet build "ASP.NetCoreHelloWorld.csproj" -c Release -o /app

FROM build AS publish
RUN dotnet publish "ASP.NetCoreHelloWorld.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "ASP.NetCoreHelloWorld.dll"]