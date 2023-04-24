# Tipos de Variáveis em JavaScript

Variáveis e constantes são elementos fundamentais em qualquer linguagem de programação, incluindo JavaScript. Variáveis são usadas para armazenar valores que podem ser alterados durante a execução do programa, enquanto as constantes são usadas para armazenar valores que não podem ser alterados.

`var`, `let` e `const` são palavras-chave usadas para declarar variáveis em JavaScript.

`let` e `const` foram introduzidas no ES6 (ECMAScript 2015). Ambas têm escopo de bloco, o que significa que uma variável declarada com `let` ou `const` só é acessível dentro do bloco em que foi declarada (um bloco é qualquer coisa cercada por chaves, como um loop, uma instrução if ou uma função).

A diferença entre `let` e `const` é que as variáveis ​​`let` podem ser reatribuídas dentro do seu escopo, enquanto as variáveis ​​`const` não podem ser reatribuídas. Isso torna `const` útil para declarar constantes ou valores que não devem ser alterados.

Para declarar uma variável em JavaScript, você pode usar a palavra-chave `var`, `let` ou `const`, seguida pelo nome da variável e, opcionalmente, um valor inicial. Aqui estão alguns exemplos:

  ```javascript
  var numero = 5; // variável declarada com "var"
  let texto = "Hello"; // variável declarada com "let"
  const pi = 3.14; // constante declarada com "const"
  ```

Observe que o valor da variável pode ser alterado a qualquer momento usando a atribuição de valor:

  ```javascript
  numero = 10; // numero agora tem o valor 10
  texto = "World"; // texto agora tem o valor "World"
  ```

No entanto, o valor de uma constante não pode ser alterado depois de ser definido:

  ```javascript
  pi = 2.71; // isso causaria um erro porque "pi" é uma constante
  ```

É uma boa prática usar constantes sempre que o valor não precisa ser alterado e variáveis quando o valor pode mudar durante a execução do programa. Além disso, o uso de "let" em vez de "var" é recomendado em versões mais recentes do JavaScript para evitar problemas com escopo de variáveis.

## Escopo de Variáveis em JavaScript

O escopo de variáveis em JavaScript define a visibilidade de uma variável dentro de um determinado bloco de código. Em outras palavras, o escopo determina onde a variável pode ser acessada e modificada dentro do programa.

Existem dois tipos de escopo de variáveis em JavaScript: escopo global e escopo local.

O escopo global é o escopo mais amplo, onde as variáveis são definidas fora de qualquer bloco de código, como funções ou loops. Variáveis globais podem ser acessadas e modificadas em qualquer parte do programa, o que pode levar a erros difíceis de depurar. Aqui está um exemplo de variável global:

### Escopo Global

A variável `var` foi o primeiro tipo de variável introduzido em JavaScript. Ela é global por padrão, o que significa que ela pode ser acessada de qualquer lugar do código. Além disso, a variável `var` pode ser declarada várias vezes no mesmo escopo sem gerar erro. No entanto, seu escopo é limitado ao escopo da função em que ela foi declarada, se houver.

```javascript
// Variáveis globais devem ter nomes descritivos e ser declaradas fora de qualquer bloco de código
let contadorGlobal = 0;

function addContadorGlobal() {
  contadorGlobal++; // A variável contadorGlobal pode ser acessada e modificada dentro da função
  console.log(`Contador global é agora: ${contadorGlobal}`);
}

addContadorGlobal(); // Chama a função para incrementar a variável globalCount
```

### Escopo Local

O **escopo local** é o escopo dentro de um bloco de código, como uma `função` ou um `loop`. **Variáveis locais** só podem ser acessadas dentro do bloco onde foram definidas e podem ter o mesmo nome de variáveis globais ou de outros escopos locais sem conflitos. Aqui está um exemplo de variável local:

```javascript
function calculoAreaCirculo(raio) {
  // Variáveis locais devem ter nomes descritivos e ser declaradas dentro do bloco de código onde são usadas
  const PI = 3.14159;
  let area = PI * raio * raio; // A variável area só pode ser acessada dentro desta função
  console.log(`A área do circulo de raio ${raio} é ${area}`);
}

calculoAreaCirculo(5); // Chama a função para calcular a área de um círculo com raio 5
```

### Exemplo com Escopo global e local

```javascript
function exemplo() {
  let variavelEscopoGlobal = 1;
  if (true) {
    let variavelEscopoLimitado = 2;
    console.log(variavelEscopoGlobal); // imprime "1"
  }
  console.log(variavelEscopoLimitado); // gera um erro: "Uncaught ReferenceError: variavelEscopoLimitado is not defined"
}

exemplo();
```

No exemplo acima, a variável `variavelEscopoGlobal` tem escopo global, enquanto a variável `variavelEscopoLimitado` tem escopo limitado ao bloco de código `if`. A tentativa de acessar a variável `variavelEscopoLimitado` fora do bloco de código resulta em um erro.
