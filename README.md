# Firstly, you have to download all software below :
- Visual Studio 2019
- Visual Studio Code
- Nodejs
- Git
- Postman
- MySQL Workbench

# Secondly, get source code LTS LGT Procuratio Project
 1. You need to login with account lotus (...@lotus-ts.com)
 
 2. Click link to get source : https://dev.azure.com/LGTVN/_git/LTS%20LGT%20Procuratio%20Project
![image](https://user-images.githubusercontent.com/82664727/159402637-75a3ff6d-d528-4604-8844-0a970db5e4bc.png)
Copy link :  
![image](https://user-images.githubusercontent.com/82664727/159403054-c534188d-8372-4127-a712-95f22e21d0d9.png)

3. Open Visual Studio 2019, click **clone a repository**, paste link you just copied to repository location (change path if neccessary)
![image](https://user-images.githubusercontent.com/82664727/159404483-8abbddd5-b050-44ce-b3e2-85952568e515.png)

# Run back-end
1. When cloning code successfully, click _branch master_, tab _remote_, choose branch **_dev/dev_product_**
![image](https://user-images.githubusercontent.com/82664727/159405729-9b8ca44e-80a2-4401-be7c-548adf116f4d.png)

2. Close Visual Studio 2019, open folder which contain code project, click _**Procuratio.sln**_ to open project
![image](https://user-images.githubusercontent.com/82664727/159406056-23c530c2-7a06-4b5a-a487-05251e9a3742.png)

3. Choose tab **_git changes_**, pull latest code 
![image](https://user-images.githubusercontent.com/82664727/159406553-8ab55859-9bca-4a0e-98df-09f5f9d348c7.png)

4. Create new branch 
![image](https://user-images.githubusercontent.com/82664727/159406751-7449c548-8d4b-4b77-9ef4-9ebce400d49d.png)

5. Set branch name following the rules, then click button **_Create_**:
![image](https://user-images.githubusercontent.com/82664727/159407182-3ae1e071-83a2-4a8a-a9af-cbc43f397b18.png)
![image](https://user-images.githubusercontent.com/82664727/159407113-121d094c-9cb3-4edb-869b-f55969a5ee63.png)

6. Change connection string in **_appsetting.Development.json_** at _**Identity.Api**_ and _**Product.Api**_
![image](https://user-images.githubusercontent.com/82664727/159408376-735fad86-cfb4-4194-9c42-d9f70af9b3de.png)
## In appsetting.Development.json at Identity.Api:
Change _CorsOrigins_, _AppDomain_, _IssuerUri_
In _ConnectionStrings _ change _Server_ to your localhost
![image](https://user-images.githubusercontent.com/82664727/159408709-47774256-da6a-4d2e-9110-142a1c8a9fbf.png)
Change Uid and password (Pwd) like user, password you use to login in MySql Workbench
![image](https://user-images.githubusercontent.com/82664727/159408880-6fc91a3a-0af7-42ee-ade3-0ee55d7c7bd2.png)
And change this
![image](https://user-images.githubusercontent.com/82664727/159408931-604eefdd-1401-4c1f-bb81-85078094f057.png)
## In appsetting.Development.json at Product.Api:
Change like this
![image](https://user-images.githubusercontent.com/82664727/159409763-d7b72072-f733-43ad-8170-21ec16d7ef8b.png)
And user, password are the same with appsetting.Development.json at Identity.Api
![image](https://user-images.githubusercontent.com/82664727/159409811-e6ee148e-4dd3-4787-b524-c8a00fe307f1.png)

7. Run the solution 
Right click to your solution and select _Set Starup Project_...
![image](https://user-images.githubusercontent.com/82664727/159410650-ec124b38-1418-496c-ad25-7f57e1b6b842.png)

Select _Multipkle startup project_ and change _Action_ of Identity.Api and Product.Api to **Start** then click _Apply/Ok_

![image](https://user-images.githubusercontent.com/82664727/159410565-9acf0902-b6eb-47b7-852d-7ab3b73260a1.png)

8. When Identity.Api and Product.Api are run successfully , open postman and run api: https://localhost:44343/api/Users/dummy to create user 
![image](https://user-images.githubusercontent.com/82664727/159423381-4bfde0bc-d670-4992-afac-3b0d5a98e503.png)

# Run front-end
1. Open **ClientApp** folder at _Product.Api_ project in Visual Studio Code  
![image](https://user-images.githubusercontent.com/82664727/159424807-074928a6-ebf8-40ea-ae46-17b34fe4083e.png)

2. Turn on terminal or Ctrl ~ in Visual Studio Code and install yarn : ```yarn install```
![image](https://user-images.githubusercontent.com/82664727/159425254-6576cc84-0b64-4343-84de-d296474f8623.png)

3. Open manage computer certificates in computer and export file localhost with private key that you want and name will be **localhost.pfx**
![image](https://user-images.githubusercontent.com/82664727/159425927-6fff618d-06cc-422f-897d-9ef9fa09605b.png)
![image](https://user-images.githubusercontent.com/82664727/159426172-06ae5cce-93fe-44de-8a2b-c4428049a247.png)
![image](https://user-images.githubusercontent.com/82664727/159426978-1626dc80-3bd9-4e00-ac88-586e1656750d.png)

4. Convert localhost.pfx to localhost.pem : https://www.sslshopper.com/ssl-converter.html

5. Replace file localhost.pem in Visual Studio Code  

6. ``` yarn run serve ``` to run front-end and _Ctrl Click_ to the link : https://localhost:3000/
![image](https://user-images.githubusercontent.com/82664727/159427859-50dee439-637e-459b-a657-164d3c04916c.png)

7. Login with email and password as below:
![image](https://user-images.githubusercontent.com/82664727/159428270-cf474384-60d4-45a9-bf89-8dce7d63146e.png)

8. Change password when first login:

![image](https://user-images.githubusercontent.com/82664727/159428594-01b6750d-0fca-4268-9a73-417cc9a8d6c5.png)

9. Done
![image](https://user-images.githubusercontent.com/82664727/159429079-25b119f8-b4d6-4f5d-8410-b2ee78e655b4.png)









