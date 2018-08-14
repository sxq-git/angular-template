# angular-template
angular template dotnet core

## How to deploy on Azure server
- Login Azure `https://portal.azure.com/`
- Create Web App enter information (App name, Subscribtion, Resource Group, OS: Windows) and create
- Go to App name and select Application Settings
- On Application settings add config
  * ASPNETCORE_ENVIRONMENT: production
  * CONNECTION_STRING
  * WEBSITE_NODE_DEFAULT_VERSION
    * NodeJs and npm version that azure web app supports following url `https://{app_name}.scm.azurewebsites.net/api/diagnostics/runtime`
- Select Deployment Credentials tab to create deployment user
- Select Deployment Options tab, choose Local Git Repository
- Add git remote url 
  * `git remote add azure https://{deployment_user}@{app_name}.scm.azurewebsites.net/{app_name}`
- Push code to azure server 
  * `git push azure {branch}:master`