# Integração CRM e ERP com AWS Lambda e S3

## Este **README.md** contém todas as informações sobre o projeto, incluindo as instruções de **instalação**, **como usar**, **deploy**, e outros detalhes importantes.

Este projeto implementa uma integração simples entre dois sistemas fictícios (CRM e ERP), utilizando AWS Lambda e S3. A infraestrutura é gerenciada via Serverless Framework.

## Tabela de Conteúdos
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Como Usar](#como-usar)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Deploy](#deploy)
- [Licença](#licença)

## Pré-requisitos
- Node.js (versão 14 ou superior)
- AWS CLI configurado com suas credenciais da AWS
- Serverless Framework instalado globalmente:
  ```bash
  npm install -g serverless

## Instalação
- Clone o repositório:
  git clone https://github.com/usuario/serverless_framework.git
- Acesse a pasta do projeto:
  cd serverless_framework
- Instale as dependências do projeto. Se você já tem o Node.js e o Serverless Framework instalados, execute:
  npm install
- Configure suas credenciais AWS: Certifique-se de ter o AWS CLI configurado. Se ainda não tiver, execute o seguinte comando e forneça suas credenciais AWS:
  aws configure
- Se necessário, instale o Serverless Framework globalmente: Caso não tenha o Serverless Framework instalado, faça isso com:
  npm install -g serverless

## Como usar
- Execute o seguinte comando para fazer o deploy da infraestrutura na AWS (Lambda e S3):
  serverless deploy
- Isso criará as funções Lambda e o bucket S3 na AWS de acordo com a configuração definida no serverless.yml.
- Para invocar a função Lambda, utilize o comando:
  serverless invoke --function nome_da_funcao

## Testando a aplicação
- Após o deploy, você pode testar o fluxo completo da integração ERP e CRM, que processa os dados do ERP, transforma em um formato JSON e os armazena no bucket S3. O próximo passo seria o Lambda #02, que pega os dados do S3 e envia ao CRM.

## Tecnologias Utilizadas
- AWS Lambda: Utilizado para processar e transformar os dados entre o ERP e o CRM.
- Amazon S3: Armazena os dados transformados no formato JSON.
- Serverless Framework: Ferramenta para definir e gerenciar a infraestrutura na AWS como código.
- Python: Linguagem utilizada para escrever as funções Lambda.

## Deploy
- Para realizar o deploy da infraestrutura na AWS, basta rodar o seguinte comando dentro da pasta do projeto:
  serverless deploy
- Este comando irá provisionar os recursos necessários na AWS, como funções Lambda e o bucket S3, utilizando a configuração definida no arquivo serverless.yml. Após o deploy, você pode verificar o funcionamento do sistema através da invocação das funções ou por meio do log gerado.
