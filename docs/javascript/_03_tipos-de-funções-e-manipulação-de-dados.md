## Funções

---

### Introdução a Funções em Javascript

Uma função em JavaScript é um bloco de código que executa uma tarefa específica. As funções são usadas para modularizar o código, tornando-o mais fácil de ler e manter. As funções também são usadas para reutilizar código, permitindo que você escreva uma vez e use várias vezes em seu programa.

Sintaxe de Função em JavaScript

A sintaxe básica de uma função em JavaScript é a seguinte:

```javascript
function nome_da_funcao(parametro1, parametro2, ..., parametroN) {
   // Bloco de código que executa a tarefa da função
}
```

Onde:

- `nome_da_funcao`: é o nome que você escolhe para sua função.
- `parametro1, parametro2, ..., parametroN`: são os parâmetros opcionais que você pode passar para a função. Os parâmetros são usados para receber valores que a função irá processar.
- `Bloco de código que executa a tarefa da função`: é o código que a função irá executar quando for chamada.

Por exemplo, vamos criar uma função simples que recebe dois parâmetros e retorna a soma desses parâmetros:

```javascript
function somar(valor1, valor2) {
   return valor1 + valor2;
}
```

Chamando uma Função em JavaScript

Uma vez que você tenha criado uma função, você pode chamá-la em qualquer lugar em seu programa. Para chamar uma função, você simplesmente usa seu nome seguido por parênteses com os argumentos (se houver) que você deseja passar para a função.

Por exemplo, para chamar a função `somar` que criamos anteriormente, você pode fazer o seguinte:

```javascript
var resultado = somar(2, 3);
console.log(resultado); // Saída: 5
```

O que aconteceu aqui é que chamamos a função `somar` passando os valores `2` e `3` como argumentos. A função `somar` então retorna a soma desses valores, que é `5`, que é atribuído à variável `resultado`. Em seguida, imprimimos o resultado usando a função `console.log`.

Retorno de Valores em Funções em JavaScript

As funções em JavaScript podem retornar valores usando a palavra-chave `return`. Quando uma função encontra a palavra-chave `return`, ela interrompe a execução e retorna um valor para quem chamou a função.

Por exemplo, considere a seguinte função que verifica se um número é par ou ímpar:

```javascript
function par_ou_impar(numero) {
   if(numero % 2 === 0) {
      return "par";
   } else {
      return "ímpar";
   }
}
```

Podemos chamar essa função e armazenar o resultado em uma variável:

```javascript
var resultado = par_ou_impar(3);
console.log(resultado); // Saída: "ímpar"
```

Parâmetros de Funções em JavaScript

As funções em JavaScript podem receber parâmetros para processar valores específicos. Os parâmetros são passados ​​para a função como argumentos quando a função é chamada. Os parâmetros são opcionais e você pode passar quantos parâmetros desejar.

Por exemplo, a função `somar` que criamos anteriormente recebe dois parâmetros. Você pode passar qualquer valor para esses parâmetros, desde que correspondam ao tipo de dados que a função espera.

```javascript
function somar(valor1, valor2) {
   return valor1 + valor2;
}

var resultado = somar(2, 3);
console.log(resultado); // Saída: 5
```

Aqui, a função `somar` espera dois parâmetros, `valor1` e `valor2`, que são usados ​​para somar os valores e retornar o resultado.

#### Funções Anônimas em JavaScript

Em JavaScript, você pode criar funções anônimas, que são funções que não possuem nome. As funções anônimas são usadas em situações em que você precisa passar uma função como argumento para outra função.

Por exemplo, a função `setTimeout` em JavaScript espera uma função como argumento para ser executada após um certo período de tempo.

```javascript
setTimeout(function() {
   console.log("Executado após 3 segundos");
}, 3000);
```

Aqui, passamos uma função anônima como argumento para `setTimeout`. A função será executada após 3 segundos e imprimirá a mensagem "Executado após 3 segundos" no console.

Funções são uma parte fundamental de JavaScript e são usadas para modularizar o código, tornando-o mais fácil de ler e manter. As funções também são usadas para reutilizar código, permitindo que você escreva uma vez e use várias vezes em seu programa. Até agora, discutimos a sintaxe básica de uma função em JavaScript, como chamar funções, retornar valores e usar funções anônimas. Com uma compreensão sólida de como as funções funcionam em JavaScript, você estará pronto para escrever código mais complexo e eficiente em JavaScript.

#### CALLBACK

Em JavaScript, um callback é uma função que é passada como argumento para outra função e é executada quando essa função é concluída. O termo "callback" é usado porque a função passada é "chamada de volta" para executar uma ação adicional.

Callbacks são comuns em JavaScript porque a linguagem permite o uso de funções como valores de variáveis, tornando-as cidadãos de primeira classe na linguagem. Isso significa que as funções podem ser tratadas como qualquer outra variável, incluindo passá-las como argumentos para outras funções.

Callbacks são frequentemente usados para lidar com tarefas assíncronas em JavaScript, como fazer chamadas de API ou ler arquivos, onde é necessário esperar uma resposta antes de executar uma ação adicional. Em vez de bloquear a execução do programa enquanto espera pela resposta, o código pode continuar executando e chamar o callback quando a resposta for recebida.

Por exemplo, a função `setTimeout()` em JavaScript é um exemplo comum de uma função que usa callbacks. A função `setTimeout()` recebe dois argumentos: uma função de callback e um tempo em milissegundos. A função de callback é executada depois que o tempo especificado passa:

```javascript
setTimeout(function() {
  console.log('Essa mensagem será exibida após 3 segundos');
}, 3000);
```

Nesse exemplo, uma função anônima é passada como um callback para a função `setTimeout()`. Essa função de callback será chamada após um atraso de 3 segundos.

Callbacks são uma parte fundamental do modelo de programação assíncrona em JavaScript, e são amplamente usados em bibliotecas e frameworks populares, como jQuery, React, Node.js, entre outros.

#### PROMISE

Em JavaScript, `Promise` é um objeto que representa a eventual conclusão (ou falha) de uma operação assíncrona e seu resultado. A ideia básica é que, em vez de esperar que uma operação assíncrona seja concluída antes de continuar a execução do código, podemos criar uma promessa que será resolvida posteriormente com o resultado da operação.

A promessa pode estar em um de três estados: pendente, resolvida ou rejeitada. Quando a promessa está pendente, a operação assíncrona ainda está em andamento. Quando a operação é concluída com sucesso, a promessa é resolvida com o resultado da operação. Se a operação falhar, a promessa é rejeitada com um motivo de erro.

As promessas podem ser usadas para simplificar o código em comparação com o uso de callbacks. Em vez de aninhar várias funções de callback, podemos encadear várias promessas em uma cadeia, usando os métodos `then()` e `catch()`. O método `then()` é usado para lidar com a resolução bem-sucedida da promessa, enquanto o método `catch()` é usado para lidar com a rejeição da promessa.

Abaixo, segue um exemplo simples de como usar uma promessa em JavaScript:

```javascript
function multiplica_por_dois(valor) {
  return new Promise((resolve, reject) => {
    if (typeof valor === 'number') {
      resolve(valor * 2);
    } else {
      reject(new Error('O argumento não é um número.'));
    }
  });
}

multiplica_por_dois(4)
  .then(result => {
    console.log(result); // Resultado: 8
  })
  .catch(error => {
    console.error(error.message);
  });
```

Neste exemplo, a função `multiplica_por_dois()` retorna uma nova promessa que é resolvida com o resultado da multiplicação por dois do argumento passado. Se o argumento não for um número, a promessa é rejeitada com um objeto de erro.

Fora da função, usamos o método `then()` para acessar o valor resolvido da promessa e imprimir o resultado da multiplicação. Também usamos o método `catch()` para lidar com quaisquer erros que possam ocorrer na execução da promessa.

Em resumo, as promessas são objetos que representam a conclusão (ou falha) de uma operação assíncrona e seu resultado. Elas são usadas para simplificar o código em comparação com o uso de callbacks e podem ser encadeadas em uma cadeia usando os métodos `then()` e `catch()`.

#### ASYNC/AWAIT

Em JavaScript, `async`/`await` é uma forma de lidar com tarefas assíncronas que simplifica a sintaxe em relação ao uso de callbacks e promessas. `async` é uma palavra-chave que pode ser usada para declarar uma função assíncrona, que retorna uma promessa que será resolvida com o valor retornado pela função. `await` é uma palavra-chave que pode ser usada dentro de uma função assíncrona para aguardar a resolução de uma promessa antes de continuar a execução do código.

O uso de `async`/`await` pode tornar o código mais legível e fácil de manter em comparação com o uso de callbacks ou promessas. Em vez de aninhar várias funções de callback ou encadear várias promessas, o código pode ser escrito de forma mais sequencial, parecendo com código síncrono. Isso pode tornar o código mais fácil de entender e depurar.

Veja um exemplo simples abaixo para ilustrar o uso de `async`/`await` em JavaScript:

```javascript
async function fetchUserData(userId) {
  const response = await fetch(`https://api.example.com/users/${userId}`);
  const userData = await response.json();
  return userData;
}

fetchUserData(123)
  .then(userData => {
    console.log(`Nome do usuário: ${userData.name}`);
  })
  .catch(error => {
    console.error(error);
  });
```

Neste exemplo, a função `fetchUserData()` é declarada com a palavra-chave `async`. Dentro da função, usamos `await` para aguardar a resposta da API antes de transformar a resposta em um objeto JSON. A função retorna o objeto JSON, que é resolvido como um valor de promessa quando a função é concluída.

Fora da função, chamamos a função `fetchUserData()` passando um ID de usuário como argumento. Em seguida, usamos o método `then()` para acessar o valor resolvido da promessa e imprimir o nome do usuário. Também usamos o método `catch()` para lidar com quaisquer erros que possam ocorrer na execução da função assíncrona.

Em resumo, `async`/`await` é uma forma mais elegante e fácil de ler e escrever código assíncrono em JavaScript. Algumas situações comuns em que você pode querer usar `async`/`await` em vez de callbacks ou promessas são:

1. Fazer requisições assíncronas de dados em uma API;
2. Ler ou gravar arquivos em um sistema de arquivos;
3. Acessar bancos de dados;
4. Executar tarefas assíncronas em segundo plano;
5. Executar tarefas assíncronas complexas que dependem de outras operações assíncronas.

Além disso, o uso de `async`/`await` pode tornar o código mais legível e fácil de manter em comparação com o uso de callbacks ou promessas. Em vez de aninhar várias funções de callback ou encadear várias promessas, o código pode ser escrito de forma mais sequencial, parecendo com código síncrono. Isso pode tornar o código mais fácil de entender e depurar.

No entanto, é importante lembrar que o uso excessivo de `async`/`await` pode levar a problemas de desempenho, pois a execução de uma função assíncrona pode bloquear a execução do thread principal do aplicativo. Portanto, é importante avaliar cuidadosamente a complexidade da tarefa assíncrona e se a abordagem `async`/`await` é a melhor para ela.

### Conversões e manipulação de dados

Em JavaScript, assim como em outras linguagem de programaçao exitem o que chamamos de built-in functions (ou funções integradas) são funções que já vêm pré-definidas na linguagem e podem ser usadas diretamente pelo desenvolvedor sem precisar criar ou importar uma biblioteca externa. Essas funções são amplamente usadas para realizar tarefas comuns de programação, como manipulação de strings, números e datas.

Algumas das funções integradas mais comuns em JavaScript incluem:

- `parseInt()`: converte uma string em um número inteiro.
- `parseFloat()`: converte uma string em um número decimal.
- `isNaN()`: verifica se um valor é um número ou não.
- `toString()`: converte um valor em uma string.
- `Math.random()`: gera um número aleatório entre 0 e 1.
- `Math.floor()`: arredonda um número para baixo para o número inteiro mais próximo.
- `Math.ceil()`: arredonda um número para cima para o número inteiro mais próximo.
- `Math.round()`: arredonda um número para o número inteiro mais próximo.
- `Date.now()`: retorna a data atual em milissegundos desde 1 de janeiro de 1970.

Essas são apenas algumas das muitas funções integradas em JavaScript. Você pode encontrar uma lista completa dessas funções na documentação oficial do JavaScript. Além disso, você pode criar suas próprias funções personalizadas em JavaScript para realizar tarefas específicas de acordo com suas necessidades.

#### Conversão de tipos de dados em JavaScript

JavaScript é uma linguagem dinamicamente tipada, o que significa que os tipos de dados são determinados em tempo de execução. Isso permite que você converta facilmente um tipo de dados em outro, conforme necessário.

Existem várias maneiras de converter tipos de dados em JavaScript. Vamos ver as principais:

- `Number()`: converte um valor em um número.
- `String()`: converte um valor em uma string.
- `Boolean()`: converte um valor em um booleano.
- `parseInt()`: converte uma string em um número inteiro.
- `parseFloat()`: converte uma string em um número decimal.

Por exemplo:

```javascript
let num = "10";
console.log(Number(num)); // 10

let str = 42;
console.log(String(str)); // "42"

let bool = 0;
console.log(Boolean(bool)); // false

let int = "10";
console.log(parseInt(int)); // 10

let float = "3.14";
console.log(parseFloat(float)); // 3.14
```

Observe que, ao converter uma string em um número, você pode usar `parseInt()` para converter para um número inteiro ou `parseFloat()` para um número decimal.

1. Manipulação de strings em JavaScript

Strings são uma parte importante da manipulação de dados em JavaScript. Aqui estão algumas técnicas comuns de manipulação de strings em JavaScript:

- Concatenação de strings: use o operador `+` para concatenar duas ou mais strings. Por exemplo:

```javascript
let str1 = "Hello";
let str2 = "World";
console.log(str1 + " " + str2); // "Hello World"
```

- Acesso a caracteres: use colchetes `[]` para acessar caracteres em uma string. Por exemplo:

```javascript
let str = "JavaScript";
console.log(str[0]); // "J"
console.log(str[4]); // "S"
```

- Método `slice()`: use o método `slice()` para extrair uma parte de uma string. Por exemplo:

```javascript
let str = "JavaScript";
console.log(str.slice(0, 4)); // "Java"
console.log(str.slice(4)); // "Script"
```

- Método `toUpperCase()` e `toLowerCase()`: use esses métodos para converter uma string para maiúsculas ou minúsculas. Por exemplo:

```javascript
let str = "JavaScript";
console.log(str.toUpperCase()); // "JAVASCRIPT"
console.log(str.toLowerCase()); // "javascript"
```

#### Manipulação de arrays em JavaScript

Arrays são uma estrutura de dados poderosa em JavaScript e podem ser facilmente manipulados. Aqui estão algumas técnicas comuns de manipulação de arrays em JavaScript:

- Acesso a elementos: use colchetes `[]` para acessar elementos em um array. Por exemplo:

```javascript
let arr = [1, 2, 3];
console.log(arr[0]); // 1
console.log(arr[2]); // 3
```

JavaScript possui diversos métodos de manipulação de array que permitem adicionar, remover, alterar e pesquisar elementos em um array. Alguns dos métodos mais comuns são:

| Método       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `concat()`   | Retorna um novo array composto pela concatenação do array original com outros arrays e/ou valores.                                                                                                                                                                                                                                                                                                                                                   |
| `join()`     | Retorna uma string que contém todos os elementos do array concatenados, separados por um separador especificado.                                                                                                                                                                                                                                                                                                                                     |
| `slice()`    | Retorna um novo array que é uma cópia de uma parte do array original, especificada pelos índices de início e fim.                                                                                                                                                                                                                                                                                                                                   |
| `splice()`   | Adiciona e/ou remove elementos do array original, retornando um novo array com os elementos removidos.                                                                                                                                                                                                                                                                                                                                             |
| `push()`     | Adiciona um ou mais elementos ao final do array original e retorna o novo tamanho do array.                                                                                                                                                                                                                                                                                                                                                          |
| `pop()`      | Remove o último elemento do array original e retorna esse elemento.                                                                                                                                                                                                                                                                                                                                                                                |
| `shift()`    | Remove o primeiro elemento do array original e retorna esse elemento.                                                                                                                                                                                                                                                                                                                                                                              |
| `unshift()`  | Adiciona um ou mais elementos no início do array original e retorna o novo tamanho do array.                                                                                                                                                                                                                                                                                                                                                        |
| `indexOf()`  | Retorna o índice da primeira ocorrência de um elemento no array original, ou -1 se o elemento não for encontrado.                                                                                                                                                                                                                                                                                                                                    |
| `lastIndexOf()` | Retorna o índice da última ocorrência de um elemento no array original, ou -1 se o elemento não for encontrado.                                                                                                                                                                                                                                                                                                                                        |
| `filter()`   | Retorna um novo array contendo apenas os elementos do array original que atendem a uma determinada condição especificada por uma função de teste.                                                                                                                                                                                                                                                                                                    |
| `map()`      | Retorna um novo array contendo os resultados da aplicação de uma função a cada elemento do array original.                                                                                                                                                                                                                                                                                                                                           |
| `reduce()`   | Executa uma função em cada elemento do array original, acumulando um valor resultante ao longo do array.                                                                                                                                                                                                                                                                                                                                             |
| `forEach()`  | Executa uma função em cada elemento do array original, sem retornar um novo array.                                                                                                                                                                                                                                                                                                                                                                   |
| `some()`     | Retorna `true` se pelo menos um elemento do array atender a uma determinada condição.                                                                                                                                                                                                                                                                                                                                                                 |
| `every()`    | Retorna `true` se todos os elementos do array atenderem a uma determinada condição.                                                                                                                                                                                                                                                                                                                                                                   |
| `find()`     | Retorna o primeiro elemento do array que atende a uma determinada condição.                                                                                                                                                                                                                                                                                                                                                                         |
| `findIndex()` | Retorna o índice do primeiro elemento do array que atende a uma determinada condição.                                                                                                                                                                                                                                                                                                                                                                 |
| `flat()`     | Cria um novo array com todos os elementos de sub-arrays concatenados de forma recursiva até a profundidade especificada.                                                                                                                                                                                                                                                                                                                             |

- `concat()`: Este método retorna um novo array composto pela concatenação do array original com outros arrays e/ou valores. Por exemplo:

```javascript
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const arrayConcatenado = array1.concat(array2);

console.log(arrayConcatenado); // [1, 2, 3, 4, 5, 6]
```

- `join()`: Este método retorna uma string que contém todos os elementos do array concatenados, separados por um separador especificado. Por exemplo:

```javascript
const array = ['apple', 'banana', 'orange'];
const string = array.join(', ');

console.log(string); // "apple, banana, orange"
```

- `slice()`: Este método retorna um novo array que é uma cópia de uma parte do array original, especificada pelos índices de início e fim. Por exemplo:

```javascript
const array = ['a', 'b', 'c', 'd', 'e'];
const newArray = array.slice(1, 4);

console.log(newArray); // ["b", "c", "d"]
```

- `splice()`: Este método adiciona e/ou remove elementos do array original, retornando um novo array com os elementos removidos. Por exemplo:

```javascript
const array = ['a', 'b', 'c', 'd', 'e'];
const removedElements = array.splice(2, 2, 'x', 'y');

console.log(array); // ["a", "b", "x", "y", "e"]
console.log(removedElements); // ["c", "d"]
```

- `push()`: Este método adiciona um ou mais elementos ao final do array original e retorna o novo tamanho do array. Por exemplo:

```javascript
const array = ['a', 'b', 'c'];
const newLength = array.push('d', 'e');

console.log(array); // ["a", "b", "c", "d", "e"]
console.log(newLength); // 5
```

- `pop()`: Este método remove o último elemento do array original e retorna esse elemento. Por exemplo:

```javascript
const array = ['a', 'b', 'c'];
const lastElement = array.pop();

console.log(array); // ["a", "b"]
console.log(lastElement); // "c"
```

- `shift()`: Este método remove o primeiro elemento do array original e retorna esse elemento. Por exemplo:

```javascript
const array = ['a', 'b', 'c'];
const firstElement = array.shift();

console.log(array); // ["b", "c"]
console.log(firstElement); // "a"
```

- `unshift()`: Este método adiciona um ou mais elementos no início do array original e retorna o novo tamanho do array. Por exemplo:

```javascript
const array = ['a', 'b', 'c'];
const newLength = array.unshift('x', 'y');

console.log(array); // ["x", "y", "a", "b", "c"]
console.log(newLength); // 5
```

- `indexOf()`: Este método retorna o índice da primeira ocorrência de um elemento no array original, ou -1 se o elemento não for encontrado. Por exemplo:

```javascript
const array = ['apple', 'banana', 'orange'];
const index = array.indexOf('banana');

console.log(index); // 1
```

- `lastIndexOf()`: Este método retorna o índice da última ocorrência de um elemento no array original, ou -1 se o elemento não for encontrado. Por exemplo:

```javascript
const array = ['apple', 'banana', 'orange', 'banana'];
const index = array.lastIndexOf('banana');

console.log(index); // 3
```

- `filter()`: Este método cria um novo array contendo apenas os elementos do array original que passam em um teste especificado por uma função. Por exemplo:

```javascript
const array = [1, 2, 3, 4, 5];
const newArray = array.filter(function(element) {
  return element > 3;
});

console.log(newArray); // [4, 5]
```

- `map()`: Este método cria um novo array com os resultados de uma função aplicada a cada elemento do array original. Por exemplo:

```javascript
const array = [1, 2, 3, 4, 5];
const newArray = array.map(function(element) {
  return element * 2;
});

console.log(newArray); // [2, 4, 6, 8, 10]
```

- `reduce()`: Este método executa uma função em cada elemento do array original, resultando em um único valor de saída. Por exemplo:

```javascript
const array = [1, 2, 3, 4, 5];
const sum = array.reduce(function(acc, curr) {
  return acc + curr;
}, 0);

console.log(sum); // 15
```

- `forEach()`: Este método executa uma função em cada elemento do array original, sem retornar um novo array. Por exemplo:

```javascript
const array = ['apple', 'banana', 'orange'];
array.forEach(function(element) {
  console.log(element);
});

// "apple"
// "banana"
// "orange"
```

- `some()`: Este método verifica se pelo menos um elemento do array original passa em um teste especificado por uma função, retornando um valor booleano. Por exemplo:

```javascript
const array = [1, 2, 3, 4, 5];
const hasEven = array.some(function(element) {
  return element % 2 === 0;
});

console.log(hasEven); // true
```

- `every()`: Este método verifica se todos os elementos do array original passam em um teste especificado por uma função, retornando um valor booleano. Por exemplo:

```javascript
const array = [1, 2, 3, 4, 5];
const areAllEven = array.every(function(element) {
  return element % 2 === 0;
});

console.log(areAllEven); // false
```

- `find()`: Este método retorna o valor do primeiro elemento do array original que passa em um teste especificado por uma função, ou undefined se nenhum elemento passar no teste. Por exemplo:

```javascript
const array = [1, 2, 3, 4, 5];
const even = array.find(function(element) {
  return element % 2 === 0;
});

console.log(even); // 2
```

- `findIndex()`: Este método retorna o índice do primeiro elemento do array original que passa em um teste especificado por uma função, ou -1 se nenhum elemento passar no teste. Por exemplo:

```javascript
const array = [1, 2, 3, 4, 5];
const index = array.findIndex(function(element) {
  return element % 2 === 0;
});

console.log(index); // 1
```

- `flat()`: Cria um novo array com todos os elementos de sub-arrays concatenados de forma recursiva até a profundidade especificada.

```javascript
const myArray = [1, [2, 3], [[4, 5], 6]];
const flattenedArray = myArray.flat(2);
console.log(flattenedArray); // [1, 2, 3, 4, 5, 6]
```

Esses são apenas alguns exemplos dos métodos disponíveis para manipulação de arrays em JavaScript. É importante lembrar que alguns desses métodos modificam o array original, enquanto outros criam um novo array. Além disso, esses métodos podem ser combinados e encadeados para realizar operações mais complexas. Há muitas outras funções disponíveis que você pode explorar na documentação do JavaScript.
