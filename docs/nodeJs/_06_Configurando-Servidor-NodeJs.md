## Configurando o servidor

Nesta etapa iremos desenvolver o código que é responsável por configurar e iniciar um servidor HTTP utilizando o framework Express em Node.js. A classe `App` cria uma instância do servidor Express e define os middlewares e rotas que serão utilizados.

Na função `middlewares()`, é definido um middleware que faz o parsing das requisições para o formato JSON.

Na função `routes()`, é definido o uso das rotas importadas do módulo `./controllers` para o caminho `/api/v1`.

Por fim, a instância do servidor é exportada como um módulo Node.js, que pode ser utilizado em outros arquivos para iniciar o servidor com a chamada `require('./app')`.

Um exemplo básico de como configurar um servidor HTTP utilizando o Express em Node.js:

```javaScript
// src/app.js
// Importa o framework Express
const express = require("express");

// Importa as rotas definidas no arquivo controllers.js
const routes = require("./controllers");

// Define a rota base para as APIs
routes.use('/api/v1', routes);

// Importa as configurações do banco de dados
require("./database");

class App {
  constructor() {
    // Inicializa o servidor
    this.server = express();
    // Configura os middlewares
    this.middlewares();
    // Configura as rotas
    this.routes();
  }

  // Configura os middlewares utilizados pelo servidor
  middlewares() {
    // Configura o servidor para interpretar os dados enviados no formato JSON
    this.server.use(express.json());
  }

  // Configura as rotas utilizadas pelo servidor
  routes() {
    // Define as rotas baseadas no arquivo controllers.js
    this.server.use(routes);
  }
}

// Exporta o servidor configurado e iniciado
module.exports = new App().server;
```

A classe `App` é responsável por configurar o servidor, seus middlewares e rotas. A classe é inicializada no final do código e seu atributo `server` é exportado para ser utilizado em outros arquivos.

A variável `express` é responsável por importar o framework Express.

A variável `routes` é responsável por importar as rotas definidas no arquivo `controllers.js`.

A linha `routes.use('/api/v1', routes)` define a rota base para todas as APIs definidas no arquivo `controllers.js`. Neste caso, todas as rotas terão como prefixo a string `/api/v1`.

A linha `require("./database")` importa as configurações do banco de dados utilizado pela aplicação.

A função `middlewares` é responsável por configurar os middlewares utilizados pelo servidor. Neste caso, o servidor é configurado para interpretar os dados enviados no formato JSON.

A função `routes` é responsável por configurar as rotas utilizadas pelo servidor. Neste caso, o servidor é configurado para utilizar as rotas definidas no arquivo `controllers.js`.

Por fim, a classe `App` é exportada com seu atributo `server` já iniciado, para que possa ser utilizada em outros arquivos.

## Testando o servidor

Após configurarmos o servidor em `app.js` podemos criar um arquivo `server.js` para inicializar o servidor e ouvir as requisições HTTP na porta especificada. O arquivo `server.js` é o ponto de entrada da aplicação, onde podemos configurar variáveis de ambiente, inicializar o banco de dados e outros serviços, além de iniciar o servidor HTTP.

um exemplo básico de arquivo `server.js` que utiliza o arquivo `app.js` para configurar e iniciar o servidor:

```javascript
// Importa o módulo que inicializa a aplicação
const app = require('./app');

// Define a porta em que o servidor irá escutar, utilizando a variável de ambiente "PORT" ou, caso não esteja definida, a porta 3000
const port = process.env.PORT || 3000;

// Inicia o servidor na porta especificada, e exibe uma mensagem no console para informar que a aplicação está sendo executada
app.listen(port, () => {
  console.log(`Servidor iniciado na porta ${port}`);
});
```

Basicamente, este arquivo inicia o servidor na porta especificada utilizando o módulo `app.js` que contém a definição da aplicação, e exibe uma mensagem no console para informar que o servidor foi iniciado com sucesso. Ele também utiliza a variável de ambiente `PORT`, caso esteja definida, para especificar a porta em que o servidor irá escutar. Isso é útil quando a aplicação está hospedada em um ambiente em nuvem, como o Heroku, que pode especificar a porta em que a aplicação deve ser executada através dessa variável de ambiente. Caso a variável `PORT` não esteja definida, o servidor irá escutar na porta `3000` por padrão.

Ao utilizar o `server.js`, também podemos separar as configurações do servidor da lógica da aplicação em si, o que torna o código mais organizado e modular. Além disso, podemos executar outras tarefas antes de iniciar o servidor, como por exemplo a validação de variáveis de ambiente e a configuração de bibliotecas e serviços externos.

Para rodar o Sevidor a partir do `server.js`, podemos executar o seguinte comando:

```bash
node src/server.js
```

Isso iniciará o servidor na porta que foi definida, neste caso a 3000. Abra um navegador e acesse `http://localhost:3000`. Você deve ver a mensagem "Cannot GET /" isso acontece porque não há nenhuma rota definida para a raiz do servidor. Quando o servidor recebe uma solicitação GET para a raiz, ele não sabe como responder porque não há uma rota definida para essa solicitação específica, pois definimos a rota base para as APIs `routes.use('/api/v1', routes)` em `src/app` e em cada rota em `controllers/index.js` definimos um prefixo de rota `router.use("/cliente", clienteRouters);`, sendo assim temos a seguinte estrutura de rotas:

- **Rota base**: `http://localhost:3000/api/v1` definida nas configuraçoes de `app.js`.
- **Rotas da API**: que é composta pela **rota base** mais o prefixo de rota definido em `src/controllers/index.js`, exemplo: `http://localhost:3000/api/v1/clientes`

```bash
http://localhost:3000/api/v1/clientes
```

- **Rotas com parametros** que permitem que o cliente da API forneça informações adicionais para a rota,Exemplo `http://localhost:3000/api/v1/clientes/:id`

```bash
http://localhost:3000/api/v1/clientes/1
```

```tree
nome-do-projeto/
├── src/
|   ├── config/
|   │   └── database.js
|   ├── controllers
|   |   └── clientes.js
|   |   └── enderecos.js
|   |   └── index.js
|   ├── database
|   |   ├── migrations/
|   |   |   └── data-clientes.js
|   |   |   └── data-enderecos.js
|   |   └── index.js
|   ├── models
|   |   └── Clientes.js
|   |   └── Enderecos.js
|   |   └── ...
|   ├── app.js
|   ├── server.js
├── node_modules/
|   └── ... 
├── .sequelizerc
├── package-lock.json
└── package.json
```
