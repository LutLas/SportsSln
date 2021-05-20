#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/aspnet:3.1 AS base
FROM mcr.microsoft.com/dotnet/sdk:3.1 AS build
COPY /bin/Release/netcoreapp3.1/publish/ SportsStore/
ENV ASPNETCORE_ENVIRONMENT Production
EXPOSE 5000
WORKDIR /SportsStore
ENTRYPOINT ["dotnet", "SportsStore.dll","--urls=http://0.0.0.0:5000"]