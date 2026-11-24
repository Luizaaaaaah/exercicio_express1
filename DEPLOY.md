# Publicação da API de notas — Aula 08

As mudanças nesta branch preparam o servidor Express para deploy no Render:

- A porta agora utiliza **process.env.PORT || 3000**.
- O CORS passa a utilizar o middleware **cors()**, instalado pelo projeto, com tratamento apropriado de requisições preflight.
- A leitura do arquivo JSON utiliza caminho baseado no diretório do servidor.

## Testar localmente

~~~bash
npm install
node server.js
~~~

Teste **http://localhost:3000/api/notes**. Para o CRUD completo, utilize a [coleção Postman da disciplina](https://github.com/Luizaaaaaah/Programacao_Web/blob/reorganizacao/atividades/aula-08/postman/notas-crud.postman_collection.json).

## Render

Crie um serviço **Web Service** conectado ao repositório, utilizando:
- Linguagem/Runtime: Node.js
- Build Command: **npm install**
- Start Command: **node server.js**

O serviço informará uma URL pública. Teste o endpoint **/api/notes** antes de configurar o front-end.

## Limitações

O arquivo **data.json** continua sendo a fonte de dados. Em serviços que não garantem armazenamento persistente, notas criadas após a inicialização podem desaparecer em reinícios ou novos deploys. Esta atividade tem finalidade didática; não publique dados pessoais reais.

Esta branch contém ajustes de configuração **não validados em execução por este assistente**. Revise e teste antes de integrar à main.

O repositório original contém arquivos **node_modules** já rastreados. Um arquivo .gitignore evita novos arquivos, mas não remove automaticamente os antigos do Git.
