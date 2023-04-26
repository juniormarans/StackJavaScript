# Tipos de dados em JavaScript

JavaScript possui vários tipos de dados, como números, strings, booleanos, arrays, objetos e muito mais. Cada tipo de dado é usado para representar um conjunto específico de valores e tem um conjunto específico de operações que podem ser realizadas com ele.

## Tipos de dados primitivos

Os tipos de dados primitivos são aqueles que são diretamente suportados pela linguagem. Eles são imutáveis, o que significa que seus valores não podem ser alterados depois de definidos. Os tipos de dados primitivos em JavaScript são:

- Number: são usados para representar valores numéricos. Podem ser inteiros ou decimais. Exemplo:

  ```javascript
  let idade = 30; 
  let altura = 1.75;
  typeof idade; // imprime number
  ```

- Strings: são usados para representar valores de texto. Podem ser definidos usando aspas simples ou duplas. Exemplo:

  ```javascript
  let nome = "João";
  let sobrenome = 'Silva';
  typeof nome; // imprime string
  ```

- Booleanos: são usados para representar valores verdadeiro ou falso. Exemplo:

  ```javascript
  let aprovado = true;
  let reprovado = false;
  typeof aprovado; // imprime boolean
  ```

- Null: é usado para representar um valor nulo ou vazio. Exemplo:

  ```javascript
  let valor = null;
  ```

- Undefined: é usado para representar uma variável que ainda não foi definida. Exemplo:

  ```javascript
  let x;
  console.log(x); // imprime "undefined"
  ```

- Symbol: é usado para criar valores únicos e não modificáveis. Exemplo:

  ```javascript
  let id = Symbol();
  ```

## Tipos de dados não primitivos

Os tipos de dados não primitivos são aqueles que são definidos pelo usuário ou são objetos. Eles são mutáveis, o que significa que seus valores podem ser alterados depois de definidos. Os tipos de dados não primitivos em JavaScript são:

- Arrays: são usados para representar coleções ordenadas de valores. Podem conter qualquer tipo de dado, inclusive outros arrays. Exemplo:

  ```javascript
  let numeros = [1, 2, 3];
  let nomes = ["João", "Maria", "Pedro"];
  let misto = [[1, 2, 3], ["João", "Maria", "Pedro"], 2, "Marcos"];
  ```

- Objetos: são usados para representar coleções de propriedades e valores relacionados. Cada propriedade é uma chave que aponta para um valor. Exemplo:

  ```javascript
  let pessoa = { 
    nome: "João", 
    idade: 30, 
    altura: 1.75,
  };
  ```

- Funções: são usadas para agrupar um conjunto de ações em um bloco de código reutilizável. Podem ser declaradas com ou sem parâmetros. Exemplo:

  ```javascript
  function saudacao(nome) {
    console.log("Olá, " + nome + "!");
  }

  saudacao("João"); // imprime "Olá, João!"
  ```

Em resumo, JavaScript possui vários tipos de dados que são usados para representar diferentes tipos de valores. É importante entender os diferentes tipos de dados para poder trabalhar com eles corretamente em seus programas.
