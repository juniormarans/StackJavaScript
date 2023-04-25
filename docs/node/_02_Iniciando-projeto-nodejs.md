# Iniciando no Node.js

Após a instalação do Node.js e do npm, o próximo passo para criar um projeto de API RESTful em Node.js é seguir os seguintes passos:

## Passo 1 Crie um diretório para o projeto e navegue até ele

```bash
mkdir projetos/nome-do-projeto #cria um diretório
cd projetos/nome-do-projeto # move até o diretório
```

Lembre-se organizar seu ambiente de desenvolvimento é uma parte importante para garantir uma experiência de programação eficiente e produtiva, neste caso criamos um diretório `projetos` onde armazenaremos nossas aplicaçoes.

## Passo 2 Inicialize o projeto Node.js com o npm

```bash
npm init -y
```

Isso irá criar um arquivo `package.json` no diretório do projeto, que contém informações sobre o projeto e suas dependências. O arquivo package.json é um arquivo em formato JSON que contém metadados sobre o projeto e suas dependências.

Este arquivo é importante porque ele armazena informações sobre as dependências do projeto, scripts, configurações e outras informações importantes que serão utilizadas para gerenciar o projeto.

Aqui está um exemplo de um arquivo package.json típico:

```json
{
  "name": "exemplo",
  "version": "1.0.0",
  "description": "Exemplo de aplicação Node.js",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "dependencies": {
    "express": "^4.17.1"
  },
  "devDependencies": {
    "nodemon": "^2.0.7"
  },
  "engines": {
    "node": ">=14.0.0",
    "npm": ">=7.0.0"
  },
  "license": "MIT",
  "repository": {
    "type": "git",
    "url": "https://github.com/nome-do-repositorio.git"
  },
  "author": {
    "name": "Nome do Autor",
    "email": "email@dominio.com"
  },
  "keywords": [
    "node",
    "exemplo",
    "rest",
    "api"
  ],
  "contributors": [
    {
      "name": "Nome do Contribuidor",
      "email": "email@dominio.com"
    }
  ]
}
```

Vejamos agora o que cada um desses campos significa:

- `name`: é o nome do seu projeto e deve ser único no registro de pacotes do npm.

- `version`: é a versão atual do seu projeto.

- `description`: é uma descrição breve do seu projeto.

- `main`: é o arquivo principal do seu projeto.

- `scripts`: é um objeto que contém vários comandos que podem ser executados para realizar tarefas específicas, como iniciar a aplicação ou executar testes automatizados.

- `dependencies`: é um objeto que contém todas as dependências que sua aplicação precisa para rodar corretamente. Essas dependências serão instaladas automaticamente pelo npm.

- `devDependencies`: é um objeto que contém todas as dependências que são necessárias apenas durante o desenvolvimento da aplicação, como por exemplo, testes automatizados. Essas dependências não serão instaladas quando a aplicação for instalada em um ambiente de produção.

- `engines`: é um objeto que especifica a versão mínima do Node.js e do npm necessária para rodar sua aplicação.

- `license`: é a licença sob a qual seu projeto é disponibilizado.

- `repository`: é a URL do repositório do seu projeto.

- `author`: é o nome do autor do projeto e seu email.

- `keywords`: são palavras-chave que descrevem seu projeto. Essas palavras-chave são usadas pelo npm para categorizar seu projeto e facilitar a busca.

- `contributors`: é uma lista de contribuidores do projeto.

Essas são algumas das principais propriedades que podem ser encontradas em um arquivo package.json. Além dessas, existem outras propriedades que podem ser definidas, dependendo das necessidades do projeto.
Em resumo, o arquivo package.json é fundamental em projetos Node.js, pois ele ajuda a gerenciar dependências, configurar scripts e outras configurações importantes para o projeto.

## Passo 3 Instale os pacotes necessários para criar uma API RESTful em Node.js

   ```bash
   npm i express body-parser cors 

   ```

   O pacote `express` é o framework para criação de aplicações Node.js, `body-parser` é usado para analisar o corpo das requisições HTTP e `cors` é utilizado para habilitar o acesso de outras origens (como outros servidores) à API.

## Passo 4 Crie um arquivo `index.js` no diretório do projeto e configure o servidor express

```js
const express = require('express');
const bodyParser = require('body-parser');
const cors = require('cors');

const app = express();
const port = 3000;

app.use(cors());
app.use(bodyParser.json());

app.get('/', (req, res) => {
    res.send('Bem-vindo à API RESTful');
});

app.listen(port, () => {
    console.log(`Servidor iniciado em http://localhost:${port}`);
});
```

Vamos entender o que está acontecendo em cada linha do código:

```js
const express = require('express');
```

Aqui estamos importando o módulo `express` para o nosso código. O `express` é um framework para criação de aplicações web em Node.js. A palavra-chave `const` é utilizada para declarar uma constante.

```js
const bodyParser = require('body-parser');
```

Estamos importando o módulo `body-parser` que é um middleware para análise do corpo das requisições HTTP.

```js
const cors = require('cors');
```

Estamos importando o módulo `cors` que é um middleware que permite o acesso de outras origens à API.

```js
const app = express();
```

Aqui estamos criando a nossa aplicação express, que será utilizada para configurar as rotas e endpoints da API.

```js
const port = 3000;
```

Definimos uma variável para a porta em que o servidor express será iniciado.

```js
app.use(cors());
app.use(bodyParser.json());
```

Aqui estamos utilizando os middlewares `cors` e `body-parser` que importamos anteriormente para nossa aplicação express. O `cors` habilita o acesso de outras origens à API e o `body-parser` analisa o corpo das requisições HTTP.

```js
app.get('/', (req, res) => {
  res.send('Bem-vindo à API RESTful');
});
```

Aqui estamos definindo uma rota para a raiz da nossa aplicação (`/`). Quando um usuário acessar essa rota, a API enviará como resposta uma mensagem de boas-vindas.

```js
app.listen(port, () => {
  console.log(`Servidor iniciado em http://localhost:${port}`);
});
```

Finalmente, aqui estamos iniciando o servidor express na porta definida anteriormente e imprimindo uma mensagem de sucesso no console.

## Passo 5 Teste o servidor

Para rodar o codigo criado em `index.js` execute o seguinte comando:

```bash
node index.js
```

Isso iniciará o servidor na porta 3000. Abra um navegador e acesse `http://localhost:3000`. Você deve ver a mensagem "Bem-vindo à API RESTful".

A partir daqui, você pode começar a criar as rotas da API RESTful, definindo as operações HTTP, os **parametros** e as respostas esperadas. O express facilita muito a criação de rotas e manipulação de requisições e respostas HTTP. Com as rotas definidas, você pode criar a lógica de negócios da aplicação, que pode incluir acesso a banco de dados, autenticação e autorização, validação de dados, entre outros.

## Parâmetros

Parâmetros de rotas, ou route parameters, são uma forma de passar informações dinâmicas para a sua aplicação através da URL. Eles são utilizados para identificar um recurso específico, como um usuário ou um produto, ou para passar  informações adicionais para a nossa aplicação. Podemos dividir os parâmetros em:

### Parâmetros de rota

Em uma URL, os parâmetros de rota (Route Parameters) são definidos após a rota base e são indicados pelo caractere `:` seguido do nome do parâmetro. Por exemplo, considerando a rota `/users/:id`, o parâmetro `id` é um parâmetro de rota.

Ao receber uma requisição contendo um parâmetro de rota, o Express armazena o valor desse parâmetro em um objeto chamado `params`, que é uma propriedade do objeto `request` (ou `req`, para abreviar). O valor do parâmetro pode ser acessado através desse objeto.

Aqui está um exemplo de como usar parâmetros de rota em uma aplicação Node.js com Express:

```javascript
const express = require('express');
const bodyParser = require('body-parser');
const cors = require('cors');

const app = express();
const port = 3000;

app.use(cors());
app.use(bodyParser.json());

// Definindo uma rota inicial
app.get('/', (req, res) => {
    res.send('Bem-vindo à API RESTful');
});

// Definindo uma rota com um parâmetro
app.get('/usuario/:id', (req, res) => {
    const userId = req.params.id;
    res.send(`Informações do usuário com ID ${userId}`);
});

app.listen(port, () => {
    console.log(`Servidor iniciado em http://localhost:${port}`);
});
```

Nesse exemplo, criamos a rota `/usuario/:id` recebe um parâmetro de rota `id`. Quando um usuário acessa essa rota com um ID específico, o Express armazena esse ID no objeto `params` e podemos acessá-lo através da propriedade `id`. Em seguida, podemos usar esse ID para buscar informações específicas do usuário com esse ID em um banco de dados, por exemplo.

Para testar essa rota, basta acessar `http://localhost:3000/usuario/123` no navegador, onde `123` é um exemplo de ID de usuário. A mensagem de resposta irá incluir esse ID na mensagem.

Claro, aqui vão alguns exemplos de como utilizar parâmetros de query string e route parameters em uma aplicação Node.js com Express:

### Parâmetros de Query String

```javascript
const express = require('express');
const bodyParser = require('body-parser');
const cors = require('cors');

const app = express();
const port = 3000;

app.use(cors());
app.use(bodyParser.json());

// Definindo uma rota inicial
app.get('/', (req, res) => {
    res.send('Bem-vindo à API RESTful');
});

// Definindo uma rota com um parâmetro
app.get('/usuario/:id', (req, res) => {
    const userId = req.params.id;
    res.send(`Informações do usuário com ID ${userId}`);
});

// Rota que recebe parâmetros via query string
app.get('/usuario', (req, res) => {
    const nome = req.query.nome;
    const idade = req.query.age;
    res.send(`Nome: ${nome}, Idade: ${idade}`);
});
app.listen(port, () => {
    console.log(`Servidor iniciado em http://localhost:${port}`);
});
```

Nesse exemplo, a rota `/usuario` recebe os parâmetros `nome` e `idade` via query string. Esses parâmetros são acessados através do objeto `req.query`.

Para testar essa rota, basta acessar `http://localhost:3000/usuario?nome=João&idade=30` no navegador.
