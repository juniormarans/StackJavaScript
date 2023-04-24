# Conversões e manipulação de dados

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

## Conversão de tipos de dados em JavaScript

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

## Manipulação de arrays em JavaScript

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
