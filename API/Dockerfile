ARG VERSION=8.0
FROM mcr.microsoft.com/dotnet/sdk:${VERSION}
WORKDIR /Workspace
RUN \
    dotnet new mvc -n API.Web && \
    dotnet new classlib -n API.Core && \
    dotnet new classlib -n API.Persistence && \
    dotnet new xunit -n API.Tests && \
    dotnet tool install --global dotnet-ef
WORKDIR /Workspace/API.Core
RUN \
    dotnet add package Microsoft.EntityFrameworkCore.Design
WORKDIR /Workspace/API.Persistence
RUN \
    dotnet add package Microsoft.EntityFrameworkCore.Design && \
    dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL
WORKDIR /Workspace/API.Tests
RUN \
    dotnet add package Moq 