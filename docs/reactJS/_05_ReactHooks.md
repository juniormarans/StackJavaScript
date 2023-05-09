## React Hooks

React Hooks é uma adição importante ao React 16.8 que permite que você use recursos de estado e ciclo de vida em componentes funcionais. Até a versão 16.7 do React, os componentes funcionais eram limitados a receber propriedades e renderizar elementos na tela.

Com o uso de hooks, os componentes funcionais agora podem ter acesso a recursos de estado, ciclo de vida e outras funcionalidades anteriormente disponíveis apenas em componentes de classe. Isso significa que você pode escrever componentes mais simples e fáceis de entender, sem precisar escrever código redundante.

Os hooks são funções que permitem que você "se enganche" em certos recursos do React, como estado, efeitos colaterais, referências e contexto, e os utilize em seus componentes funcionais. Existem alguns hooks básicos fornecidos pelo React, como useState, useEffect e useContext, mas você também pode criar seus próprios hooks personalizados para compartilhar a lógica entre seus componentes.

Os hooks permitem que você compartilhe lógica entre componentes sem a necessidade de criar um componente de classe ou usar render props. Isso torna o código mais fácil de ler, manter e reutilizar. Além disso, os hooks ajudam a simplificar a lógica de negócios do componente, evitando que ela seja distribuída por toda a árvore de componentes.

### useState

O useState é um dos hooks básicos do React que permite adicionar estado a um componente funcional. De forma científica, podemos dizer que o useState é um método utilizado para gerenciamento de estados dentro de um componente funcional React, permitindo que o mesmo reaja a mudanças de estado e renderize novamente com base nessas mudanças.

O useState recebe um valor inicial como argumento e retorna um array contendo o valor atual do estado e uma função para atualizar o valor. Essa função de atualização é usada para modificar o valor do estado e atualizar o componente.

Um exemplo de uso do useState seria para criar um contador em um componente funcional. 

```javascript
  import React, { useState } from 'react';

  function Contador() {
    const [contador, setContador] = useState(0);

    function incrementar() {
      setContador(contador + 1);
    }

    return (
      <div>
        <h2>Contador: {contador}</h2>
        <button onClick={incrementar}>Incrementar</button>
      </div>
    );
  }
```

Nesse exemplo, a função useState é utilizada para criar uma variável de estado "contador" com valor inicial 0. Em seguida, é criada uma função "incrementar" que atualiza o estado "contador" com o valor atual mais 1. Essa função é chamada quando o botão "Incrementar" é clicado.

Ao clicar no botão, o estado "contador" é atualizado e o componente é renderizado novamente, exibindo o novo valor do contador.

É importante lembrar que o useState deve ser utilizado apenas em componentes funcionais, e não em componentes de classe.

### useCallback

O useCallback é um hook do React que permite que você otimize o desempenho de seus componentes funcionais ao memorizar funções. De forma científica, podemos dizer que o useCallback é um método utilizado para memoização de funções dentro de um componente funcional React, permitindo que o mesmo utilize a mesma instância de uma função em várias renderizações, caso seus argumentos não tenham mudado.

Ao memorizar funções, o useCallback evita que o React recrie essas funções sempre que o componente é renderizado novamente, o que pode causar uma degradação do desempenho, especialmente em componentes complexos que renderizam muitas vezes.

Um exemplo de uso do useCallback seria para criar uma função de filtro em uma lista de itens em um componente funcional.

```javascript
  import React, { useState, useCallback } from 'react';

  function ListaDeItens() {
    const [itens, setItens] = useState([
      { id: 1, nome: 'Item 1' },
      { id: 2, nome: 'Item 2' },
      { id: 3, nome: 'Item 3' }
    ]);
    const [filtro, setFiltro] = useState('');

    const filtrarItens = useCallback(() => {
      return itens.filter(item => item.nome.toLowerCase().includes(filtro.toLowerCase()));
    }, [itens, filtro]);

    return (
      <div>
        <input type="text" value={filtro} onChange={(e) => setFiltro(e.target.value)} />
        <ul>
          {filtrarItens().map(item => (
            <li key={item.id}>{item.nome}</li>
          ))}
        </ul>
      </div>
    );
  }
```

Nesse exemplo, a função useCallback é utilizada para memoizar a função "filtrarItens", que filtra a lista de itens com base no filtro digitado pelo usuário. A função recebe o array de itens e o filtro como argumentos e retorna uma nova lista filtrada.

O useCallback é utilizado para evitar que a função seja recriada sempre que o estado de "itens" ou "filtro" for atualizado. Isso ajuda a melhorar o desempenho do componente, pois a mesma instância da função é reutilizada em várias renderizações, a menos que seus argumentos tenham mudado.

### useMemo

O useMemo é um hook do React que permite que os valores computados sejam armazenados em cache, evitando o recálculo desnecessário desses valores toda vez que o componente é renderizado novamente. Esse recálculo desnecessário pode resultar em um desempenho inadequado, especialmente em componentes complexos que precisam renderizar muitas vezes.

Ao memorizar valores, o useMemo otimiza o desempenho do componente, garantindo que os valores computados sejam reutilizados em várias renderizações, a menos que as dependências tenham mudado. Isso permite que o React evite a execução de cálculos adicionais desnecessários e ajuda a garantir que o componente seja atualizado apenas quando necessário.

Um exemplo de uso do useMemo seria para criar um valor computado em um componente funcional.

```javascript
import React, { useState, useMemo } from 'react';

function Calculadora() {
  const [valor1, setValor1] = useState(0);
  const [valor2, setValor2] = useState(0);

  const resultado = useMemo(() => {
    console.log('Calculando resultado...');
    return valor1 + valor2;
  }, [valor1, valor2]);

  return (
    <div>
      <input type="number" value={valor1} onChange={(e) => setValor1(Number(e.target.value))} />
      <input type="number" value={valor2} onChange={(e) => setValor2(Number(e.target.value))} />
      <p>Resultado: {resultado}</p>
    </div>
  );
}
```

Nesse exemplo, a função useMemo é utilizada para memoizar o valor computado "resultado", que é a soma dos valores de "valor1" e "valor2". A função recebe os valores de "valor1" e "valor2" como argumentos e retorna a soma dos dois valores.

O useMemo é utilizado para evitar que o valor de "resultado" seja recalculado sempre que o componente é renderizado novamente. Isso ajuda a melhorar o desempenho do componente, pois o mesmo valor é reutilizado em várias renderizações, a menos que as suas dependências tenham mudado.

### useEffect

O useEffect é um hook do React que permite que você execute efeitos colaterais em componentes funcionais. De forma científica, podemos dizer que o useEffect é um método que permite que você execute efeitos colaterais em componentes funcionais, como manipulação do DOM, chamadas a APIs externas ou atualizações de estado.

O useEffect é executado após cada renderização do componente e pode ser configurado para executar somente quando certas dependências são atualizadas. Isso permite que você controle quando o efeito é executado e garanta que ele seja executado apenas quando necessário.

```javascript
  import React, { useState, useEffect } from 'react';

  function ExemploUseEffect() {
    const [count, setCount] = useState(0);

    useEffect(() => {
      const intervalId = setInterval(() => {
        setCount(count + 1);
      }, 1000);

      return () => {
        clearInterval(intervalId);
      };
    }, [count]);

    return (
      <div>
        <p>O contador está em: {count}</p>
      </div>
    );
  }
```

Ao executar esse código, você verá que o valor do estado count é atualizado a cada segundo. O useEffect garante que o intervalo de tempo seja definido apenas uma vez e que seja limpo antes da próxima atualização do componente. Isso ajuda a evitar possíveis problemas de desempenho ou vazamentos de memória.
