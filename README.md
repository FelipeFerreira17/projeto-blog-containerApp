# Projeto blog containerApp
Projeto da DIO de criar um blog no container App do Azure

## Descrição
Nesse projeto vamos criar um blog usando serviços do Azure para demonstrar o funcionamento de aplicações web hospedadas na nuvem.

 ## Parte 1
 Crie um dockerfile para uma imagem do nginx
 
```More actions
FROM nginx:alpine
COPY blog/html /usr/share/nginx/html
```
Faça build da image e execute na porta 80.
```More actions
docker build -t blog-flp-apps:latest .
docker run -d -p 80:80 blog-flp-apps:latest
```
## Parte 2
Faça login no azure com o seguinte comando
```
az login
```
Crie um grupo de recursos

Crie o ACR e faça login nele
```
az group create --name nome-do-grupo --location nome-da-região
az acr create --resource-group nome-do-grupo --name nome-do-acr --sku basic
az acr login --name nome-do-acr
```
Colocar tag na imagem e fazer push para o ACR
```
docker tag blog-flp-app:latest nome-do-acr.azureacr.io/blog-flp-app:latest
docker push nome-do-acr.azureacr.io/blog-flp-app:latest
```

