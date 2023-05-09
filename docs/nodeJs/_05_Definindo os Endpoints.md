## Introdução

Definir os endpoints de uma API é uma das etapas mais importantes no desenvolvimento de uma API RESTful. Os endpoints são as URLs da API que respondem a solicitações HTTP dos clientes.

Algumas considerações na hora de definir os endpoints:

- **Identificar as operações que a API deve suportar** - Determine quais operações a API deve suportar, como criar, ler, atualizar e excluir recursos.
- **Definir os recursos** - Identifique os recursos que a API irá manipular, como "usuários", "produtos", "pedidos", etc. Cada recurso deve ter um endpoint associado.
- **Definir as URLs dos endpoints** - As URLs dos endpoints devem ser claras e descritivas. Elas devem incluir o nome do recurso e a operação que está sendo realizada, conforme necessário. Por exemplo, se a API gerencia usuários e você deseja criar um novo usuário, o endpoint pode ser algo como `POST /usuario`.
- **Definir os métodos HTTP** - Cada endpoint deve ser associado a um método HTTP específico que define a operação que está sendo realizada. Por exemplo, um endpoint para criar um novo recurso deve usar o método HTTP `POST`, enquanto um endpoint para atualizar um recurso existente deve usar o método HTTP `PUT` ou `PATCH`.
- **Definir os parâmetros** - Os endpoints podem incluir parâmetros na URL, como IDs de recursos, ou como parte do corpo da solicitação HTTP. Certifique-se de definir claramente quais parâmetros são necessários para cada endpoint.
- **Documentar a API** - Documente cada endpoint da API, incluindo sua URL, método HTTP, parâmetros, corpo da solicitação e resposta. A documentação deve ser clara e fácil de entender.
- **Testar a API** - Teste cada endpoint da API para garantir que ele esteja funcionando corretamente e que esteja respondendo corretamente às solicitações HTTP.

Ao seguir esses passos, é possível definir endpoints de API claros e fáceis de usar para os clientes, facilitando a integração de outras aplicações e serviços com sua API.

### Criando Endpoints

É comum organizar os endpoints em um diretório separado em uma API Node para manter uma estrutura de código mais organizada e escalável. Essa abordagem ajuda a separar a lógica de negócios da camada de infraestrutura e a facilitar a manutenção e a adição de novos endpoints à medida que a API cresce.

Uma boa prática é criar um diretório chamado `routes` ou `controllers`, onde os arquivos contendo as definições dos endpoints são mantidos. Esses arquivos podem ser nomeados de acordo com a funcionalidade que eles oferecem, como `clientes.js`, `enderecos.js` ou `produtos.js`, por exemplo.

Cada arquivo de definição de endpoint deve exportar um objeto com as rotas correspondentes ao endpoint. Por exemplo, um arquivo `clientes.js` pode conter as rotas `/clientes`, `/clientes/:id` etc.

Um exemplo de código para criar um endpoint `/clientes` usando o framework Express em um arquivo `clientes.js` dentro de um diretório `controllers` seria:

```javascript
// src/controllers/clientes.js
const express = require('express')
const router = express.Router()

// Importa o Models Cliente
const Cliente = require("../../models/Clientes")

// Define a rota para buscar todos os clientes
router.get('/', async (req, res) => {
  try {
    // Busca todos os clientes, mas exclui a senha da resposta
    const clientes = await Cliente.findAll({
      attributes: { exclude: ["senha"] } // Atributos que devem ser excluídos da resposta
    });
    // Envia a resposta como JSON com status 200 (OK)
    res.status(200).json(clientes);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});

// Define a rota para buscar um cliente pelo ID
router.get('/:id', async (req, res) => {
  try {
    // Busca um cliente pelo ID, mas exclui a senha e o ID da resposta
    const cliente = await Cliente.findByPk(req.params.id, {
      attributes: { exclude: ["senha", "id"] } // Atributos que devem ser excluídos da resposta
    });
    // Envia a resposta como JSON com status 200 (OK)
    res.status(200).json(cliente);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});

// Define a rota para Criar um cliente
router.post('/', async (req, res) => {
  try {
    // Cria um novo cliente com os dados recebidos no corpo da requisição
    const cliente = await Cliente.create(req.body);
    // Envia a resposta como JSON com status 201 (Created)
    res.status(201).json(cliente);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});

// Define a rota para atualizar um cliente pelo ID
router.put('/:id', async (req, res) => {
  try {
    // Busca o cliente pelo ID
    const cliente = await Cliente.findByPk(req.params.id);
    
    // Verifica se o cliente foi encontrado
    if (!cliente) {
      return res.status(404).json({ error: 'Cliente não encontrado' });
    }
    
    // Atualiza as informações do cliente
    const updatedCliente = await cliente.update(req.body);
    
    // Retorna o cliente atualizado como resposta
    res.json(updatedCliente);
  } catch (error) {
    // Em caso de erro, loga o erro e retorna uma mensagem de erro ao cliente
    console.log(error);
    res.status(500).json({ error: 'Erro ao atualizar o cliente' });
  }
});

// Define a rota para apagar um cliente pelo ID
router.delete('/:id', async (req, res) => {
  try {
    // Busca um cliente pelo ID
    const cliente = await Cliente.findByPk(req.params.id);
    // Verifica se o cliente foi encontrado
    if (!cliente) {
      // Se o cliente não foi encontrado, envia uma mensagem de erro com status 404 (Não encontrado)
      return res.status(404).send("Cliente não encontrado");
    }
    // Remove o cliente do banco de dados
    await cliente.destroy();
    // Envia a resposta com status 204 (No Content) para indicar que o cliente foi removido com sucesso
    res.sendStatus(204);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});


module.exports = router
```

O código apresentado é um arquivo de definição de rotas para uma API RESTful em Node.js. Primeiramente, ele importa o módulo 'express' e cria um novo objeto de roteador com o método 'Router()' desse módulo.

Em seguida, ele importa o modelo de dados Cliente e define rotas para buscar, criar, atualizar e deletar clientes.

- '/clientes' permite atravez do método HTTP GET a busca de todos os clientes no banco de dados, excluindo a senha dos clientes retornados na resposta.

- '/clientes/:id' permite a busca de um cliente específico no banco de dados pelo seu ID, também excluindo a senha e o ID do cliente na resposta.

- '/clientes' com método HTTP POST é utilizada para criar um novo cliente, recebendo os dados do cliente no corpo da requisição.

- '/clientes/:id' com método HTTP PUT é utilizada para atualizar as informações de um cliente específico pelo seu ID.

- '/clientes/:id' com método HTTP DELETE é utilizada para excluir um cliente do banco de dados pelo seu ID.

Em caso de erro em alguma dessas operações, a API retorna uma mensagem de erro com status 500 (Erro interno do servidor). Se algum cliente não for encontrado em operações de busca, retorna uma mensagem de erro com status 404 (Não encontrado).

Esse arquivo define um roteador do Express que possui as rotas `/users`, `/users/:id`, `/users/:id/orders`, `/users/:id/orders/:orderId` etc. O código para cada rota pode ser definido dentro de cada manipulador de rota correspondente, como mostrado nos comentários acima.

O mesmo padrão pode ser utilizado para criar o endpoint `/enderecos` usando o framework Express em um arquivo `usr/controllers/enderecos.js` :

```javascript
// usr/controllers/enderecos.js
const express = require('express')
const router = express.Router()

// Importa o Models Endereco
const Endereco = require("../../models/Enderecos")

// Define a rota para buscar todos os enderecos
router.get('/', async (req, res) => {
  try {
    // Busca todos os enderecos
    const enderecos = await Endereco.findAll({
      attributes: { exclude: ["senha"] } // Atributos que devem ser excluídos da resposta
    });
    // Envia a resposta como JSON com status 200 (OK)
    res.status(200).json(enderecos);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});

// Define a rota para buscar um endereco pelo ID
router.get('/:id', async (req, res) => {
  try {
    // Busca um endereco pelo ID, mas exclui a senha e o ID da resposta
    const endereco = await Endereco.findByPk(req.params.id, {
      attributes: { exclude: ["senha", "id"] } // Atributos que devem ser excluídos da resposta
    });
    // Envia a resposta como JSON com status 200 (OK)
    res.status(200).json(endereco);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});

// Define a rota para Criar um endereco
router.post('/', async (req, res) => {
  try {
    // Cria um novo endereco com os dados recebidos no corpo da requisição
    const endereco = await Endereco.create(req.body);
    // Envia a resposta como JSON com status 201 (Created)
    res.status(201).json(endereco);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});

// Define a rota para atualizar um endereco pelo ID
router.put('/:id', async (req, res) => {
  try {
    // Busca o endereco pelo ID
    const endereco = await Endereco.findByPk(req.params.id);
    
    // Verifica se o endereco foi encontrado
    if (!endereco) {
      return res.status(404).json({ error: 'Endereco não encontrado' });
    }
    
    // Atualiza as informações do endereco
    const updatedEndereco = await endereco.update(req.body);
    
    // Retorna o endereco atualizado como resposta
    res.json(updatedEndereco);
  } catch (error) {
    // Em caso de erro, loga o erro e retorna uma mensagem de erro ao endereco
    console.log(error);
    res.status(500).json({ error: 'Erro ao atualizar o endereco' });
  }
});

// Define a rota para apagar um endereco pelo ID
router.delete('/:id', async (req, res) => {
  try {
    // Busca um endereco pelo ID
    const endereco = await Endereco.findByPk(req.params.id);
    // Verifica se o endereco foi encontrado
    if (!endereco) {
      // Se o endereco não foi encontrado, envia uma mensagem de erro com status 404 (Não encontrado)
      return res.status(404).send("Endereco não encontrado");
    }
    // Remove o endereco do banco de dados
    await endereco.destroy();
    // Envia a resposta com status 204 (No Content) para indicar que o endereco foi removido com sucesso
    res.sendStatus(204);
  } catch (error) {
    // Em caso de erro, loga o erro no console e envia uma mensagem de erro com status 500 (Erro interno do servidor)
    console.error(error);
    res.status(500).send("Erro interno do servidor");
  }
});


module.exports = router
```

Essa é apenas uma abordagem possível para criar endpoints em uma API Node, e existem várias outras maneiras de fazer isso, dependendo das necessidades específicas de cada API.

para que essas rotas possam ser utilizadas por um servidor NodeJs temos que  instancia-las, é comum criar um arquivo separado para gerenciar as rotas. Nesse arquivo, geralmente são definidos os prefixos dos endpoints da API. Não há uma convenção oficial para o nome dos arquivos de configuração de rotas em Node.js, mas geralmente os desenvolvedores utilizam nomes como "routes.js", "controllers/index.js", "api.js", "apiRoutes.js", "router.js", entre outros.

vamaos utilizar o `src/controllers/index.js`, que ficara com o seguinte codigo.

```js
// src/controllers/index.js
const express = require('express');
const router = express.Router();

// Importa as rotas do arquivo "clientes.js"
const clienteRouters = require("./clientes")
// Importa as rotas do arquivo "enderecos.js"
const enderecoRouters = require("./enderecos")

// Registra as rotas do arquivo "clientes.js" no path "/cliente"
router.use("/cliente", clienteRouters);
// Registra as rotas do arquivo "enderecos.js" no path "/endereco"
router.use("/endereco", enderecoRouters);

// Exporta as rotas registradas
module.exports = router;
```

Nesse código, um arquivo de rotas central é criado para importar todas as rotas da API. As rotas são separadas em arquivos específicos, onde cada arquivo contém as rotas para uma entidade ou recurso específico da API. As rotas são registradas usando o método `use()` do router do Express.

A partir daqui, você pode começar a criar as rotas da API RESTful, definindo as operações HTTP, os **parametros** e as respostas esperadas. O express facilita muito a criação de rotas e manipulação de requisições e respostas HTTP. Com as rotas definidas, você pode criar a lógica de negócios da aplicação, que pode incluir acesso a banco de dados, autenticação e autorização, validação de dados, entre outros.

#### Parâmetros

Parâmetros de rotas, ou route parameters, são uma forma de passar informações dinâmicas para a sua aplicação através da URL. Eles são utilizados para identificar um recurso específico, como um usuário ou um produto, ou para passar  informações adicionais para a nossa aplicação. Podemos dividir os parâmetros em:

- **Parâmetros de rota** Em uma URL, os parâmetros de rota (Route Parameters) são definidos após a rota base e são indicados pelo caractere `:` seguido do nome do parâmetro. Por exemplo, considerando a rota `/users/:id`, o parâmetro `id` é um parâmetro de rota.

Ao receber uma requisição contendo um parâmetro de rota, o Express armazena o valor desse parâmetro em um objeto chamado `params`, que é uma propriedade do objeto `request` (ou `req`, para abreviar). O valor do parâmetro pode ser acessado através desse objeto.

Um exemplo de como usar parâmetros foi Definido na rota para buscar um endereco pelo ID mencionado no exemplo anterior.

Ao final desta etapa você tera a seguinte estrutura de diretorio:

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
├── node_modules/
|   └── ... 
├── .sequelizerc
├── package-lock.json
└── package.json
```
