# Exercicios de fixação

## Estruturas de decisão

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

## Estruturas de repetição

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
