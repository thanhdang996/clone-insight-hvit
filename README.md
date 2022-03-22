# First, you need download all list software below :
- Visual Studio 2019
- Visual Studio Code
- Nodejs
- Git
- Postman
- MySQL Workbench

# Get source code LTS LGT Procuratio Project
 1. You need to login with account lotus (...@lotus-ts.com)
 
 2. Click link to get source : https://dev.azure.com/LGTVN/_git/LTS%20LGT%20Procuratio%20Project
![image](https://user-images.githubusercontent.com/82664727/159402637-75a3ff6d-d528-4604-8844-0a970db5e4bc.png)
Copy link :  
![image](https://user-images.githubusercontent.com/82664727/159403054-c534188d-8372-4127-a712-95f22e21d0d9.png)

3. Open Visual Studio 2019, click clone a repository, paste link you just copy to repository location (change path if you want)
![image](https://user-images.githubusercontent.com/82664727/159404483-8abbddd5-b050-44ce-b3e2-85952568e515.png)

# Run back-end
1. Clone code done, click branch master, tab remote, choosen branch dev/dev_product
![image](https://user-images.githubusercontent.com/82664727/159405729-9b8ca44e-80a2-4401-be7c-548adf116f4d.png)

2. Close Visual Studio 2019, open folder contain code project, click Procuratio.sln to open project
![image](https://user-images.githubusercontent.com/82664727/159406056-23c530c2-7a06-4b5a-a487-05251e9a3742.png)

3. Choosen tab git changes, pull code latest
![image](https://user-images.githubusercontent.com/82664727/159406553-8ab55859-9bca-4a0e-98df-09f5f9d348c7.png)

4. Create new branch 
![image](https://user-images.githubusercontent.com/82664727/159406751-7449c548-8d4b-4b77-9ef4-9ebce400d49d.png)

5. Name branch name follow the rules, then click button "Create":
![image](https://user-images.githubusercontent.com/82664727/159407182-3ae1e071-83a2-4a8a-a9af-cbc43f397b18.png)
![image](https://user-images.githubusercontent.com/82664727/159407113-121d094c-9cb3-4edb-869b-f55969a5ee63.png)

6. You need to change connect string in appsetting.Development.json at Identity.Api and Product.Api
![image](https://user-images.githubusercontent.com/82664727/159408376-735fad86-cfb4-4194-9c42-d9f70af9b3de.png)
## In appsetting.Development.json at Identity.Api:
Change this ( CorsOrigins, AppDomain, IssuerUri
ConnectionStrings change Server to localhost
![image](https://user-images.githubusercontent.com/82664727/159408709-47774256-da6a-4d2e-9110-142a1c8a9fbf.png)
Change Uid and password (Pwd) like user, password you use to login in MySql
![image](https://user-images.githubusercontent.com/82664727/159408880-6fc91a3a-0af7-42ee-ade3-0ee55d7c7bd2.png)
And below change this
![image](https://user-images.githubusercontent.com/82664727/159408931-604eefdd-1401-4c1f-bb81-85078094f057.png)
## In appsetting.Development.json at Product.Api:
Change like this
![image](https://user-images.githubusercontent.com/82664727/159409763-d7b72072-f733-43ad-8170-21ec16d7ef8b.png)
And user, password change same appsetting.Development.json at Identity.Api
![image](https://user-images.githubusercontent.com/82664727/159409811-e6ee148e-4dd3-4787-b524-c8a00fe307f1.png)

7. Start up serve BE 
Click Set Starup Project...
![image](https://user-images.githubusercontent.com/82664727/159410650-ec124b38-1418-496c-ad25-7f57e1b6b842.png)

Start 2 server Identity.Api and Product.Api then click Ok

![image](https://user-images.githubusercontent.com/82664727/159410565-9acf0902-b6eb-47b7-852d-7ab3b73260a1.png)

8. When run 2 server, open postman run api: https://localhost:44343/api/Users/dummy to create user 
![image](https://user-images.githubusercontent.com/82664727/159423381-4bfde0bc-d670-4992-afac-3b0d5a98e503.png)

# Run front-end
1. Open Visual Studio Code and add folder contain front-end
![image](https://user-images.githubusercontent.com/82664727/159424807-074928a6-ebf8-40ea-ae46-17b34fe4083e.png)

2. Turn on terminal in vs code and instaill yarn : ```yarn install```
![image](https://user-images.githubusercontent.com/82664727/159425254-6576cc84-0b64-4343-84de-d296474f8623.png)

3. Open manage computer certificates in computer and export file localhost with private key and name localhost.pfx
![image](https://user-images.githubusercontent.com/82664727/159425927-6fff618d-06cc-422f-897d-9ef9fa09605b.png)
![image](https://user-images.githubusercontent.com/82664727/159426172-06ae5cce-93fe-44de-8a2b-c4428049a247.png)
![image](https://user-images.githubusercontent.com/82664727/159426978-1626dc80-3bd9-4e00-ac88-586e1656750d.png)

4. Convert localhost.pfx to localhost.pem : https://www.sslshopper.com/ssl-converter.html

5. Replace file localhost.pem in code fron-end 

6. ``` yarn run serve ``` to run front-end, open link : https://localhost:3000/
![image](https://user-images.githubusercontent.com/82664727/159427859-50dee439-637e-459b-a657-164d3c04916c.png)

7. Login with email and password as below:
![image](https://user-images.githubusercontent.com/82664727/159428270-cf474384-60d4-45a9-bf89-8dce7d63146e.png)

8. Change password:

![image](https://user-images.githubusercontent.com/82664727/159428594-01b6750d-0fca-4268-9a73-417cc9a8d6c5.png)

9. Done
![image](https://user-images.githubusercontent.com/82664727/159429079-25b119f8-b4d6-4f5d-8410-b2ee78e655b4.png)









