**

## GitHub Action

 

 - Perform Sonar Analysis    
 - Build .NET Core    
 - Deploy the application into Azure Web App



# Setup

1. Fork into your github repository
2. Create account in [https://sonarcloud.io](https://sonarcloud.io) (ignore this step if you already have account)
3. Create sonar token from [https://sonarcloud.io/account/security](https://sonarcloud.io/account/security)
4. Go to github repository -> Settings -> Secrets -> Add a new secrets
5. Add Name as “SONAR_TOKEN” and sonar token value (created in step 3)
6. Go to Azure portal and create “Web App” (Publish - Code, Runtime Stack - .NET Core 3.1, Operating System - Linux)
7. Open .github/workflows/main.yml file and update your Web App name into variable - AZURE_WEBAPP_NAME
8. Open created Web App in Azure Portal and download profile file using “Get Publish Profile” link
9. Go to github repository -> Settings -> Secrets -> Add a new secrets
10. Add Name as “azureWebAppPublishProfile” and paste all contents of profile (downloaded in step 8)
11. That’s all, GitHub action will be triggered if you modify the file in the repository.
12. Open Web App and Sonarcloud URLs to see application and static code analysis results respectively
