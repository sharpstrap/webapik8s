FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine3.12 AS build
WORKDIR /app

# Copy project file and restore
COPY "./Api/SharpStrapTemplate.Api.csproj" "./Api/"
RUN dotnet restore ./Api/SharpStrapTemplate.Api.csproj

# Copy the actual source code
COPY "./Api" "./Api"

# Build and publish the app
RUN dotnet publish "./Api/SharpStrapTemplate.Api.csproj" -c Release -o /app/publish

#FINAL image
FROM mcr.microsoft.com/dotnet/aspnet:5.0-alpine3.12
WORKDIR /app
COPY --from=build /app/publish .
ENTRYPOINT ["dotnet", "SharpStrapTemplate.Api.dll"]