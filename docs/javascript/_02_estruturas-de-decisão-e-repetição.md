## Estruturas de decisão e repetição

---

### Estrutura de Decisão

As estruturas de decisão em JavaScript são responsáveis por permitir que o programa faça escolhas lógicas e tome diferentes caminhos de acordo com as condições estabelecidas. As estruturas de decisão mais comuns são: if, if-else, switch-case e operador ternário.

Tabela:

| Estrutura | Descrição |
|-----------|-----------|
| if | Verifica se uma condição é verdadeira e executa um bloco de código caso a condição seja atendida |
| if-else | Verifica se uma condição é verdadeira e executa um bloco de código caso a condição seja atendida, caso contrário, executa um outro bloco de código |
| switch-case | Verifica uma expressão e executa um bloco de código dependendo do valor dessa expressão |
| operador ternário | É uma forma abreviada de escrever uma estrutura if-else em apenas uma linha |

#### if

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

#### switch-case

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

#### ternário

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

#### try/catch/finally

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

### Estruturas de Repetição

Estruturas de repetição são uma das principais ferramentas disponíveis em linguagens de programação, permitindo que o programador execute uma sequência de instruções repetidamente. Em JavaScript, existem duas estruturas de repetição disponíveis: `while` e `for`.

#### WHILE

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

#### FOR

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

##### Incialização

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

#### Condição

A condição é a segunda parte da estrutura `for`. Ela define a condição de parada da repetição. A condição é avaliada no início de cada iteração e, se for verdadeira, o bloco de código dentro das chaves será executado. Se a condição for falsa, o bloco de código não será executado e o controle será passado para a próxima instrução após o bloco `for`.

A condição pode ser qualquer expressão que possa ser avaliada como verdadeira ou falsa. Por exemplo:

```javascript
for (let i = 0; i < 10; i++) {
   // código a ser executado enquanto i for menor que 10
}
```

Nesse exemplo, a condição é `i < 10`, o que significa que o bloco de código será executado enquanto o valor da variável `i` for menor que `10`.

#### Incremento/Decremento

O incremento/decremento é a terceira parte da estrutura `for`. Ela define como a variável de controle será modificada a cada iteração. O incremento/decremento é executado no final de cada iteração, depois que o bloco de código dentro das chaves é executado.

O incremento/decremento pode ser uma instrução única ou uma série de instruções separadas por vírgulas. Por exemplo:

```javascript
for (let i = 0; i < 10; i += 2) {
   // código a ser executado enquanto i for menor que 10
}
```

Nesse exemplo, a variável `i` é incrementada em `2` a cada iteração, em vez do valor padrão de `1`.

#### For of

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

#### FOR IN

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

### Exercicios de fixação

#### Exercicio de Estruturas de decisão

1. Crie um programa utilizando operador `if` e `else` que: leia um número inteiro e verifique se ele é par ou ímpar.

2. Crie um programa utilizando operador `if` e `else` que: verifique se uma pessoa é maior ou menor de idade (considere que a idade mínima é 18 anos).

3. Crie um programa utilizando operador `if` e `else` que: leia duas notas de um aluno, calcule a media e verifique se ele foi aprovado ou reprovado (nota mínima de aprovação é 6).

4. Crie um programa utilizando operador `switch-case` que: leia um número inteiro de 1 a 7 e imprima o dia da semana correspondente.

5. Crie um programa utilizando operador `switch-case` que: leia uma letra e verifique se ela é vogal ou consoante.

6. Crie um programa utilizando operador `switch-case` que: leia um número inteiro de 1 a 12 e imprima o nome do mês correspondente.

7. Crie um programa utilizando operador `ternario` que: leia um número e informe se ele é positivo ou negativo.

8. Crie um programa utilizando operador `ternario` que: leia a idade de uma pessoa e informe se ela é maior ou menor de idade.

9. Crie um programa utilizando operador `ternario` que: leia dois números e informe qual deles é o maior.

10. Crie um programa utilizando operador `try-catch-finally` que: tente converter uma string em um número, e caso ocorra um erro, informe uma mensagem amigável ao usuário.

11. Crie um programa utilizando operador `try-catch-finally` que: tente acessar uma propriedade de um objeto que não existe, e caso ocorra um erro, informe uma mensagem amigável ao usuário.

12. Crie um programa utilizando operador `try-catch-finally` que: tente dividir um número por zero, e caso ocorra um erro, informe uma mensagem amigável ao usuário.

#### Exercicio de Estruturas de repetição

1. Crie um programa utilizando a estrutura `for` que: exiba no console os números de 1 a 10.

2. Crie um programa  utilizando a estrutura `for` que: exiba no console os números pares de 1 a 20.

3. Crie um programa utilizando a estrutura `for` que: exiba no console os números de 50 a 1 em ordem decrescente, pulando de 5 em 5.

4. Crie um programa utilizando a estrutura `while` que: exiba no console a soma dos números de 1 a 10.

5. Crie um programa utilizando a estrutura `while` que: exiba no console os números ímpares de 1 a 20.

### Respostas Exercicios de fixação

#### Estruturas de decisão

1. Crie um programa utilizando operador `if` e `else` que: leia um número inteiro e verifique se ele é par ou ímpar.

    ```javascript
    let numero = 10; // exemplo
    if (numero % 2 === 0) {
    console.log(numero + " é par.");
    } else {
    console.log(numero + " é ímpar.");
    }
    ```

2. Crie um programa utilizando operador `if` e `else` que: verifique se uma pessoa é maior ou menor de idade (considere que a idade mínima é 18 anos).

    ```javascript
    let idade = 20; // exemplo
    if (idade >= 18) {
    console.log("Maior de idade.");
    } else {
    console.log("Menor de idade.");
    }
    ```

3. Crie um programa utilizando operador `if` e `else` que: leia duas notas de um aluno, calcule a media e verifique se ele foi aprovado ou reprovado (nota mínima de aprovação é 6).

    ```javascript
    let nota1 = 7; // primeira nota
    let nota2 = 5; // segunda nota
    let media = (nota1 + nota2) / 2;
    if (media >= 6) {
    console.log("Aprovado.");
    } else {
    console.log("Reprovado.");
    }
    ```

4. Crie um programa utilizando operador `switch-case` que: leia um número inteiro de 1 a 7 e imprima o dia da semana correspondente.

    ```javascript
    let numero = 5; // exemplo
    switch (numero) {
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
        console.log("Número inválido");
    }
    ```

5. Crie um programa utilizando operador `switch-case` que: leia uma letra e verifique se ela é vogal ou consoante.

    ```javascript
    let letra = "a"; // exemplo
    switch (letra) {
    case "a":
    case "e":
    case "i":
    case "o":
    case "u":
        console.log("Vogal");
        break;
    default:
        console.log("Consoante");
    }
    ```

6. Crie um programa utilizando operador `switch-case` que: leia um número inteiro de 1 a 12 e imprima o nome do mês correspondente.

    ```javascript
    let numero = 9; // exemplo
    switch (numero) {
    case 1:
        console.log("Janeiro");
        break;
    case 2:
        console.log("Fevereiro");
        break;
    case 3:
        console.log("Março");
        break;
    case 4:
        console.log("Abril");
        break;
    case 5:
        console.log("Maio");
        break;
    case 6:
        console.log("Junho");
        break;
    case 7:
        console.log("Julho");
        break;
    case 8:
        console.log("Agosto");
        break;
    case 9:
        console.log("Setembro");
        break;
    case 10:
        console.log("Outubro");
        break;
    case 11:
        console.log("Novembro");
        break;
    case 12:
        console.log("Dezembro");
        break;
    default:
        console.log("Número inválido");
    }
    ```

7. Crie um programa utilizando operador `ternario` que: leia um número e informe se ele é positivo ou negativo.

    ```javascript
    let numero = 5; // exemplo
    let resultado = numero >= 0 ? "positivo" : "negativo";
    console.log(resultado);
    ```

8. Crie um programa utilizando operador `ternario` que: leia a idade de uma pessoa e informe se ela é maior ou menor de idade.

    ```javascript
    let idade = 20; // exemplo
    let resultado = idade >= 18 ? "maior de idade" : "menor de idade";
    console.log(resultado);
    ```

9. Crie um programa utilizando operador `ternario` que: leia dois números e informe qual deles é o maior.

    ```javascript
    let numero1 = 10; // exemplo
    let numero2 = 5; // exemplo
    let maior = numero1 > numero2 ? numero1 : numero2;
    console.log(maior);
    ```

10. Crie um programa utilizando operador `try-catch-finally` que: tente converter uma string em um número, e caso ocorra um erro, informe uma mensagem amigável ao usuário.

    ```javascript
    let texto = "123abc"; // exemplo
    let numero;

    try {
    numero = Number(texto);
    if (isNaN(numero)) {
        throw new Error("O texto não pode ser convertido em número");
    }
    console.log(`O número é ${numero}`);
    } catch (error) {
    console.log(error.message);
    } finally {
    console.log("Fim da execução do programa");
    }
    ```

11. Crie um programa utilizando operador `try-catch-finally` que: tente acessar uma propriedade de um objeto que não existe, e caso ocorra um erro, informe uma mensagem amigável ao usuário.

    ```javascript
    let objeto = {nome: "João", idade: 30}; // exemplo
    let propriedade = "endereco";
    let valor;

    try {
    valor = objeto[propriedade];
    if (!valor) {
        throw new Error(`A propriedade ${propriedade} não existe no objeto`);
    }
    console.log(`O valor da propriedade é ${valor}`);
    } catch (error) {
    console.log(error.message);
    } finally {
    console.log("Fim da execução do programa");
    }
    ```

12. Crie um programa utilizando operador `try-catch-finally` que: tente dividir um número por zero, e caso ocorra um erro, informe uma mensagem amigável ao usuário.

    ```javascript
    let numero = 10; // exemplo
    let divisor = 0;
    let resultado;

    try {
    resultado = numero / divisor;
    console.log(`O resultado da divisão é ${resultado}`);
    } catch (error) {
    console.log("Ocorreu um erro ao tentar dividir o número:", error.message);
    } finally {
    console.log("Fim da execução do programa");
    }
    ```

#### Resposta Estruturas de repetição

1. Crie um programa utilizando a estrutura `for` que: exiba no console os números de 1 a 10.

    ```javascript
    for (let i = 1; i <= 10; i++) {
    console.log(i);
    }
    ```

2. Crie um programa  utilizando a estrutura `for` que: exiba no console os números pares de 1 a 20.

    ```javascript
    for (let i = 2; i <= 20; i += 2) {
    console.log(i);
    }
    ```

3. Crie um programa utilizando a estrutura `for` que: exiba no console os números de 50 a 1 em ordem decrescente, pulando de 5 em 5.

    ```javascript
    for (let i = 50; i >= 1; i -= 5) {
    console.log(i);
    }
    ```

4. Crie um programa utilizando a estrutura `while` que: exiba no console a soma dos números de 1 a 10.

    ```javascript
    let i = 1;
    let soma = 0;

    while (i <= 10) {
    soma += i;
    i++;
    }

    console.log(`A soma dos números de 1 a 10 é ${soma}`);
    ```

5. Crie um programa utilizando a estrutura `while` que: exiba no console os números ímpares de 1 a 20.

    ```javascript
    let i = 1;

    while (i <= 20) {
    if (i % 2 !== 0) {
        console.log(i);
    }
    i++;
    }
    ```
