# Projeto blog containerApp
Projeto da DIO de criar um blog no container App do Azure

## Descrição
Nesse projeto vamos criar um blog usando serviços do Azure para demonstrar o funcionamento de aplicações web hospedadas na nuvem.

 ## Parte1
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





