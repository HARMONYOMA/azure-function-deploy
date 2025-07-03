# Azure Function CI/CD Pipeline with Monitoring

This project demonstrates how to build, deploy, secure, and monitor an HTTP-triggered Azure Function using JavaScript. The deployment is fully automated via GitHub Actions with integrated Azure CLI for monitoring setup.

## 📂 Project Structure

```text
myHttpFunctionProj/
├── HttpExample/                  # Azure Function code
│   ├── function.json
│   └── index.js
│
├── .github/
│   └── workflows/
│       └── azure-function-deploy.yml    # GitHub Actions workflow
│
├── host.json
└── package.json
``` 

## 🚀 Deployment Pipeline

The project uses GitHub Actions to:
- Build and deploy the Azure Function to Azure.
- Configure monitoring alerts using Azure CLI.
- Send email notifications when the function experiences HTTP 5xx errors.

## 🔐 Security

The function is secured with **API keys**. Only requests with the correct key can successfully invoke the function.

## 📊 Monitoring and Alerts

Monitoring is integrated with **Azure Monitor** and **Application Insights**. Alerts are configured to:
- Notify you via email when the function encounters 5xx errors.
- Provide deployment and function health insights.

## ⚙️ GitHub Secrets Required
You need to create the following GitHub secrets in your repository:
- `AZURE_FUNCTIONAPP_NAME`: Your Azure Function App name.
- `AZUREAPPSERVICE_PUBLISHPROFILE`: Publish profile from Azure.
- `AZURE_CREDENTIALS`: Azure service principal JSON for authentication.
- `APPINSIGHTS_INSTRUMENTATIONKEY`: Your App instrumentation key.
- `APPLICATIONINSIGHTS_CONNECTION_STRING`: Your App connection string.
- `ALERT_EMAIL`: youremail@example.com


## 🛠️ Setup Instructions

1. Clone this repository:
```bash
git clone <your-repo-url>
cd myHttpFunctionProj
```

2.  Create the following GitHub secrets in your repository:

- AZURE_FUNCTIONAPP_NAME
- AZUREAPPSERVICE_PUBLISHPROFILE
- AZURE_CREDENTIALS
- APPINSIGHTS_INSTRUMENTATIONKEY
- APPLICATIONINSIGHTS_CONNECTION_STRING
- ALERT_EMAIL

3.  Push your code to the main branch: 
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

4. CI/CD will run automatically:

GitHub Actions will automatically:

- Deploy your Azure Function.
- Set up monitoring.
- Configure email alerts.

📞 Contact
For questions or support, please contact: Email: anigbogup@gmail.com
