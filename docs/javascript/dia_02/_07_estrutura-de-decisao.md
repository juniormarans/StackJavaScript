# Estrutura de Decisão

As estruturas de decisão em JavaScript são responsáveis por permitir que o programa faça escolhas lógicas e tome diferentes caminhos de acordo com as condições estabelecidas. As estruturas de decisão mais comuns são: if, if-else, switch-case e operador ternário.

Tabela:

| Estrutura | Descrição |
|-----------|-----------|
| if | Verifica se uma condição é verdadeira e executa um bloco de código caso a condição seja atendida |
| if-else | Verifica se uma condição é verdadeira e executa um bloco de código caso a condição seja atendida, caso contrário, executa um outro bloco de código |
| switch-case | Verifica uma expressão e executa um bloco de código dependendo do valor dessa expressão |
| operador ternário | É uma forma abreviada de escrever uma estrutura if-else em apenas uma linha |

## if

O `if` é uma das estruturas de decisão mais básicas em JavaScript. Ele permite que o código execute uma determinada ação somente se uma condição for verdadeira. A sintaxe do `if` é a seguinte:

```javascript
if (condição) {
  // código a ser executado se a condição for verdadeira
}
```

Por exemplo, vamos supor que queremos exibir uma mensagem somente se uma pessoa tiver idade suficiente para votar nas eleições. O código ficaria assim:

```javascript
let idade = 20;

if (idade >= 18) {
  console.log("Você pode votar nas eleições.");
}
```

Nesse caso, como a idade é maior ou igual a 18, a mensagem "Você pode votar nas eleições." será exibida no console.

Também é possível usar uma cláusula `else` para executar um código caso a condição seja falsa. A sintaxe do `if-else` é a seguinte:

```javascript
if (condição) {
  // código a ser executado se a condição for verdadeira
} else {
  // código a ser executado se a condição for falsa
}
```

Por exemplo, vamos supor que queremos exibir uma mensagem informando se uma pessoa pode votar ou não nas eleições. O código ficaria assim:

```javascript
let idade = 14;

if (idade >= 16) {
  console.log("Você pode votar nas eleições.");
} else {
  console.log("Você não pode votar nas eleições.");
}
```

Nesse caso, como a idade é menor que 16, a mensagem "Você não pode votar nas eleições." será exibida no console.

Também é possível usar várias cláusulas `else if` para testar várias condições diferentes. A sintaxe do `if-else if` é a seguinte:

```javascript
if (condição1) {
  // código a ser executado se a condição1 for verdadeira
} else if (condição2) {
  // código a ser executado se a condição2 for verdadeira e a condição1 for falsa
} else if (condição3) {
  // código a ser executado se a condição3 for verdadeira e as condições 1 e 2 forem falsas
} else {
  // código a ser executado se nenhuma das condições anteriores for verdadeira
}
```

Por exemplo, vamos supor que queremos exibir uma mensagem informando em que faixa etária uma pessoa se encontra. O código ficaria assim:

```javascript
let idade = 25;

if (idade < 18) {
  console.log("Você é menor de idade.");
} else if (idade >= 18 && idade < 60) {
  console.log("Você é adulto.");
} else {
  console.log("Você é idoso.");
}
```

Nesse caso, como a idade é maior ou igual a 18 e menor que 60, a mensagem "Você é adulto." será exibida no console. Dessa forma, a utilização do else if permite uma maior flexibilidade e precisão na tomada de decisões, especialmente quando há múltiplas condições a serem avaliadas.

o trecho de codigo abaixo teria o mesmo resultado mas devemos evitá-lo:

```javascript
let idade = 25;

if (idade < 18) {
  console.log("Você é menor de idade.");
}
if (idade >= 18 && idade < 60) {
  console.log("Você é adulto.");
}
if (idade >= 60) {
  console.log("Você é adulto.");
}
```

## switch-case

O `switch-case` é uma estrutura condicional que permite executar um determinado bloco de código dependendo do valor de uma expressão. A sintaxe do `switch-case` é a seguinte:

```javascript
switch (expressão) {
  case valor1:
    // código a ser executado se a expressão for igual a valor1
    break;
  case valor2:
   // código a ser executado se a expressão for igual a valor2
    break;
  default:
    // código a ser executado se a expressão não for igual a nenhum dos valores
}
```

Por exemplo, vamos supor que queremos exibir o nome de um dia da semana com base no número correspondente. O código ficaria assim:

```javascript
let dia = 3;

switch (dia) {
  case 1:
    console.log("Domingo");
    break;
  case 2:
    console.log("Segunda-feira");
    break;
  case 3:
    console.log("Terça-feira");
    break;
  case 4:
    console.log("Quarta-feira");
    break;
  case 5:
    console.log("Quinta-feira");
    break;
  case 6:
    console.log("Sexta-feira");
    break;
  case 7:
    console.log("Sábado");
    break;
  default:
    console.log("Dia inválido");
}
```

Nesse caso, como o valor de `dia` é 3, a mensagem "Terça-feira" será exibida no console.

## ternário

O operador ternário é uma forma concisa de escrever uma estrutura `if-else`. A sintaxe do operador ternário é a seguinte:

```javascript
condição ? valorSeVerdadeiro : valorSeFalso
```

Por exemplo, vamos supor que queremos exibir uma mensagem informando se uma pessoa pode votar nas eleições. O código usando o operador ternário ficaria assim:

```javascript
let idade = 20;
let mensagem = idade >= 16 ? "Você pode votar nas eleições." : "Você não pode votar nas eleições.";
console.log(mensagem);
```

Nesse caso, como a idade é maior ou igual a 16, a mensagem "Você pode votar nas eleições." será exibida no console.

## try/catch/finally

O bloco try envolve um conjunto de instruções que podem gerar exceções (ou erros). Se ocorrer uma exceção dentro do bloco try, o controle é transferido para o bloco catch. O bloco catch é responsável por tratar a exceção, e pode conter um conjunto de instruções que lidam com o erro.

Veja um exemplo:

```javascript
try {
  // código que pode gerar exceções
} catch (e) {
  // tratamento da exceção
}
```

Neste exemplo, o código que pode gerar exceções é colocado dentro do bloco try. Se ocorrer uma exceção, o controle é transferido para o bloco catch, onde a exceção é tratada. O parâmetro e representa a exceção que foi lançada.

Vamos ver um exemplo simples de como usar o try-catch em JavaScript:

```javascript
try {
  // Código que pode lançar uma exceção
  console.log('Executando o código do bloco try...');
  throw new Error('Ocorreu um erro!');
} catch (excecao) {
  // Tratamento de exceção
  console.log('Executando o código do bloco catch...');
  console.log(excecao.message);
}
```

Além disso, é possível utilizar a cláusula finally para definir um bloco de código que será executado independentemente de ocorrer ou não uma exceção. Este bloco é opcional e pode ser utilizado para limpar recursos, por exemplo.

Veja um exemplo completo:

try {
  // código que pode gerar exceções
} catch (e) {
  // tratamento da exceção
} finally {
  // código que será executado independentemente de ocorrer ou não uma exceção
}

Em resumo, a utilização dos blocos try, catch e finally é importante para garantir que exceções sejam tratados de forma adequada durante a execução de um programa em JavaScript.
