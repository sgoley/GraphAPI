# Graph API Custom Connector

This repo is a example build of a custom connector for PowerBI to retrieve Azure AD user information via power query and the graph API.

Depends on Power Query SDK in Visual Studio


Instructions:

 - Add your client id (Application ID in Azure Registered app) and client secret (Generated Key in Azure Registered App) to root directory in respectively named files ('client_id' and 'client_secret'). 
 - For the current scope (Directory.Read.All), you will need to add the following scopes to your registered app:

    ![AAD Scope](docs/img/AADScope.png?raw=true "Title")
 
    ![Graph Scope](docs/img/GraphScope.png?raw=true "Title")
 
 - Build project in Visual Studio
 - Resulting .mez file will need to be moved from "<project>/bin/Release" to "User/Documents/PowerBI Desktop/Custom Connectors". 
 - Turn on PowerBI preview feature (Allow Custom Connectors)
 - Search for Graph Connector in Get Data

This allows you to access the login times + metrics as in the Microsoft [Azure Active Directory Activity Logs](https://appsource.microsoft.com/en-us/product/power-bi/e7cf3f33-014a-4c43-8f48-da3d31496d4e?tab=Overview) Content Pack. 
