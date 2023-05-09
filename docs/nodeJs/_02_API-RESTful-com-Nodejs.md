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

