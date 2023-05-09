## Router Guards

Os Router Guards são mecanismos utilizados para garantir que o acesso a determinadas rotas em uma aplicação ocorra apenas quando certas condições são satisfeitas. Essas condições podem incluir a autenticação do usuário, nível de acesso, permissões, entre outros.

No React, é possível implementar Router Guards por meio de bibliotecas de roteamento, como o React Router. Essas bibliotecas fornecem mecanismos para definir funções de validação que serão executadas antes de renderizar uma determinada rota. Se a validação não for bem-sucedida, a rota não será renderizada e o usuário será redirecionado para outra página.

```javascript
  import { BrowserRouter, Routes, Route, Navigate } from 'react-router-dom';

  function App() {
    const isAuthenticated = false;

    function PrivateRoute({ element: Component, ...rest }) {
      return (
        <Route
          {...rest}
          element={isAuthenticated ? (
            <Component />
          ) : (
            <Navigate to="/login" replace />
          )}
        />
      );
    }

    return (
      <BrowserRouter>
        <Routes>
          <Route path="/login" element={<LoginPage />} />
          <PrivateRoute path="/" element={<HomePage />} />
        </Routes>
      </BrowserRouter>
    );
  }
```

Neste exemplo, definimos a função PrivateRoute que recebe o componente que deve ser renderizado como elemento (element) e outras propriedades para a rota. Dentro desta função, usamos o elemento ternário para validar se o usuário está autenticado.

Se o usuário estiver autenticado, o componente filho é renderizado. Caso contrário, o usuário é redirecionado para a página de login usando o elemento Navigate com a propriedade to definida para "/login" e a propriedade replace definida como true.

Em seguida, usamos a função PrivateRoute para renderizar a página inicial (`<HomePage />`) somente se o usuário estiver autenticado. Se o usuário não estiver autenticado, ele será redirecionado para a página de login.
