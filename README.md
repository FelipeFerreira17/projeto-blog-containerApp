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






