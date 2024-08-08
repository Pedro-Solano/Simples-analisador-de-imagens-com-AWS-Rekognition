#Analisador simples de imagens com AWS Rekognition

Código para criação de uma função Lambda e demais recursos necessários na AWS, utilizando o framework Serveless `(https://www.serverless.com/)`.

A função recebe a url de uma imagem e retorna um texto em português contendo a análise da imagem.

A análise é feita pelo AWS Rekognition, que retorna um texto em inglês.

A tradução para o português utilizando o AWS Translate.

Utiliza-se o Jest para implementação dos testes e o pacote NTL para facilitar a execução desses.

O comando `sls deploy` faz o deploy da função na AWS e retorna uma URL para invocação dela, no formato: 

```bash
https://xxxxxxxxxx.execute-api.us-east-1.amazonaws.com/
```
A URL da imagem a ser analisada deve ser informada como query string. O nome do parâmetro é imageUrl. 

Exemplo:
```bash
https://xxxxxxxxxx.execute-api.us-east-1.amazonaws.com/imageUrl="URL da imagem"
```

O resultado será exibido na tela do navegador.

Projeto do curso "Aplicações Serverless na AWS - Erick Wendel"

###Comandos importantes:

Instalação do framework serverless e do Jest:

```bash
npm i -D jest@28 serverless@3.16
```

Instalação do aws-sdk, para utilização dos serviços Rekognition e Translate.

```bash
npm i aws-sdk@2.1128 
```

Instalação do NTL:

```bash
npm i -g ntl 
```

Instalação da biblioteca Axios

```bash
npm i axios@0.17
```
