## Resolução desafio

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
