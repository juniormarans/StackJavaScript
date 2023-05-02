## Iniciando um projeto com ReactJS

Iniciar um projeto no React JS requer a instalação e configuração adequadas de ferramentas e bibliotecas. Para iniciar um projeto no React JS, siga o passo a passo:

1. Instale o Node.js: O React JS é uma biblioteca baseada no Node.js, por isso, é necessário instalá-lo em seu sistema antes de iniciar um novo projeto React. Você pode fazer o download da versão mais recente do [Node.js](https://nodejs.org/) no site oficial e instalar seguindo as instruções.

2. Crie um novo projeto.

```bash
  npx create-react-app nome-do-seu-projeto
```

3. Execute o projeto: Depois de criar o projeto, navegue para o diretório do projeto no terminal.

```bash
  npm start
```

O servidor será iniciado em `http://localhost:3000` e qualquer alteração que você fizer no código será refletida automaticamente no navegador.

### Selecione template

Ao iniciar um novo projeto em React, você pode usar o parâmetro `--template` para especificar um modelo personalizado para ser usado como ponto de partida. Isso pode ser útil se você já tem um modelo personalizado criado ou se deseja usar um modelo diferente do padrão fornecido pelo Create React App.

```bash
  npx create-react-app my-app --template [nome do template]
```

O Create React App inclui vários modelos diferentes que você pode usar, como cra-template-typescript, cra-template-redux, cra-template-redux-typescript, entre outros.

Se desejar usar um modelo personalizado que não está incluído no Create React App, pode especificar a URL do repositório Git do modelo em vez do nome do modelo.

```bash
  npx create-react-app my-app --template git+https://github.com/[username]/[reponame].git
```

Isso clonará o repositório Git do modelo e usará os arquivos como ponto de partida para o seu projeto React.

Depois de iniciar o projeto com o modelo personalizado, você pode modificar o código e os arquivos do modelo para atender às suas necessidades específicas.
