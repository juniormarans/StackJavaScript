# Estruturas de Repetição

Estruturas de repetição são uma das principais ferramentas disponíveis em linguagens de programação, permitindo que o programador execute uma sequência de instruções repetidamente. Em JavaScript, existem duas estruturas de repetição disponíveis: `while` e `for`.

## WHILE

A instrução `while` é usada para executar um bloco de código enquanto uma determinada condição for verdadeira. A sintaxe é a seguinte:

```javascript
while (condição) {
   // código a ser executado enquanto a condição for verdadeira
}
```

A condição pode ser qualquer expressão que possa ser avaliada como verdadeira ou falsa. Enquanto a condição for verdadeira, o bloco de código dentro das chaves será executado repetidamente. Quando a condição se tornar falsa, a execução será interrompida e o controle será passado para a próxima instrução após o bloco `while`.

Veja um exemplo simples de como utilizar o `while`:

```javascript
let contador = 0;

while (contador < 5) {
  console.log("O contador é: " + contador);
  contador++;
}
```

Nesse exemplo, o `while` é usado para imprimir o valor de "contador" enquanto ele for menor que 5. A cada iteração, o valor de "contador" é incrementado em 1. O resultado desse código seria:

```javascript
O contador é: 0
O contador é: 1
O contador é: 2
O contador é: 3
O contador é: 4
```

## FOR

A instrução `for` é usada para executar um bloco de código um número fixo de vezes. Ela é composta por três partes:

- A inicialização: onde é definida a variável de controle e atribuído o seu valor inicial;
- A condição: que define a condição de parada da repetição;
- O incremento/decremento: que define como a variável de controle será modificada a cada iteração.

A sintaxe da estrutura `for` é a seguinte:

```javascript
for (inicialização; condição; incremento/decremento) {
   // código a ser executado enquanto a condição for verdadeira
}
```

A seguir, vou explicar cada parte da estrutura `for` em mais detalhes.

### Incialização

A inicialização é a primeira parte da estrutura `for`. Ela é usada para definir a variável de controle e atribuir o seu valor inicial. A variável de controle é usada para contar o número de iterações do laço e é geralmente denominada de `i` (embora possa ter outro nome).

A inicialização pode conter uma ou mais instruções separadas por vírgulas. Por exemplo:

Veja um exemplo  de como utilizar o `for` contendo somente uma variavel de inicialização :

```javascript
for (let i = 0; i < 5; i++) {
  console.log("O valor de i é: " + i);
}
```

Nesse exemplo, o `for` é usado para imprimir o valor de "i" enquanto ele for menor que 5. A cada iteração, o valor de "i" é incrementado em 1. O resultado desse código seria:

```javascript
for (let i = 0, j = 10; i < 10; i++, j--) {
   // código a ser executado enquanto a condição for verdadeira
}
```

Nesta inicialização, definimos duas variáveis de controle: `i` e `j`. A variável `i` é iniciada em `0` e a variável `j` em `10`. Na maioria dos casos, usamos apenas uma variável de controle.

## Condição

A condição é a segunda parte da estrutura `for`. Ela define a condição de parada da repetição. A condição é avaliada no início de cada iteração e, se for verdadeira, o bloco de código dentro das chaves será executado. Se a condição for falsa, o bloco de código não será executado e o controle será passado para a próxima instrução após o bloco `for`.

A condição pode ser qualquer expressão que possa ser avaliada como verdadeira ou falsa. Por exemplo:

```javascript
for (let i = 0; i < 10; i++) {
   // código a ser executado enquanto i for menor que 10
}
```

Nesse exemplo, a condição é `i < 10`, o que significa que o bloco de código será executado enquanto o valor da variável `i` for menor que `10`.

## Incremento/Decremento

O incremento/decremento é a terceira parte da estrutura `for`. Ela define como a variável de controle será modificada a cada iteração. O incremento/decremento é executado no final de cada iteração, depois que o bloco de código dentro das chaves é executado.

O incremento/decremento pode ser uma instrução única ou uma série de instruções separadas por vírgulas. Por exemplo:

```javascript
for (let i = 0; i < 10; i += 2) {
   // código a ser executado enquanto i for menor que 10
}
```

Nesse exemplo, a variável `i` é incrementada em `2` a cada iteração, em vez do valor padrão de `1`.

## For of

O `for...of` é uma estrutura de repetição introduzida no ECMAScript 6 (também conhecido como ES6 ou ECMAScript 2015) que permite iterar sobre elementos iteráveis, como arrays, strings, objetos do tipo Map e Set, entre outros.

A sintaxe do `for...of` é a seguinte:

```javascript
for (variável of iterável) {
  // código a ser executado para cada elemento do iterável
}
```

Onde `variável` é a variável que receberá o valor de cada elemento do iterável em cada iteração, e `iterável` é o objeto iterável a ser percorrido.

Por exemplo, podemos usar o `for...of` para iterar sobre um array:

```javascript
const array = [1, 2, 3];

for (const elemento of array) {
  console.log(elemento);
}
```

Nesse caso, a cada iteração, a variável `elemento` receberá o valor de cada elemento do array, na ordem em que aparecem. O resultado impresso no console seria:

```javascript
1
2
3
```

Podemos também usar o `for...of` para iterar sobre uma string:

```javascript
const string = "JavaScript";

for (const caractere of string) {
  console.log(caractere);
}
```

Nesse caso, a cada iteração, a variável `caractere` receberá um dos caracteres da string, na ordem em que aparecem. O resultado impresso no console seria:

```javascript
J
a
v
a
S
c
r
i
p
t
```

É importante notar que o `for...of` não permite acessar o índice de cada elemento do iterável. Se for necessário acessar o índice, é recomendado utilizar o `for` convencional ou o método `forEach` dos arrays.

Em resumo, o `for...of` é uma estrutura de repetição que permite iterar sobre elementos iteráveis de forma simples e concisa, tornando o código mais legível e fácil de entender.

## FOR IN

O `for...in` é uma estrutura de repetição em JavaScript que permite iterar sobre as propriedades enumeráveis de um objeto. A sintaxe do `for...in` é a seguinte:

```javascript
for (propriedade in objeto) {
  // código a ser executado para cada propriedade do objeto
}
```

Onde `propriedade` é o nome de cada propriedade enumerável do objeto em cada iteração, e `objeto` é o objeto a ser percorrido.

Por exemplo, podemos usar o `for...in` para iterar sobre as propriedades de um objeto:

```javascript
const objeto = {
  nome: "João",
  idade: 30,
  profissao: "Desenvolvedor",
};

for (const propriedade in objeto) {
  console.log(`${propriedade}: ${objeto[propriedade]}`);
}
```

Nesse caso, a cada iteração, a variável `propriedade` receberá o nome de cada propriedade enumerável do objeto, e o valor de cada propriedade será acessado usando a sintaxe de colchetes `objeto[propriedade]`. O resultado impresso no console seria:

```javascript
nome: João
idade: 30
profissao: Desenvolvedor
```

É importante notar que o `for...in` itera apenas sobre as propriedades enumeráveis do objeto, ou seja, aquelas que têm a flag `enumerable` definida como `true`. Algumas propriedades padrão dos objetos, como `length` de arrays e `prototype` de funções, por exemplo, têm a flag `enumerable` definida como `false` e, portanto, não são iteradas pelo `for...in`.

Além disso, é recomendado usar o `for...in` apenas em objetos simples, como objetos literais, e não em objetos complexos que podem herdar propriedades indesejadas de seus protótipos. Para iterar sobre elementos de arrays e outros tipos de coleções, é recomendado utilizar o `for...of` ou o `forEach` dos arrays.

Em resumo, o `for...in` é uma estrutura de repetição que permite iterar sobre as propriedades enumeráveis de um objeto, acessando seus nomes e valores de forma simples e direta.
