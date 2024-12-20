# Web Application project

Group work with two persons.

Delivery date: 17.1.2025

**IMPORTANT:**

- Regular commits are relevant to the grade for this and all other exercises. 
- Commits also in every practical work hour.
- It is a NO-GO to put the entire code of the exercise into a single commit.
- **Start modelling with Plant UML.**

## What should be included:
- Plant UML. Until 6.12.2024
- Entities, at least 8.
- Some *value types* and a little bit of inheritance ;-).
- Generate test data with Bogus.
- Work with services.
- Use GUIDs, DTOs, ...
- Use validation.
- Implement a meaningful exception handling.
- Testing (with fixtures, mocking, ...)

## Create a new Solution (folder structure like a maven project)

You can also choose your own structure, however it should follow (for example) the Clean-Architecture guidelines.

Rename XxxApp!

```cmd
md XxxApp
cd XxxApp
md src
cd src
md XxxApp.Application
md XxxApp.WebApp
cd XxxApp.Application
dotnet new classlib
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
cd ..\XxxApp.WebApp
dotnet new webapp
dotnet add reference ..\XxxApp.Application
cd ..
cd ..
md test
cd test
md XxxApp.Test
cd XxxApp.Test
dotnet new xunit
dotnet add reference ..\..\src\XxxApp.Application
cd ../..
dotnet new sln
dotnet sln add src\XxxApp.WebApp
dotnet sln add src\XxxApp.Application
dotnet sln add test\XxxApp.Test
start XxxApp.sln
```
