# What is it?

Sharpstrap is an "uber" dotnet new template that includes a full project, ready to deploy immediately.

Normally you'd need to:
 - `dotnet new` or create new solution
 - Setup docker build
 - Setup CI/CD
 - Setup Kubernetes builds or otherwise

With sharpstrap, you can simply run

```
dotnet new sharpstrap
helm deploy
```

You'll then be setup immediately with all neccessary application components, including a database, ingress, and best practises asp.net core web application.