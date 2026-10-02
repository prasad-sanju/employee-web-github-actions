# Employee Web App - GitHub Actions CI/CD

Simple HTML/CSS/JavaScript web application for learning GitHub Actions, Docker, Azure Container Registry and Azure Web App.

## Run locally
Open `index.html` in a browser.

## Docker
`docker build -t employee-web-app .`
`docker run --rm -p 8080:80 employee-web-app`
Open http://localhost:8080

## CI workflow
Checkout -> validate files -> Docker build -> run container -> curl test.

## CD workflow
Azure OIDC login -> ACR login -> Docker build -> push -> Azure Web App deployment.

Required GitHub secrets: AZURE_CLIENT_ID, AZURE_TENANT_ID, AZURE_SUBSCRIPTION_ID, ACR_NAME, ACR_LOGIN_SERVER, WEBAPP_NAME.
