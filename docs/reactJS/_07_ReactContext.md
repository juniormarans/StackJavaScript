## React Context

React Context é um recurso do React que permite o compartilhamento de dados entre componentes em uma árvore de componentes, sem a necessidade de passar props manualmente em cada nível da árvore. Isso pode melhorar significativamente a eficiência e a escalabilidade do aplicativo, permitindo que os dados sejam acessados e atualizados facilmente em qualquer parte da árvore.

O React Context é composto por um objeto Provider e um objeto Consumer. O Provider é responsável por fornecer o contexto aos componentes filhos, enquanto o Consumer é responsável por consumir os dados do contexto.

Por exemplo, imagine uma aplicação em que diferentes componentes precisam acessar informações do usuário, como o nome e o endereço. Em vez de passar essas informações manualmente para cada componente, pode-se usar o React Context para fornecer acesso a esses dados em toda a árvore de componentes.

Para criar um contexto no React, é possível utilizar a função createContext(). Esta função retorna um objeto com dois elementos: Provider e Consumer. O Provider é utilizado para prover o contexto para os componentes filhos, enquanto o Consumer é utilizado para consumir os dados do contexto.

```javascript
  import React, { createContext, useState } from 'react';

  // Criando um contexto com informações de usuário
  export const UserContext = createContext();

  const App = () => {
    const [user, setUser] = useState({
      name: 'John Doe',
      address: '123 Main Street'
    });

    // Utilizando o Provider para prover o contexto para os componentes filhos
    return (
      <UserContext.Provider value={user}>
        <div>
          <Component1 />
          <Component2 />
        </div>
      </UserContext.Provider>
    );
  };

  // Utilizando o Consumer para consumir os dados do contexto
  const Component1 = () => {
    return (
      <UserContext.Consumer>
        {user => (
          <div>
            <p>{user.name}</p>
            <p>{user.address}</p>
          </div>
        )}
      </UserContext.Consumer>
    );
  };

  const Component2 = () => {
    return (
      <UserContext.Consumer>
        {user => (
          <div>
            <p>{user.name}</p>
            <p>{user.address}</p>
          </div>
        )}
      </UserContext.Consumer>
    );
  };
```

Nesse exemplo, a função createContext() é utilizada para criar um contexto chamado UserContext, que contém informações de usuário. Essas informações são fornecidas pelo componente App, que utiliza o Provider para prover o contexto para os componentes filhos Component1 e Component2. Esses componentes, por sua vez, utilizam o Consumer para consumir os dados do contexto e exibir as informações do usuário.
