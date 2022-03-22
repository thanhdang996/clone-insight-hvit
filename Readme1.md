# Git branch usages
- Checkout branch dev_product 
# How to build a development environment

## Development Environments
1. Install Nodejs : https://nodejs.org/en/
2. Install Visual Studio 2019 : https://my.visualstudio.com/Downloads?q=Visual%20Studio%202019
3. Install Visual Studio Code : https://code.visualstudio.com/download
4. Install MySQL Workbench : https://dev.mysql.com/downloads/workbench/

# Get source code LTS LGT Procuratio Project
1.  Click link to get source : https://dev.azure.com/LGTVN/_git/LTS%20LGT%20Procuratio%20Project

# Run back-end
1.  Clone dev_product branch
2.  Close Visual Studio 2019
3.  Open file ```Procuratio.sln``` in Visual Studio 2019
4.  Change connection string in appsetting.Development.json at Identity.Api and Product.Api
5.  Change CorsOrigins, AppDomain, IssuerUri, Authority to https://localhost:3000
6.  Change Server name to localhost
7.  Change Uid and password (Pwd) as same as user, password you use to login in MySql Workbench
8. Select Multiple startup project and change Action of Identity.Api and Product.Api to Start then click Apply/Ok

# Run front-end
1. Open terminal and install yarn: ```yarn install```
2. Open manage computer certificates in computer and port file localhost with private key that you want and name will be localhost.pfx
3. Replace file localhost.pem in Visual Studio Code
4. ```yarn run serve``` to run front-end
