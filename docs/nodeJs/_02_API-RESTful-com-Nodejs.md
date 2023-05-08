## API RESTful com Node.js

O Node.js é uma plataforma de desenvolvimento de software baseada em JavaScript. Ela permite que os desenvolvedores possam escrever aplicativos do lado do servidor usando a mesma linguagem de programação do lado do cliente.

Para implementar uma API RESTful com Node.js, é necessário seguir alguns passos básicos:

1. Instale o Node.js no seu sistema.
2. Crie um projeto Node.js usando o npm (Node Package Manager).
3. Instale os pacotes necessários para implementar a API RESTful, como o Express (um framework para construção de aplicativos web), o Body-parser (para análise de corpo de solicitação HTTP) e o CORS (para controle de acesso à API).
4. Defina o modelo conceitual de dados e o modelo de dados da API, usando ferramentas como o Sequelize (para bancos de dados SQL).
5. Defina as rotas da API, definindo os métodos HTTP e as operações em torno dos recursos.
6. Utilizar ferramentas como o Swagger para e documentar APIs de forma automatizada permitindo realizar  testes de solicitação HTTP.

O Node.js é uma opção viável para implementar APIs RESTful, pois ele fornece um conjunto de recursos e ferramentas para construir aplicativos escaláveis e de alta performance. Ele também é compatível com diferentes bancos de dados e provedores de serviços de nuvem, o que o torna uma opção popular para construção de sistemas distribuídos.

## Iniciando um projeto Node.js

Para criar um projeto de API RESTful em Node.js siga as seguintes etapas:

### 1 Instalando Node.js

Para seguir este guia, recomendamos que você utilize Ubuntu 20.04. Antes de começar, você deve ter uma conta de usuário com privilégios  de ´sudo´ configurados em seu sistema.

Para instalar o Node.js no Linux, siga os seguintes passos:

#### Passo 1: Abra o terminal

Abra o terminal no seu sistema Linux. O terminal pode ser encontrado no menu de aplicativos ou pressionando a tecla de atalho `Ctrl + Alt + T`.

#### Passo 2: Atualize o gerenciador de pacotes

Antes de instalar o Node.js, é recomendável atualizar o gerenciador de pacotes para garantir que você esteja baixando a versão mais recente. Use o seguinte comando no terminal:

```bash
sudo apt update
```

#### Passo 3: Instale o Node.js

Existem diferentes formas de instalar o Node.js no Linux, mas neste exemplo, usaremos o gerenciador de pacotes `apt` no Ubuntu ou no Debian. Use o seguinte comando para instalar o Node.js:

```bash
sudo apt install nodejs
```

Além disso, você também precisa instalar o gerenciador de pacotes npm (Node Package Manager), que é usado para instalar pacotes e bibliotecas JavaScript. Use o seguinte comando para instalar o npm:

```bash
sudo apt install npm
```

#### Passo 4: Verifique a instalação

Após a instalação do Node.js e npm, você pode verificar se tudo foi instalado corretamente executando o seguinte comando no terminal:

```bash
node -v
```

Este comando irá exibir a versão do Node.js instalada no seu sistema. Para verificar a versão do npm, use o seguinte comando:

```bash
npm -v
```

Instalar o Node.js no Linux é um processo simples e fácil, usando o gerenciador de pacotes `apt`. Certifique-se de atualizar o gerenciador de pacotes antes de instalar o Node.js e npm, e verifique se tudo foi instalado corretamente executando os comandos de verificação.

O Node.js é uma plataforma versátil que pode ser usada para desenvolver uma ampla gama de aplicativos, desde aplicativos web simples até aplicativos de rede complexos em tempo real. Ele é mantido pela Node.js Foundation, uma organização sem fins lucrativos que é responsável por coordenar o desenvolvimento, promover a adoção, fornecer suporte e garantir a estabilidade e a segurança da plataforma. Com sua arquitetura orientada a eventos e I/O assíncrono, o Node.js é capaz de lidar com muitas conexões simultâneas e escalonar facilmente para lidar com grandes cargas de trabalho.

### 2. Crie um projeto Node.js

#### Passo 1 Crie um diretório para o projeto e navegue até ele

```bash
mkdir projetos/nome-do-projeto #cria um diretório
cd projetos/nome-do-projeto ## move até o diretório
```

Lembre-se organizar seu ambiente de desenvolvimento é uma parte importante para garantir uma experiência de programação eficiente e produtiva, neste caso criamos um diretório `projetos` onde armazenaremos nossas aplicaçoes.

#### Passo 2 Inicialize o projeto Node.js com o npm

```bash
npm init -y
```

Isso irá criar um arquivo `package.json` no diretório do projeto, que contém informações sobre o projeto e suas dependências. O arquivo package.json é um arquivo em formato JSON que contém metadados sobre o projeto e suas dependências.

inicialmente o seu arquivo deve se parecer com isso:

```json
// package.json
{
  "name": "nome-do-projeto",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

Este arquivo é importante porque ele armazena informações sobre as dependências do projeto, scripts, configurações e outras informações importantes que serão utilizadas para gerenciar o projeto.

Aqui está outro exemplo de um arquivo `package.json` típico:

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

Essas são algumas das principais propriedades que podem ser encontradas em um arquivo `package.json`. Além dessas, existem outras propriedades que podem ser definidas, dependendo das necessidades do projeto.
Em resumo, o arquivo package.json é fundamental em projetos Node.js, pois ele ajuda a gerenciar dependências, configurar scripts e outras configurações importantes para o projeto.

Ao final desta etapa você terá a seguinte estrutura de diretório:

```tree
nome-do-projeto/
  |- package.json
```

- `nome-do-projeto/`: é o diretório raiz do projeto, que contém todos os arquivos e diretórios relacionados ao projeto.
- `package.json`: é um arquivo que descreve as informações do projeto, incluindo o nome do projeto, a versão do projeto, as dependências do projeto, as configurações de script, o autor, a licença e outras informações importantes. O arquivo é usado pelo npm para instalar as dependências do projeto e executar scripts relacionados ao projeto.

O npm tem um conjunto de comando uteis saiba mais na documentação do [npm](https://docs.npmjs.com/) ou utilize o comando `npm help npm`

### 3. Instale os Pacotes, Bibliotecas e Frameworks necessários

Embora os pacotes, bibliotecas e frameworks possam ter algumas semelhanças, eles são diferentes em sua finalidade e escopo, entenda melhor:

- **Pacote:** Um pacote é um conjunto de arquivos que podem ser facilmente compartilhados e reutilizados entre diferentes projetos em uma determinada linguagem de programação. Esses pacotes geralmente contêm módulos de código que fornecem funcionalidades específicas, como a manipulação de arquivos, a criação de servidores web, a integração com serviços externos e muito mais.

- **Biblioteca:** Uma biblioteca, por sua vez, é um conjunto de código pré-escrito que fornece funções ou classes reutilizáveis para realizar tarefas específicas em um projeto. Essas funções ou classes podem ser incorporadas diretamente no código do projeto em questão. As bibliotecas geralmente são projetadas para serem usadas em conjunto com outras bibliotecas ou com o código personalizado do projeto para fornecer uma solução completa.

- **Framework:** Já um framework é uma estrutura abrangente que fornece uma base para o desenvolvimento de software em geral. Ele inclui não apenas pacotes e bibliotecas, mas também convenções e padrões que orientam o processo de desenvolvimento. Os frameworks geralmente são voltados para a criação de um tipo específico de software, como aplicativos web, aplicativos móveis, jogos, etc

Os pacotes, bibliotecas e frameworks são gerenciados pelo sistema de gerenciamento de pacotes da linguagem de programação em questão (por exemplo, npm para Node.js, pip para Python) e podem ser instalados facilmente em um projeto com o comando apropriado.

#### Instale os pacotes necessários para criar uma API RESTful em Node.js

Há várias razões pelas quais é benéfico utilizar pacotes, bibliotecas e frameworks no desenvolvimento de software:

1. Reutilização de código: Os pacotes e frameworks já têm um código escrito e testado que pode ser reutilizado para adicionar funcionalidades ao seu projeto. Isso economiza tempo e esforço para o desenvolvedor.

2. Aumento da produtividade: Os pacotes e frameworks permitem que os desenvolvedores trabalhem mais rapidamente, uma vez que não precisam escrever o código do zero. Eles podem se concentrar em implementar a lógica de negócios específica do projeto.

3. Padronização: Os pacotes e frameworks fornecem padrões e convenções para o desenvolvimento, tornando o código mais consistente e fácil de entender para outros desenvolvedores.

4. Gerenciamento de dependências: Os pacotes e frameworks geralmente gerenciam suas próprias dependências, garantindo que todas as bibliotecas necessárias sejam instaladas corretamente e em suas versões adequadas.

5. Segurança: Os pacotes e frameworks são desenvolvidos e mantidos por uma comunidade de desenvolvedores, o que significa que eles são frequentemente revisados e atualizados para corrigir quaisquer problemas de segurança.

6. Suporte: Os pacotes e frameworks geralmente têm documentação detalhada e uma comunidade de desenvolvedores pronta para ajudar em caso de problemas.

Em resumo, o uso de pacotes e frameworks pode economizar tempo, aumentar a produtividade, garantir a qualidade do código e melhorar a segurança do software.

Existem diversos pacotes que podem ser utilizados para criar uma API RESTful em Node.js. Alguns dos mais populares incluem:

- **Express:** é um framework para Node.js que fornece recursos avançados para criar APIs RESTful e aplicativos web em geral, pode ser instalado através do `npm` com o comando:

  ```bash
  npm i express

  ```

- **Body-parser:** é um pacote que analisa o corpo das solicitações HTTP e extrai os dados enviados pelos clientes para o servidor em formato JSON ou URL-encoded, pode ser instalado através do `npm` com o comando:

  ```bash
  npm i body-parser 

  ```

- **Cors:** é um pacote que permite configurar as políticas de segurança do CORS (Cross-Origin Resource Sharing) para sua API.

  ```bash
  npm i cors 

  ```

Ao final desta etapa você terá a seguinte estrutura de diretório:

```tree
nome-do-projeto/
  |- node_modules/
  |- package-lock.json
  |- package.json

```

- `node_modules/`: é o diretório onde os pacotes de terceiros instalados pelo npm são armazenados.
- `package-lock.json`: é um arquivo gerado automaticamente pelo npm para garantir que as dependências do projeto sejam instaladas com a mesma versão, mesmo que o arquivo `package.json` tenha um caractere curinga `^` em suas dependências.

### 4. Modelo dados

O processo de modelagem de dados em desenvolvimento de uma API é indispensável, geralmente é dividido em várias etapas, que podem variar dependendo da metodologia de desenvolvimento de software adotada, podendo ter um time responsável somente por esses processos. Aqui está uma possível divisão desse processo em etapas:

1. **Análise de requisitos:** Nessa etapa, a equipe de desenvolvimento trabalha em conjunto com o cliente para entender as necessidades e objetivos do projeto. A equipe deve identificar as entidades e relações que farão parte do modelo de dados, bem como as regras de negócio que afetam o armazenamento e recuperação de informações.

2. **Modelo conceitual:** Com base na análise de requisitos, a equipe cria um modelo de dados conceitual, que descreve as entidades, atributos e relações que farão parte do modelo. Esse modelo geralmente é representado por meio de diagramas de entidade-relacionamento (ER), que mostram as entidades como caixas e as relações entre elas como linhas.

3. **Modelo lógico:** Nessa etapa, o modelo conceitual é refinado e transformado em um modelo de dados lógico, que representa como os dados serão armazenados em um banco de dados específico. O modelo lógico é projetado para atender aos requisitos de desempenho, segurança e integridade de dados, e geralmente é representado por meio de esquemas de tabelas e relacionamentos.

4. **Modelo físico:** Nessa etapa, o modelo de dados lógico é implementado em um banco de dados específico, levando em consideração as características físicas do hardware e do sistema de armazenamento. Isso inclui a escolha de índices, partições e outros recursos de otimização para maximizar a eficiência do acesso aos dados.

5. **Teste e validação:** Depois que o modelo de dados é implementado, a equipe realiza testes e validações para garantir que os dados sejam armazenados e recuperados corretamente. Isso inclui testes de integração, testes de desempenho e testes de segurança para garantir que o modelo de dados atenda aos requisitos do cliente e aos padrões de qualidade da empresa.

Essas etapas podem ser iterativas e podem ser realizadas em paralelo com outras etapas do processo de desenvolvimento de software, como design de interface de usuário, desenvolvimento de código e testes de unidade. A colaboração e comunicação efetiva entre os membros da equipe e as partes intereçadas são fundamentais para garantir que o modelo de dados atenda às necessidades do projeto e da empresa.

Entre essas etapas iremos destacar:

#### Modelo conceitual

Um modelo conceitual de dados pode ser representado de diversas formas, dependendo do contexto de uso e das necessidades da aplicação. por exemplo um diagrama entidade-relacionamento (ER) que descreve as entidades (tabelas), os atributos (colunas) e os relacionamentos entre essas entidades.Imagine uma aplicação de e-commerce que precisa armazenar informações sobre produtos, clientes e pedidos. Para cada uma dessas entidades, é necessário criar um modelo de dados que defina os campos e as relações com outras entidades. O modelo de dados para a entidade "produto", por exemplo, pode incluir campos como nome, descrição, preço e quantidade em estoque. Por exemplo, em uma aplicação de e-commerce, podemos ter as seguintes entidades:

- **Cliente**: representa um usuário que está navegando e comprando na loja online. Pode ter atributos como nome, e-mail e senha.
- **Produto**: representa um item que está à venda na loja online. Pode ter atributos como nome, descrição, preço e quantidade em estoque.
- **Categoria**: representa uma categoria na qual um produto pode ser classificado. Pode ter atributos como nome e descrição.
- **Endereço**: representa o endereço de um cliente. Pode ter atributos como rua, número, complemento, cidade, estado e CEP.
- **Pedido**: representa um pedido feito por um cliente. Pode ter atributos como data de criação, status e valor total.
- **Item_Pedido**: representa um item que foi adicionado a um pedido. Pode ter atributos como quantidade e valor unitário.
- **Pagamento**: representa um pagamento feito por um cliente para um pedido. Pode ter atributos como data de criação, valor e status.
- **Reembolso**: representa um reembolso que foi emitido para um cliente em relação a um pedido. Pode ter atributos como data de criação, valor e status.

Um diagrama ER simples para este modelo de dados seria:

```mermaid
erDiagram
    PRODUTO ||--|| CATEGORIA : pertence_a
    PRODUTO ||--|{ ITEM_PEDIDO : aparece_em
    CLIENTE ||--o{ ENDERECO : possui
    CLIENTE ||--o{ PEDIDO : faz
    PEDIDO ||--|{ ITEM_PEDIDO : contem
    PEDIDO ||--o{ PAGAMENTO : possui
    PAGAMENTO ||--o{ REEMBOLSO : tem
    PEDIDO ||--o{ REEMBOLSO : tem
```

Nesse diagrama, cada tabela é representada por um retângulo, e os relacionamentos entre as tabelas são indicados por linhas que conectam os retângulos. A cardinalidade do **relacionamento** é indicada por símbolos no final de cada linha.

Uma vez definido o modelo conceitual de dados, podemos utilizá-lo para criar o modelo de dados em Node.js que ira realizar operações no banco de dados, como inserir novos registros, atualizar informações existentes ou recuperar dados para exibir na interface do usuário. Isso é feito através de um ORM, que traduz as operações de banco de dados em chamadas a métodos do modelo correspondente.

#### Modelo lógico: e ORM Sequelize

Em resumo, um modelo lógico é uma representação mais detalhada do sistema, que utiliza uma linguagem formal para definir as entidades, atributos, relacionamentos e regras de negócio. Nessa etapa, o modelo conceitual é traduzido para o modelo lógico, que pode ser implementado em um banco de dados. O modelo lógico é independente de tecnologia, ou seja, pode ser implementado em diferentes sistemas gerenciadores de banco de dados.

#### ORM

ORM (Object-Relational Mapping) é uma técnica de programação que permite mapear objetos de um modelo lógico para uma tabela em um banco de dados relacional. Isso permite que o desenvolvedor trabalhe com objetos em vez de escrever diretamente SQL para interagir com o banco de dados.

O ORM fornece uma camada de abstração entre o código da aplicação e o banco de dados, permitindo que as consultas SQL sejam geradas automaticamente com base nas operações feitas nos objetos. Isso torna o desenvolvimento de aplicativos mais produtivo e reduz a complexidade de escrever e manter o código SQL.

Geralmente os ORMs têm a capacidade de realizar operações básicas de CRUD (criação, leitura, atualização e exclusão) em tabelas de banco de dados, bem como gerenciar as relações entre as tabelas. Alguns exemplos de ORMs populares incluem Sequelize para Node.js, Hibernate para Java e Entity Framework para .NET, SQLAlchemy para Python, entre outras.

Embora possam ter um impacto positivo no desenvolvimento de aplicativos, Os ORMs também têm algumas desvantagens. Por exemplo, pode ser menos eficiente do que o SQL direto, pois a geração de SQL pode adicionar camadas adicionais de abstração e, portanto, diminuir a velocidade de execução. Além disso, os ORMs podem ser menos flexíveis do que o SQL direto, pois a geração automática de SQL pode ser limitada em alguns casos específicos.

#### Sequelize

O Sequelize é um Object-Relational Mapping (ORM) para Node.js, que permite trabalhar com bancos de dados relacionais de forma mais fácil e produtiva. O Sequelize é uma ferramenta poderosa e fácil de usar, que oferece suporte a vários bancos de dados relacionais e recursos avançados, como migrações de banco de dados.Para utilizar o Sequelize em um projeto Node.js, é necessário instalá-lo através do NPM (Node Package Manager). Abaixo está o comando para instalar o `Sequelize`:

```bash
npm i sequelize
```

- O `sequelize` é um pacote que permite a realização de operações de banco de dados em um projeto Node.js, fornecendo uma interface simples e poderosa para interagir com bancos de dados relacionais. Ao utilizar o comando `npm i sequelize`, o pacote `sequelize` será instalado no diretório `node_modules` do projeto, e sua referência será adicionada ao arquivo `package.json`, na seção `dependencies`. A instalação do `sequelize` é necessária para que a aplicação possa utilizar as funcionalidades do ORM e interagir com o banco de dados de forma eficiente e segura.

```bash
npm i pg-hstore
```

- O `pg` é um pacote que fornece uma interface Node.js para interagir com o PostgreSQL. Ele permite que o Sequelize se conecte ao banco de dados e execute operações de leitura e gravação de dados de forma segura e eficiente.

- O `pg-hstore` é um pacote que permite a conversão de objetos JavaScript para a representação de texto hstore do PostgreSQL, que é usado para armazenar pares de chave-valor em uma coluna de banco de dados. Ele é necessário quando se deseja utilizar a funcionalidade hstore do PostgreSQL com o Sequelize.

A instalação desses pacotes é necessária para que a aplicação possa se conectar ao banco de dados PostgreSQL e realizar operações de leitura e gravação de dados de forma segura e eficiente, utilizando o Sequelize como ORM, para outros bancos consulte a documentção do [Sequelize](https://sequelize.org/docs/v6/getting-started/).

```bash
npm i sequelize-cli -D
```

- O `sequelize-cli` é uma ferramenta de linha de comando que facilita a criação de migrações de banco de dados, a geração de modelos e a criação de arquivos de configuração para o Sequelize. Ele é uma extensão do pacote `sequelize`, que é utilizado para realizar operações de banco de dados em um projeto Node.js. Ao utilizar o comando `npm i sequelize-cli -D`, o pacote `sequelize-cli` será instalado no diretório `node_modules` do projeto, e sua referência será adicionada ao arquivo `package.json`, na seção `devDependencies`. A opção `-D` indica que a dependência será instalada como uma dependência de desenvolvimento, ou seja, ela não será necessária para a execução da aplicação em produção, apenas para o desenvolvimento e testes.

Após a instalação, é necessário configurar a conexão com o banco de dados PostgreSQL. Para isso, iremos criar dois arquivos:

---

#### sequelizerc

- `.sequelizerc`: arquivo de configuração do Sequelize que permite personalizar o comportamento do CLI do Sequelize. Ele é usado para especificar diretórios e arquivos personalizados que podem ser usados pelo Sequelize para gerar código automaticamente, como arquivos de migração, modelos, seeders, etc.

O arquivo `.sequelizerc` é um arquivo no formato JavaScript (sem extenção .js) que pode exportar um objeto com as seguintes propriedades:

```javascript
const { resolve } = require("path");

module.exports = {
  config: resolve(__dirname, "src", "config", "database.js"),
  "models-path": resolve(__dirname, "src", "app", "models"),
  "migrations-path": resolve(__dirname, "src", "database", "migrations"),
  "seeders-path": resolve(__dirname, "src", "database", "seeds"),
};

```

Entenda melhor linha a linha do arquivo `.sequelizerc`:

```javascript
const { resolve } = require("path");
```

Esta linha está importando o método `resolve` do módulo `path` do Node.js. O método `resolve` é usado para resolver caminhos de arquivos e diretórios, garantindo que os caminhos sejam corretamente concatenados e formatados independentemente do sistema operacional.

```javascript
module.exports = {
```

Aqui estamos exportando um objeto que contém as configurações do Sequelize. Isso permite que outras partes do código possam acessar as configurações exportadas.

```javascript
  config: resolve(__dirname, "src", "config", "database.js"),
```

Definindo o caminho para o arquivo de configuração do Sequelize `src/config/database.js`.

```javascript
  "models-path": resolve(__dirname, "src", "app", "models"),
```

Caminho para o diretório que contém os modelos do Sequelize `src/app/models`.

```javascript
  "migrations-path": resolve(__dirname, "src", "database", "migrations"),
```

Definindo o caminho para o diretório que contém as migrações do Sequelize `src/database/migrations`.

```javascript
  "seeders-path": resolve(__dirname, "src", "database", "seeds"),
};
```

Por fim, aqui estamos definindo o caminho para o diretório que contém os seeders do Sequelize`src/database/seeds`.

Com essas configurações em `.sequelizerc`, o Sequelize será capaz de encontrar os arquivos necessários nos diretórios corretos para executar as operações de banco de dados.

---

#### database.js

`database.js` com as informações necessárias para a conexão, é uma boa prática em uma aplicação Node.js separar os os arquivos de código em diretorios, é comum encontrarmos um `src` e dentro um diretório de configuração `config`. Essa separação ajuda a manter o código organizado e facilita a manutenção, uma vez que as configurações estão centralizadas em um só lugar.

```javascript
// src/config/database.js
module.exports = {
  dialect: "postgres",
  host: "localhost",
  username: "postgres",
  password: "123",
  database: "node",
  define: {
    timestamp: true, // cria duas colunas: createdAt e updatedAt
    underscored: true,
    underscoredAll: true,
  },
};
```

- `dialect`: o tipo de banco de dados que você está usando, nesse caso PostgresSQL
- `host`: o nome ou endereço IP do servidor do banco de dados
- `username`: o nome de usuário usado para conectar-se ao banco de dados
- `password`: a senha associada ao usuário
- `database`: o nome do banco de dados que o aplicativo irá conectar
- `define`: um objeto de configuração para definir as opções de modelagem do Sequelize, um ORM (Object-Relational Mapping) do Node.js que é frequentemente usado com o PostgresSQL. As opções definidas nesse objeto são:
  - `timestamp`: cria duas colunas: `createdAt` e `updatedAt`, que registram a data e hora da criação e atualização de um registro.
  - `underscored`: define se os nomes das tabelas e colunas do banco de dados devem usar letras minúsculas e sublinhados (_) para separar palavras (por exemplo, `nome_da_tabela` em vez de `NomeDaTabela`).
  - `underscoredAll`: define se o mesmo padrão de nomenclatura deve ser aplicado aos nomes dos campos (colunas) dos modelos.

Essas configurações podem variar dependendo do banco de dados e do ORM que você está usando, mas em geral, um arquivo de configuração de banco de dados é usado para armazenar informações de conexão com o banco de dados e opções de configuração específicas do banco de dados e do ORM.

Ao final desta etapa você terá a seguinte estrutura de diretório:

```tree
nome-do-projeto/
├── src/
|   ├── config/
|   │   └── database.js
├── node_modules/
|   └── ... 
├── .sequelizerc
├── package-lock.json
└── package.json
```

- `src/`: diretório que contém o código fonte do projeto.

- `src/config/`: lembre-se este diretório que contém arquivos de configuração para o seu aplicativo, incluindo arquivos de configuração de banco de dados e outros parâmetros globais.

- `src/config/database.js`, que é responsável por definir as configurações de conexão com o banco de dados PostgreSQL, como nome do banco de dados, usuário, senha, host e porta.

#### Modelos e Migrações

No contexto de uma API Node.js com Sequelize, modelos e migrações são conceitos relacionados à definição e manipulação de dados no banco de dados.

- **Modelos**: são **classes** que definem a estrutura dos dados que serão **manipulados** pelo aplicativo. Eles são tipicamente definidos com a ajuda do Sequelize, um ORM (Object-Relational Mapping) que fornece uma interface para mapear objetos JavaScript para tabelas de banco de dados relacionais. Os modelos do Sequelize geralmente contêm propriedades que correspondem às colunas da tabela do banco de dados, bem como métodos que permitem criar, ler, atualizar e excluir (CRUD) registros do banco de dados.

- **Migrações**: são arquivos de script que **definem a estrutura da tabela** do banco de dados e as alterações na estrutura da tabela ao longo do tempo. As migrações são normalmente criadas usando uma biblioteca de migração, como o `Sequelize CLI` (Command-Line Interface). As migrações podem ser usadas para criar e alterar tabelas, colunas, índices e chaves estrangeiras. Elas garantem que a estrutura do banco de dados corresponda à estrutura definida pelo modelo do aplicativo.

Na maioria das vezes, é recomendável criar os modelos primeiro e, em seguida, criar as migrações que definem a estrutura da tabela do banco de dados.

Ao criar os modelos primeiro, você pode definir a estrutura de dados que será usada em seu aplicativo e usar esses modelos para gerar as migrações. Isso ajuda a garantir que a estrutura da tabela do banco de dados corresponda à estrutura de dados esperada pelo aplicativo. Além disso, a criação de modelos primeiro permite que você teste e depure sua lógica de negócios sem se preocupar com a estrutura do banco de dados subjacente.

Depois de criar os modelos, você pode usar ferramentas como o Sequelize CLI para gerar automaticamente as migrações com base nesses modelos. As migrações geradas fornecem um ponto de partida sólido para definir a estrutura da tabela do banco de dados e podem ser personalizadas conforme necessário para atender às necessidades específicas do seu aplicativo.

Após a configuração da conexão com o banco de dados, podemos criar modelos para as tabelas que serão utilizadas na aplicação. Os modelos são definidos utilizando o Sequelize e representam as tabelas do banco de dados.

Uma boa prática é salvar os modelos de banco de dados em um diretório chamado `src/models`. Isso ajuda a manter uma estrutura organizada do projeto, facilita a localização dos arquivos e ajuda a evitar confusão com outros tipos de arquivos, como rotas ou controladores.

Ao salvar os modelos em um diretório separado, é possível também criar subdiretórios para organizar os modelos por categoria, se for necessário. Por exemplo, é possível ter um diretório `models/produtos/` para todos os modelos relacionados a produtos ou a um determinado subgrupo, más tenha cuidado para não se perder, mantenha o seu código o mais organizado possível, e lembre-se que outros desenvolvedores podem dar continuidade ao seu projeto.

Com base no modelo conceitual de dados, podemos começar a criar o modelo de dados usando o Sequelize.

Para cada entidade, precisamos criar um `ORM` correspondente no nosso diretorio `src/models`. Vamos criar um arquivo separado para cada modelo, seguindo o padrão de nomenclatura  do Sequelize.

O Sequelize segue um padrão de nomenclatura para a criação de modelos, tabelas e colunas no banco de dados, e geralmente segue as seguintes convenções:

- Os nomes das tabelas no banco de dados devem ser no plural e em letras minúsculas, underscore (`_`) para separar as palavras  (exemplo: `usuarios`, `itens_pedidos`).
- Os nomes das colunas no banco de dados devem ser em letras minúsculas e separados por underscore `_` (exemplo: `primeiro_nome`, `ultimo_nome`).
- Os nomes dos modelos no Sequelize devem seguir o padrão de nomenclatura "PascalCase". Isso significa que o nome do modelo deve ter a primeira letra de cada palavra em maiúscula, sem espaços ou caracteres especiais, (exemplo: `Usuario`, `ItemPedido`,).
- As propriedades dos modelos no Sequelize devem seguir o mesmo padrão de nomenclatura das colunas no banco de dados (exemplo: `firstName`, `lastName`, `createdAt`).

Essas convenções ajudam a manter a consistência e a legibilidade do código ao trabalhar com o Sequelize. No entanto, é possível personalizar o padrão de nomenclatura do Sequelize usando as configurações do modelo e do Sequelize.

Começaremos criando O Modelo "Clientes" com os seguintes campos: **nome**, **emal** e **senha**. O arquivo de modelo para Clientes deve ficar assim:

```javascript
// src/models/Clientes.js

// Importa as classes Sequelize e Model do pacote Sequelize
const { Sequelize, Model } = require('sequelize');

// Define a classe Clientes, que estende a classe Model
class Clientes extends Model {

  // Define o método init, que é chamado para inicializar a classe com as colunas da tabela do banco de dados
  static init(sequelize) {
    // Chama o construtor da classe Model para definir as colunas da tabela
    super.init(
      {
        nome: Sequelize.STRING, // Coluna "nome" do tipo STRING
        email: Sequelize.STRING, // Coluna "email" do tipo STRING
        senha: Sequelize.STRING, // Coluna "senha" do tipo STRING
      },
      {
        sequelize, // Objeto de conexão com o banco de dados
      }
    );
  }
  // Define o método associate, que é chamado para definir as associações entre as tabelas do banco de dados
  static associate(models) {
    // Define a associação "hasMany" entre a tabela Clientes e a tabela Enderecos
    // Isso significa que um cliente pode ter vários endereços
    this.hasMany(models.Enderecos);
  }
}
// Exporta a classe Clientes para uso em outros módulos
module.exports = Clientes;

```

```javascript
// src/models/Clientes.js

// Importa as classes Sequelize e Model do pacote Sequelize
const { Sequelize, Model } = require('sequelize');

// Define a classe Enderecos, que estende a classe Model
class Enderecos extends Model {

  // Define o método init, que é chamado para inicializar a classe com as colunas da tabela do banco de dados
  static init(sequelize) {
    // Chama o construtor da classe Model para definir as colunas da tabela
    super.init(
      {
        cep: Sequelize.STRING, // Coluna "cep" do tipo STRING
        logradouro: Sequelize.STRING, // Coluna "logradouro" do tipo STRING
        complemento: Sequelize.STRING, // Coluna "complemento" do tipo STRING
        bairro: Sequelize.STRING, // Coluna "bairro" do tipo STRING
        localidade: Sequelize.STRING, // Coluna "localidade" do tipo STRING
        uf: Sequelize.STRING, // Coluna "uf" do tipo STRING
        cliente_id:  Sequelize.INTEGER // Coluna "cliente_id" do tipo INTEGER, que armazena a chave estrangeira da tabela Clientes
      },
      {
        sequelize, // Objeto de conexão com o banco de dados
      }
    );
  }

  // Define o método associate, que é chamado para definir as associações entre as tabelas do banco de dados
  static associate(models) {
    // Define a associação "belongsTo" entre a tabela Enderecos e a tabela Clientes
    // Isso significa que um endereço pertence a um cliente
    this.belongsTo(models.Clientes, { foreignKey: "cliente_id" }); // Define a chave estrangeira da tabela Clientes
  }
}

// Exporta a classe Enderecos para uso em outros módulos
module.exports = Enderecos;
```

Podemos criar os modelos restantes seguindo o mesmo padrão, ao final desta etapa vc tera a seguinte estrutura de diretorio:

```tree
nome-do-projeto/
├── src/
|   ├── config/
|   │   └── database.js
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

Agora podemos construir as **migrations**, podemos criar um diretorio `database/migratios`, que ja referenciamos no `.sequelizerc` na linha `migrations-path`, apos a criação dos diretorio podemos utilizar o **sequelize-cli** para gerar um migration:

Para gerar uma migração usando o Sequelize CLI, você pode usar o comando `sequelize migration:generate`, seguido pelo nome da migração que você deseja criar. Por exemplo:

```bash
sequelize migration:generate --name create_clientes

```

O comando acima irá gerar um novo arquivo de migração com o nome composto pela `data da migraçao` e o nome `create_clientes`. Dentro do arquivo gerado, você pode definir as operações que serão executadas na tabela do banco de dados, como criar uma nova tabela, adicionar ou remover colunas, entre outras, no exemplo abaixo iremos criar a tabela cliente:

```javaScript
// src/database/migrations/{numero-migration}-create_clientes.js
// Exporta um objeto com os métodos up e down
module.exports = {
  // Método up é responsável por criar a tabela "clientes"
  up: (queryInterface, Sequelize) => {
    // Utiliza o objeto queryInterface para criar a tabela "clientes"
    return queryInterface.createTable("clientes", {
      // Coluna "id", do tipo INTEGER, não pode ser nula, é auto-incremental e chave primária
      id: {
        type: Sequelize.INTEGER,
        allowNull: false,
        autoIncrement: true,
        primaryKey: true,
      },
      // Coluna "nome", do tipo STRING, não pode ser nula
      nome: {
        type: Sequelize.STRING,
        allowNull: false,
      },
      // Coluna "email", do tipo STRING, não pode ser nula e é única (não permite repetições)
      email: {
        type: Sequelize.STRING,
        allowNull: false,
        unique: true,
      },
      // Coluna "senha", do tipo STRING, não pode ser nula
      senha: {
        type: Sequelize.STRING,
        allowNull: false,
      },
      // Coluna "created_at", do tipo DATE, não pode ser nula
      created_at: {
        type: Sequelize.DATE,
        allowNull: false,
      },
      // Coluna "updated_at", do tipo DATE, não pode ser nula
      updated_at: {
        type: Sequelize.DATE,
        allowNull: false,
      },
    });
  },

  // Método down é responsável por remover a tabela "clientes"
  down: (queryInterface) => {
    // Utiliza o objeto queryInterface para remover a tabela "clientes"
    return queryInterface.dropTable("clientes");
  },
};

```

aplicando a migração:

```bash
sequelize db:migrate

```

Depois de definir as operações, você pode executar a migração usando o comando `sequelize db:migrate`. Isso irá aplicar as alterações no banco de dados.

para gerar a migraçao do models `Enderecos` o processo e bem parecido:

```bash
sequelize migration:generate --name create_enderecos

```

Novamente  irá gerar um novo arquivo de migração com o nome composto pela `data da migraçao` e o nome `create_enderecos`. Dentro do arquivo gerado, defina a estrutura da `migrations` **Enderecos**:

```javaScript
// // src/database/migrations/{data}-create_enderecos.js
module.exports = {
  // Método up é responsável por criar a tabela "enderecos"
  up: (queryInterface, Sequelize) => {
    // Utiliza o objeto queryInterface para criar a tabela "enderecos"
    return queryInterface.createTable("enderecos", {
      id: {
        type: Sequelize.INTEGER,
        allowNull: false,
        autoIncrement: true,
        primaryKey: true,
      },
      cep: {
        type: Sequelize.STRING,
        allowNull: true,
      },
      logradouro: {
        type: Sequelize.STRING,
        allowNull: true,
      },
      complemento: {
        type: Sequelize.STRING,
        allowNull: true,
      },
      bairro: {
        type: Sequelize.STRING,
        allowNull: true,
      },
      localidade: {
        type: Sequelize.STRING,
        allowNull: true,
      },
      uf: {
        type: Sequelize.STRING,
        allowNull: true,
      },
      created_at: {
        type: Sequelize.DATE,
        allowNull: false,
      },
      updated_at: {
        type: Sequelize.DATE,
        allowNull: false,
      },
      cliente_id: { // coluna referenciando o id da tabela clientes
        type: Sequelize.INTEGER,
        references: { model: "clientes", key: "id" }, // faz referência à tabela clientes
        onUpdate: "CASCADE", // quando o id do cliente for atualizado, atualiza também na tabela de endereços
        onDelete: "CASCADE", // quando um cliente for deletado, deleta também todos os seus endereços
        allowNull: false, // não permite valores nulos para essa coluna
      },
    });
  },

  down: queryInterface => {
    return queryInterface.dropTable("enderecos"); // remove a tabela de endereços
  },
};
```

nao esqueça de aplicar a migração:

```bash
sequelize db:migrate

```

Além disso, você pode usar opções adicionais com o comando `sequelize migration:generate`, como `--help` para ver a lista completa de opções disponíveis.

segue alguns comandos uteis do sequelize-cli:

| Comando                                            | Descrição                                                             |
| -------------------------------------------------- | --------------------------------------------------------------------- |
| `sequelize init`                                   | Inicia um novo projeto do sequelize-cli no diretório atual            |
| `sequelize model:generate --name User --attributes` | Gera um novo modelo de usuário com atributos especificados            |
| `sequelize db:create`                              | Cria um novo banco de dados com base nas configurações do sequelize    |
| `sequelize db:migrate`                             | Executa as migrações de banco de dados pendentes                       |
| `sequelize db:seed:all`                            | Executa todos os arquivos de sementes disponíveis                      |
| `sequelize db:drop`                                | Elimina todas as tabelas do banco de dados configurado                 |
| `sequelize migration:create`                       | Cria um novo arquivo de migração vazio                                  |
| `sequelize migration:run`                          | Executa todas as migrações de banco de dados pendentes                  |
| `sequelize migration:undo`                         | Reverte a migração mais recente                                          |
| `sequelize seed:generate --name User`              | Gera um novo arquivo de semente para a tabela de usuários especificada |


```javascript
// models/index.js
const Sequelize = require('sequelize');
const sequelize = new Sequelize('nome_do_banco', 'usuário', 'senha', {
  host: 'localhost',
  dialect: 'postgres'
});

const models = {
  Produto: sequelize.import('./Produto'),
  Categoria: sequelize.import('./Categoria'),
  Cliente: sequelize.import('./Cliente'),
  Endereco: sequelize.import('./Endereco'),
  Pedido: sequelize.import('./Pedido'),
  ItemPedido: sequelize.import('./ItemPedido'),
  Pagamento: sequelize.import('./Pagamento'),
  Reembolso: sequelize.import('./Reembolso'),
};

Object.keys(models).forEach((modelName) => {
  if ('associate' in models[modelName]) {
    models[modelName].associate(models);
  }
});

models.sequelize = sequelize;
models.Sequelize = Sequelize;

module.exports = models;
```

Nesse exemplo, o arquivo "index.js" importa todos os modelos e define as associações entre eles. Ao final, o arquivo exporta um objeto com todos os modelos e as instâncias do Sequelize.

Com as tabelas criadas no banco de dados, podemos utilizar o Sequelize para realizar operações de inserção, alteração e remoção de registros. Para isso, podemos utilizar os métodos `create`, `update

### 5. Defina as rotas da API

#### Passo 1 Crie um arquivo `index.js` no diretório do projeto e configure o servidor express

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

Importando o módulo `express` para o nosso código. O `express` é um framework para criação de aplicações web em Node.js. A palavra-chave `const` é utilizada para declarar uma constante.

```js
const bodyParser = require('body-parser');
```

Importando o módulo `body-parser` que é um middleware para análise do corpo das requisições HTTP.

```js
const cors = require('cors');
```

Importando o módulo `cors` que é um middleware que permite o acesso de outras origens à API.

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

Utilizamos os middlewares `cors` e `body-parser` que importamos anteriormente para nossa aplicação express. O `cors` habilita o acesso de outras origens à API e o `body-parser` analisa o corpo das requisições HTTP.

```js
app.get('/', (req, res) => {
  res.send('Bem-vindo à API RESTful');
});
```

Definindo uma rota para a raiz da nossa aplicação (`/`). Quando um usuário acessar essa rota, a API enviará como resposta uma mensagem de boas-vindas.

```js
app.listen(port, () => {
  console.log(`Servidor iniciado em http://localhost:${port}`);
});
```

Finalmente, aqui estamos iniciando o servidor express na porta definida anteriormente e imprimindo uma mensagem de sucesso no console.

#### Passo 2 Teste o servidor

Para rodar o codigo criado em `index.js` execute o seguinte comando:

```bash
node index.js
```

Isso iniciará o servidor na porta 3000. Abra um navegador e acesse `http://localhost:3000`. Você deve ver a mensagem "Bem-vindo à API RESTful".

A partir daqui, você pode começar a criar as rotas da API RESTful, definindo as operações HTTP, os **parametros** e as respostas esperadas. O express facilita muito a criação de rotas e manipulação de requisições e respostas HTTP. Com as rotas definidas, você pode criar a lógica de negócios da aplicação, que pode incluir acesso a banco de dados, autenticação e autorização, validação de dados, entre outros.

#### Parâmetros

Parâmetros de rotas, ou route parameters, são uma forma de passar informações dinâmicas para a sua aplicação através da URL. Eles são utilizados para identificar um recurso específico, como um usuário ou um produto, ou para passar  informações adicionais para a nossa aplicação. Podemos dividir os parâmetros em:

##### Parâmetros de rota

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

##### Parâmetros de Query String

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
