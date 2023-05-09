## React Router Dom

O React Router DOM é uma biblioteca JavaScript utilizada para criar aplicativos de página única (SPA) com rotas dinâmicas. Ele é baseado na biblioteca React e oferece um conjunto de componentes para gerenciar a navegação de uma aplicação web.

Os componentes principais do React Router DOM são o BrowserRouter, Routes, Route e Link. O BrowserRouter é responsável por fornecer o contexto para os componentes de roteamento e deve ser envolvido em torno de todo o aplicativo. O Routes é utilizado para encapsular componentes Route. O Route é utilizado para definir uma rota específica e renderizar um componente correspondente a essa rota. Já o Link é utilizado para criar links clicáveis que levam a uma rota específica.

Inicie um novo projeto, abra o arquivo app.js, substitua o conteúdo e execute.

```javascript
// src/App.js

  import { BrowserRouter, Routes, Route, Link } from 'react-router-dom';
  import './App.css';

  function App() {
    return (
      <BrowserRouter>
        <Routes>
          <Route exact path="/" element={<FirstPage />} />       
          <Route path="/next" element={<SecondPage />} />         
        </Routes>
      </BrowserRouter>
    );
  }

  function FirstPage() {
    return (
      <div>
        <p>Primeira Página</p>
        <button type='button'>
          <Link to='/next'>
            Próxima Página
          </Link>
        </button>
      </div>
    )
  }

  function SecondPage() {
    return (
      <div>
        <p>Segunda Página</p>
        <button type='button'>
          <Link to='/'>
            Página Anterior
          </Link>
        </button>
      </div>
    )
  }

  export default App;
```

Para executar abra o terminal:

```bash
  npm start
```

Para tornar o código mais escalável, quebra-se a o código acima, separando as páginas em arquivos de páginas e a configuração das rotas em um arquivo separado. Além de criar uma pasta para os estilos.

```tree
my-app/
  ├── node_modules/
  ├── public/
  │   ├── index.html
  │   ├── favicon.ico
  │   └── manifest.json
  ├── src/
  │   ├── pages
  │   │   ├── firstPage.js
  │   │   └── secondPage.js
  │   ├── styles
  │   │   ├── App.css
  │   │   └── index.css
  │   ├── App.js
  │   ├── index.js
  │   ├── reportWebVitals.js
  │   ├── router.js
  │   ├── setupTests.js
  ├── .gitignore
  ├── package-lock.json
  ├── package.json
  └── README.md
```

```javascript
// src/index.js

  import React from 'react';
  import ReactDOM from 'react-dom/client';
  import App from './App';
  import reportWebVitals from './reportWebVitals';

  const root = ReactDOM.createRoot(document.getElementById('root'));
  root.render(
    <React.StrictMode>
      <App />
    </React.StrictMode>
  );

  // If you want to start measuring performance in your app, pass a function
  // to log results (for example: reportWebVitals(console.log))
  // or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
  reportWebVitals();
```

```javascript
// src/pages/firstPage.js

  import {Link} from 'react-router-dom'

  function FirstPage() {
    return (
      <div>
        <p>Primeira Página</p>
        <button type='button'>
          <Link to='/next'>
            Próxima Página
          </Link>
        </button>
      </div>
    )
  }

  export default FirstPage
```

`import {Link} from 'react-router-dom'`: Importa o componente Link do pacote react-router-dom. O Link é um componente usado para criar links em um aplicativo React.
`function FirstPage() { ... }`: Define o componente FirstPage como uma função que retorna um elemento JSX. O componente é definido aqui como uma função, mas também poderia ser definido como uma classe.
`<div> ... </div>`: Cria um elemento div que contém o restante do conteúdo da página.
`<p>Primeira Página</p>`: Cria um elemento p que contém o texto "Primeira Página".
`<button type='button'> ... </button>`: Cria um botão que contém o link para a próxima página. O atributo type='button' define o tipo do botão como um botão normal, para evitar que a página seja recarregada quando o botão é clicado.
`<Link to='/next'> ... </Link>`: Cria um componente Link com o texto "Próxima Página" e um atributo ##to## que especifica a rota da próxima página (/next).
`export default FirstPage`: Exporta o componente FirstPage como o componente padrão deste módulo. Isso permite que ele seja importado em outros arquivos do aplicativo usando `import FirstPage from './firstPage'`.

```javascript
// src/pages/secondPage.js

  import {Link} from 'react-router-dom'

  function SecondPage() {
    return (
      <div>
        <p>Segunda Página</p>
        <button type='button'>
          <Link to='/'>
            Página Anterior
          </Link>
        </button>
      </div>
    )
  }

  export default SecondPage
```

`import {Link} from 'react-router-dom'`: Importa o componente Link do pacote react-router-dom. O Link é um componente usado para criar links em um aplicativo React.
`function SecondPage() { ... }`: Define o componente SecondPage como uma função que retorna um elemento JSX. O componente é definido aqui como uma função, mas também poderia ser definido como uma classe.
`<div> ... </div>`: Cria um elemento div que contém o restante do conteúdo da página.
`<p>Primeira Página</p>`: Cria um elemento p que contém o texto "Página Anterior".
`<button type='button'> ... </button>`: Cria um botão que contém o link para a página anterior. O atributo type='button' define o tipo do botão como um botão normal, para evitar que a página seja recarregada quando o botão é clicado.
`<Link to='/next'> ... </Link>`: Cria um componente Link com o texto "Página Anterior" e um atributo ##to## que especifica a rota da Página Anterior (/).
`export default FirstPage`: Exporta o componente FirstPage como o componente padrão deste módulo. Isso permite que ele seja importado em outros arquivos do aplicativo usando `import SecondPage from './secondPage'`.

```javascript
// src/router.js

  import { BrowserRouter, Routes, Route } from 'react-router-dom';

  import FirstPage from './pages/firstPage'
  import SecondPage from './pages/secondPage'

  function Router() {
    return (
      <BrowserRouter>
        <Routes>
          <Route exact path="/" element={<FirstPage />} />       
          <Route path="/next" element={<SecondPage />} />         
        </Routes>
      </BrowserRouter>
    );
  }

  export default Router
```

`import { BrowserRouter, Routes, Route } from 'react-router-dom';`: Importa os componentes necessários do pacote react-router-dom. O BrowserRouter é um componente que envolve o aplicativo e fornece a funcionalidade de roteamento. O Routes é um componente que contém as rotas do aplicativo e o Route é um componente que define uma rota em si.
`import FirstPage from './pages/firstPage'`: Importa o componente FirstPage do arquivo firstPage.js, que contém o código para a primeira página do aplicativo.
`import SecondPage from './pages/secondPage'`: Importa o componente SecondPage do arquivo secondPage.js, que contém o código para a segunda página do aplicativo.
`function Router() { ... }`: Define a função Router como um componente que retorna os elementos JSX que definem as rotas do aplicativo.
`<BrowserRouter> ... </BrowserRouter>`: Envolve o aplicativo com o componente BrowserRouter para fornecer a funcionalidade de roteamento.
`<Routes> ... </Routes>`: Define o elemento Routes, que contém todas as rotas do aplicativo.
`<Route exact path="/" element={<FirstPage />} />`: Define uma rota para a página inicial (/) do aplicativo, que renderiza o componente FirstPage. O atributo exact garante que apenas a rota exata é correspondida. O atributo path define o caminho da rota.
`<Route path="/next" element={<SecondPage />} />`: Define uma rota para a página seguinte (/next) do aplicativo, que renderiza o componente SecondPage. O atributo path define o caminho da rota.
export default Router: Exporta o componente Router como o componente padrão deste módulo. Isso permite que ele seja importado em outros arquivos do aplicativo usando `import Router from './Router'`.

```javascript
// src/App.js

  import Router from './router'

  function App() {
    return (
      <Router />
    );
  }

  export default App;
```

`import Router from './router'`: Importa o componente Router do arquivo router.js para definir as rotas do aplicativo.
`function App() { ... }`: Define a função App como um componente que retorna os elementos JSX que compõem o aplicativo.
`<Router />`: Renderiza o componente Router definido no arquivo router.js, que contém as rotas do aplicativo.
`export default App;`: Exporta o componente App como o componente padrão deste módulo. Isso permite que ele seja importado em outros arquivos do aplicativo usando `import App from './App'`.
