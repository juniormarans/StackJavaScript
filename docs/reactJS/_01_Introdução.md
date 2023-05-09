## Introdução a ReactJs

React JS é um framework de código aberto desenvolvido pelo Facebook que é amplamente utilizado para criar interfaces de usuário interativas em aplicações web. O React é baseado em um modelo de programação orientado a componentes, no qual a interface do usuário é construída a partir de componentes reutilizáveis e independentes.

O React utiliza um modelo de programação declarativa, no qual os desenvolvedores descrevem o que eles querem que a interface do usuário faça e o React cuida de como isso será feito. Esse modelo reduz a complexidade do código e torna mais fácil a manutenção e atualização da aplicação.

Além disso, ele utiliza um algoritmo de reconciliação virtual que torna mais eficiente a atualização da interface do usuário, evitando a necessidade de atualizar a página inteira. Isso resulta em uma melhor experiência do usuário e um desempenho mais rápido da aplicação.

O React também é altamente extensível, permitindo que os desenvolvedores criem suas próprias bibliotecas e plugins para estender a funcionalidade do framework. Além disso, existem várias bibliotecas de terceiros disponíveis para o React, tornando-o ainda mais versátil.

### Noções de programação funcional

A programação funcional é um paradigma de programação que enfatiza a utilização de funções para realizar cálculos e transformações de dados. Na programação funcional, as funções são consideradas como valores de primeira classe, o que significa que elas podem ser passadas como parâmetros para outras funções e retornadas como resultado de outras funções.

#### Componentes funcionais

Os componentes funcionais são uma das principais características da programação funcional em React JS. Eles são criados como funções que retornam uma descrição da interface do usuário.

```javascript
  function Welcome(props) {
    return <h1>Hello, {props.name}!</h1>;
  }
```

Este é um componente funcional que recebe um objeto props como parâmetro e retorna um elemento h1 com o nome passado como uma das propriedades desse objeto.

#### Imutabilidade

React JS utiliza o conceito de imutabilidade para prevenir alterações acidentais nos dados da aplicação. Um exemplo disso pode ser visto ao atualizar o estado de um componente. Em vez de modificar diretamente o estado, você deve criar um novo objeto com as alterações desejadas.

```javascript
  function Counter() {
    const [count, setCount] = useState(0);
    
    function increment() {
      setCount(count + 1); // ERRADO!
      setCount(prevCount => prevCount + 1); // CORRETO!
    }
    
    return (
      <div>
        <p>Count: {count}</p>
        <button onClick={increment}>Increment</button>
      </div>
    );
  }
```
