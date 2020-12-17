# What is it?

Sharpstrap is an "uber" dotnet new template that includes a full project, ready to deploy immediately.

[![NuGet Badge](https://buildstats.info/nuget/Sharpstrap.WebApi)](https://www.nuget.org/packages/Sharpstrap.WebApi/)
![.NET](https://github.com/sharpstrap/webapik8s/workflows/.NET/badge.svg)

Normally you'd need to:
 - `dotnet new` or create new solution
 - Setup docker build
 - Setup CI/CD
 - Setup Kubernetes builds or otherwise

With sharpstrap, you can simply run

```
dotnet new sharpstrap
```

You'll then be setup immediately with all neccessary application components, including a database, ingress, and best practises asp.net core web application. You'll also have helm charts ready to deploy this straight to Kubernetes!

# How to use
```
dotnet new sharpstrap
```

Set up a new repository in github.com, and push the repo there.

# Roadmap

 - Add github actions for template
 - Check helm chart
 - Deploy to github repositories and point helm there.
 - Add DB context
 - Add DB in Helm
 - Add Project tye version
 - Add "premium" version with message brokers, redis, authentication, etc