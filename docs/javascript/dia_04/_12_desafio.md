# Desafio

JavaScript é uma das linguagens de programação mais utilizadas no mundo, principalmente no desenvolvimento de aplicações web. Como programador(a) em JavaScript, é importante sempre buscar desafios para melhorar suas habilidades e aprimorar seus conhecimentos na linguagem.

## Projeto Prático

Implemente uma calculadora simples em JavaScript que pode realizar operações básicas, como adição, subtração, multiplicação e divisão, e ao final imprima em tela o resultado da operação.

Exemplos:

### Calculadora

O código a seguir define a função `calcular` que recebe dois números (`valor1` e `valor2`) e um operador (`operador`) e retorna o resultado da operação especificada pelo operador. O código usa um `switch` para verificar qual é o operador e realizar a operação apropriada.

Em seguida, o código pede para o usuário digitar os números e o operador usando a função `prompt` e chama a função `calcular` para obter o resultado. Finalmente, o código usa a função `console.log` para imprimir o resultado no console do navegador ou do Node.js.

```javascript
// Define a função de cálculo
function calcular(valor1, valor2, operador) {
let resultado;

switch (operador) {
    case "+":
    resultado = valor1 + valor2;
    break;
    case "-":
    resultado = valor1 - valor2;
    break;
    case "*":
    resultado = valor1 * valor2;
    break;
    case "/":
    resultado = valor1 / valor2;
    break;
    default:
    resultado = "Operador inválido";
}

return resultado;
}

// Pede para o usuário digitar os números e o operador
let valor1 = Number(prompt("Digite o primeiro número:"));
let valor2 = Number(prompt("Digite o segundo número:"));
let operador = prompt("Digite o operador (+, -, *, /):");

// Chama a função de cálculo e imprime o resultado
let resultado = calcular(valor1, valor2, operador);
console.log(`O resultado da operação é: ${resultado}`);
```

Você pode personalizar este exemplo adicionando mais operações ou melhorando a interface do usuário para torná-la mais amigável.

O mesmo exemplo utilizando Typescript:

```typescript
// Define a função de cálculo
function calcular(valor1: number, valor2: number, operador: string): number | string {
let resultado: number | string;

switch (operador) {
    case "+":
    resultado = valor1 + valor2;
    break;
    case "-":
    resultado = valor1 - valor2;
    break;
    case "*":
    resultado = valor1 * valor2;
    break;
    case "/":
    resultado = valor1 / valor2;
    break;
    default:
    resultado = "Operador inválido";
}

return resultado;
}

// Pede para o usuário digitar os números e o operador
let valor1 = Number(prompt("Digite o primeiro número:"));
let valor2 = Number(prompt("Digite o segundo número:"));
let operador = prompt("Digite o operador (+, -, *, /):");

// Chama a função de cálculo e imprime o resultado
let resultado = calcular(valor1, valor2, operador);
console.log(`O resultado da operação é: ${resultado}`);
```

Este código é semelhante ao exemplo anterior em JavaScript, mas com a adição de tipos de dados explícitos para as variáveis e para os parâmetros e retorno da função.

Além disso, a variável `resultado` agora pode ser do tipo `number` ou `string`, pois a função pode retornar uma mensagem de erro quando o operador é inválido. Para indicar isso, usei a sintaxe `number | string`, que significa que a variável pode ser do tipo `number` ou do tipo `string`.

Note que este código também precisa ser compilado antes de ser executado em um ambiente JavaScript. Você pode fazer isso usando o compilador TypeScript, que pode ser instalado usando o comando `npm install -g typescript` no terminal. Em seguida, execute o comando `tsc arquivo.ts` para compilar o código TypeScript e gerar um arquivo JavaScript. Depois disso, você pode executar o arquivo JavaScript normalmente em um ambiente Node.js ou em um navegador.

## Proposta

Crie uma alternativa ao código da calculadora em JavaScript utilizando `if` em vez de `switch`

Atenção! **somente para o professor**:

```javascript
// Define a função de cálculo
function calcular(valor1, valor2, operador) {
  let resultado;
  
  if (operador === "+") {
    resultado = valor1 + valor2;
  } else if (operador === "-") {
    resultado = valor1 - valor2;
  } else if (operador === "*") {
    resultado = valor1 * valor2;
  } else if (operador === "/") {
    resultado = valor1 / valor2;
  } else {
    resultado = "Operador inválido";
  }
  
  return resultado;
}

// Pede para o usuário digitar os números e o operador
let valor1 = Number(prompt("Digite o primeiro número:"));
let valor2 = Number(prompt("Digite o segundo número:"));
let operador = prompt("Digite o operador (+, -, *, /):");

// Chama a função de cálculo e imprime o resultado
let resultado = calcular(valor1, valor2, operador);
console.log(`O resultado da operação é: ${resultado}`);
```

Este código é semelhante aos exemplos anteriores, mas usa declarações `if` em vez de `switch` para verificar qual é o operador e realizar a operação apropriada.

Note que a estrutura do código é um pouco diferente do código `switch` anterior, pois as declarações `if` são aninhadas em vez de estarem em um bloco único. Além disso, a declaração `else` é usada para tratar o caso em que o operador é inválido.

Você pode personalizar este exemplo adicionando mais operações ou melhorando a interface do usuário para torná-la mais amigável.
