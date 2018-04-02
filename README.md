---
services: cosmos-db
platforms: dotnet
author: ryancrawcour
---

# Web application development with ASP.NET MVC using Azure Cosmos DB
This sample shows you how to use the Microsoft Azure Cosmos DB service to store and access data from an ASP.NET MVC application hosted on Azure Websites. 

For a complete end-to-end walk-through of creating this application, please refer to the [full tutorial on the Azure Cosmos DB documentation page](https://docs.microsoft.com/azure/cosmos-db/sql-api-dotnet-application).

## Running this sample

1. Before you can run this sample, you must have the following perquisites:
	- An active Azure Cosmos DB account - If you don't have an account, refer to the [Create a database account](https://docs.microsoft.com/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account) article.
	- Visual Studio 2013 (or higher).
	- [Azure SDK for Visual Studio 2013](https://azure.microsoft.com/en-us/downloads/)

2.Clone this repository using Git for Windows (http://www.git-scm.com/), or download the zip file.

3.From Visual Studio, open the **todo.sln** file from the root directory.

4.In Visual Studio Build menu, select **Build Solution** (or Press F6). 

5.Retrieve the URI and PRIMARY KEY (or SECONDARY KEY) values from the Keys blade of your Azure Cosmos DB account in the Azure portal. For more information on obtaining endpoint & keys for your Azure Cosmos DB account refer to [View, copy, and regenerate access keys and passwords](https://docs.microsoft.com/azure/cosmos-db/manage-account#keys).

If you don't have an account, see [Create a database account](https://docs.microsoft.com/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account) to set one up.

6.In the **Web.config** file, located in the project root, find **endpoint** and **authKey** and replace the placeholder values with the values obtained for your account.

	<add key="endpoint" value="~enter URI for your Azure Cosmos DB Account, from the Azure portal~" /> 
	<add key="authKey" value="~enter either Primary or Secondary key for your Azure Cosmos DB Account, from the Azure portal~" /> 

7.You can now run and debug the application locally by pressing **F5** in Visual Studio.

## Deploy this sample to Azure

1. In Visual Studio Solution Explorer, right-click on the project name and select **Publish...**

2. Using the Publish Website dialog, select **Microsoft Azure Web Apps**

3. In the next dialog, either select an existing web app, or follow the prompts to create a new web application. Note: If you choose to create a web application, the Web App Name chosen must be globally unique. 

4. Once you have selected the web app, click **Publish**

5. After a short time, Visual Studio will complete the deployment and open a browser with your deployed application. 

For additional ways to deploy this web application to Azure, please refer to the [Deploy a web app in Azure App Service](https://azure.microsoft.com/en-us/documentation/articles/web-sites-deploy/) article which includes information on using Azure Resource Manager (ARM) Templates, Git, MsBuild, PowerShell, Web Deploy, and many more. 

## About the code
The code included in this sample is intended to get you going with a simple ASP.NET MVC application that connects to Azure Cosmos DB. It is not intended to be a set of best practices on how to build scalable enterprise grade web applications. This is beyond the scope of this quick start sample. 

## More information
ocument
- [Azure Cosmos DB Documentation](https://docs.microsoft.com/en-us/azure/cosmos-db/index)
- [Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet)
- [Azure Cosmos DB .NET SDK Reference Documentation](https://docs.microsoft.com/dotnet/api/overview/azure/cosmosdb?view=azure-dotnet)
