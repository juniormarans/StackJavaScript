# Operadores JavaScript

Introdução

Operadores em JavaScript são usados para realizar operações matemáticas, lógicas e de atribuição em variáveis. Eles são ferramentas essenciais para escrever um código limpo e eficiente.

## Operadores Aritméticos

Os operadores aritméticos em JavaScript são utilizados para realizar operações matemáticas em variáveis. Abaixo segue uma lista dos operadores aritméticos em JavaScript:

| Operador | Descrição |
| --- | --- |
| + | Operador de adição |
| - | Operador de subtração |
| * | Operador de multiplicação |
| / | Operador de divisão |
| % | Operador de resto |
| ** | Operador de exponenciação |

E aqui estão exemplos de uso de cada um desses operadores:

### Operador de Adição (+)

O operador de adição (`+`) é usado para adicionar dois valores.

Exemplo:

```javascript
let valor1 = 5;
let valor2 = 2;
let resultado = valor1 + valor2;
console.log(resultado); // Saída: 7
```

Neste exemplo, `valor1` e `valor2` são adicionados através do operador `+`, resultando em `resultado` com valor 7.

### Operador de Subtração (-)

O operador de subtração (`-`) é usado para subtrair um valor de outro.

Exemplo:

```javascript
let valor1 = 5;
let valor2 = 2;
let resultado = valor1 - valor2;
console.log(resultado); // Saída: 3
```

Neste exemplo, `valor2` é subtraído de `valor1` através do operador `-`, resultando em `resultado` com valor 3.

### Operador de Multiplicação (*)

O operador de multiplicação (`*`) é usado para multiplicar dois valores.

Exemplo:

```javascript
let valor1 = 5;
let valor2 = 2;
let resultado = valor1 * valor2;
console.log(resultado); // Saída: 10
```

Neste exemplo, `valor1` e `valor2` são multiplicados através do operador `*`, resultando em `resultado` com valor 10.

### Operador de Divisão (/)

O operador de divisão (`/`) é usado para dividir um valor por outro.

Exemplo:

```javascript
let valor1 = 6;
let valor2 = 3;
let resultado = valor1 / valor2;
console.log(resultado); // Saída: 2
```

Neste exemplo, `valor1` é dividido por `valor2` através do operador `/`, resultando em `resultado` com valor 2.

### Operador de Resto (%)

O operador de resto (`%`) é usado para obter o resto da divisão de um valor por outro.

Exemplo:

```javascript
let valor1 = 7;
let valor2 = 2;
let resultado = valor1 % valor2;
console.log(resultado); // Saída: 1
```

Neste exemplo, `valor1` é dividido por `valor2` através do operador `%`, resultando em `resultado` com valor 1, que é o resto da divisão.

### Operador de Exponenciação (**)

O operador de exponenciação (`**`) é usado para elevar um valor a uma potência.

Exemplo:

```javascript
let valor1 = 2;
let valor2 = 3;
let resultado = valor1 ** valor2;
console.log(resultado); // Saída: 8
```

Neste exemplo, `valor1` é elevado à potência de `valor2` através do operador `**`, resultando em `resultado` com valor 8.

Os operadores aritméticos são muito úteis em JavaScript e podem ser usados em diversas situações para realizar cálculos. É importante, no entanto, usá-los com cuidado para evitar erros ou comportamentos inesper

## Precedência de Operadores Aritméticos

Os operadores aritméticos têm uma precedência definida em JavaScript, o que significa que algumas operações serão realizadas antes de outras, mesmo que não estejam entre parênteses. Abaixo segue uma tabela com a ordem de precedência dos operadores aritméticos em JavaScript:

| Operador           | Descrição                                           |
| ------------------ | --------------------------------------------------- |
| **                 | Exponenciação                                       |
| * / %              | Multiplicação, divisão e resto da divisão           |
| + -                | Adição e subtração                                  |

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
let valor3 = 2;

let resultado = valor1 + valor2 * valor3; // resultado = 20
```

Nesse exemplo, a multiplicação entre `valor2` e `valor3` é realizada primeiro, devido à sua maior precedência em relação à adição entre `valor1` e o resultado da multiplicação.

É importante lembrar que, se necessário, é possível alterar a ordem de precedência utilizando parênteses. Por exemplo, se quisermos que a adição seja realizada antes da multiplicação no exemplo anterior, podemos escrever da seguinte forma:

```javascript
let resultado = (valor1 + valor2) * valor3; // resultado = 30
```

Os operadores aritméticos em JavaScript são muito importantes para realizar cálculos matemáticos em variáveis. Além disso, entender a precedência dos operadores aritméticos é fundamental para escrever códigos corretos e eficientes. Por isso, é importante seguir as convenções de boas práticas de código, utilizar nomes descritivos para as variáveis e utilizar parênteses quando necessário para garantir a ordem correta de execução das operações.

Claro! Abaixo segue um exemplo de operadores de atribuição em JavaScript, com convenções de boas práticas de código.

## Operadores de Atribuição em JavaScript

Os operadores de atribuição em JavaScript são utilizados para atribuir valores a variáveis. Abaixo segue uma lista dos operadores de atribuição em JavaScript:

| Operador | Descrição                              |
| -------- | --------------------------------------|
| =        | Atribuição simples                     |
| +=       | Atribuição com adição                  |
| -=       | Atribuição com subtração               |
| *=       | Atribuição com multiplicação           |
| /=       | Atribuição com divisão                 |
| %=       | Atribuição com resto da divisão        |
| **=      | Atribuição com exponenciação           |
| <<=      | Atribuição com deslocamento à esquerda |
| >>=      | Atribuição com deslocamento à direita  |
| >>>=     | Atribuição com deslocamento sem sinal  |
| &=       | Atribuição com AND bit a bit           |
| ^=       | Atribuição com XOR bit a bit           |
| \|=      | Atribuição com OR bit a bit            |

### Atribuição Simples

O operador de atribuição simples (`=`) é utilizado para atribuir um valor a uma variável.

Exemplo:

```javascript
let valor = 10;
```

### Atribuição com Adição

O operador de atribuição com adição (`+=`) é utilizado para somar um valor a uma variável.

Exemplo:

```javascript
let valor = 10;
valor += 5; // valor = 15
```

### Atribuição com Subtração

O operador de atribuição com subtração (`-=`) é utilizado para subtrair um valor de uma variável.

Exemplo:

```javascript
let valor = 10;
valor -= 3; // valor = 7
```

### Atribuição com Multiplicação

O operador de atribuição com multiplicação (`*=`) é utilizado para multiplicar uma variável por um valor.

Exemplo:

```javascript
let valor = 10;
valor *= 2; // valor = 20
```

### Atribuição com Divisão

O operador de atribuição com divisão (`/=`) é utilizado para dividir uma variável por um valor.

Exemplo:

```javascript
let valor = 10;
valor /= 4; // valor = 2.5
```

### Atribuição com Resto da Divisão

O operador de atribuição com resto da divisão (`%=`) é utilizado para obter o resto da divisão de uma variável por um valor.

Exemplo:

```javascript
let valor = 10;
valor %= 3; // valor = 1
```

### Atribuição com Exponenciação

O operador de atribuição com exponenciação (`**=`) é utilizado para elevar uma variável a uma potência.

Exemplo:

```javascript
let valor = 2;
valor **= 3; // valor = 8
```

### Atribuição com Deslocamento à Esquerda

O operador de atribuição com deslocamento à esquerda (`<<=`) é utilizado para deslocar os bits de uma variável para a esquerda.

Exemplo:

```javascript
let valor = 10;
valor <<= 2; // valor = 40
```

### Atribuição com Deslocamento à Direita

O operador de atribuição com deslocamento à direita (`>>=`) é utilizado para deslocar os bits de uma variável para a direita.

Exemplo:

```javascript
let valor = 10;
valor >>= 1; // valor = 5
```

### Atribuição com Deslocamento Sem Sinal

O operador de atribuição com deslocamento sem sinal (`>>>=`) é utilizado para deslocar os bits de uma variável para a direita, preenchendo os bits mais significativos com zero.

Exemplo:

```javascript
let valor = -10;
valor >>>= 1; // valor = 2147483643
```

### Atribuição com AND Bit a Bit

O operador de atribuição com AND bit a bit (`&=`) é utilizado para realizar uma operação AND bit a bit entre uma variável e um valor.

Exemplo:

```javascript
let valor = 10;
valor &= 3; // valor = 2
```

## Operadores de Comparação

Os operadores de comparação em JavaScript permitem que você compare dois valores e verifique se eles são iguais ou diferentes, maiores ou menores que um determinado valor. Eles retornam um valor booleano (`true` ou `false`) dependendo do resultado da comparação.

Tabela com os operadores de comparação em JavaScript:

| Operador | Descrição                                              |
|----------|--------------------------------------------------------|
| ==       | Verifica se os valores são iguais, sem levar em conta o tipo de dado. |
| ===      | Verifica se os valores são iguais, levando em conta o tipo de dado. |
| !=       | Verifica se os valores são diferentes, sem levar em conta o tipo de dado. |
| !==      | Verifica se os valores são diferentes, levando em conta o tipo de dado. |
| >        | Verifica se o valor da esquerda é maior que o da direita. |
| <        | Verifica se o valor da esquerda é menor que o da direita. |
| >=       | Verifica se o valor da esquerda é maior ou igual ao da direita. |
| <=       | Verifica se o valor da esquerda é menor ou igual ao da direita. |

É importante lembrar que a utilização correta dos operadores de comparação em JavaScript é essencial para o bom funcionamento do programa e para evitar possíveis erros e bugs.

### Igualdade (==)

O operador de igualdade (`==`) é utilizado para comparar se dois valores são iguais. Ele realiza uma conversão de tipo antes da comparação, o que pode levar a resultados inesperados em alguns casos.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 == valor2); // true
```

Neste exemplo, o operador `==` compara se `valor1` é igual a `valor2`, mesmo que `valor2` seja uma string. Como o valor numérico da string "10" é igual a 10, a comparação retorna verdadeiro.

Para evitar resultados inesperados como este, é recomendado utilizar o operador de igualdade estrita (`===`) que não realiza conversão de tipo antes da comparação.

### Igualdade Estrita (===)

O operador de igualdade estrita (`===`) é utilizado para comparar se dois valores são iguais, sem realizar conversão de tipo antes da comparação. Ele leva em consideração tanto o valor quanto o tipo dos valores.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 === valor2); // false
```

Neste exemplo, o operador `===` compara se `valor1` é igual a `valor2`, levando em consideração o tipo dos valores. Como `valor1` é do tipo `number` e `valor2` é do tipo `string`, a comparação retorna falso.

### Desigualdade (!=)

O operador de desigualdade (`!=`) é utilizado para comparar se dois valores são diferentes. Assim como o operador de igualdade, ele realiza uma conversão de tipo antes da comparação.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 != valor2); // false
```

Neste exemplo, o operador `!=` compara se `valor1` é diferente de `valor2`. Como o valor numérico da string "10" é igual a 10, a comparação retorna falso.

### Desigualdade Estrita (!==)

O operador de desigualdade estrita (`!==`) é utilizado para comparar se dois valores são diferentes, sem realizar conversão de tipo antes da comparação. Ele leva em consideração tanto o valor quanto o tipo dos valores.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 !== valor2); // true
```

Neste exemplo, o operador `!==` compara se `valor1` é diferente de `valor2`, levando em consideração o tipo dos valores. Como `valor1` é do tipo `number` e `valor2` é do tipo `string`, a comparação retorna verdadeiro.

### Maior que (>)

O operador de maior que (`>`) é utilizado para comparar se um valor é maior do que outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 > valor2); // true
```

Neste exemplo, o operador `>` compara se `valor1` é maior do que `valor2`, retornando verdadeiro.

### Menor que (<)

O operador de menor que (`<`) é utilizado para comparar se um valor é menor do que outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 < valor2); // false
```

Neste exemplo, o operador `<` compara se `valor1` é menor do que `valor2`, retornando falso.

### Maior ou igual que (>=)

O operador de maior ou igual que (`>=`) é utilizado para comparar se um valor é maior ou igual a outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 >= valor2); // true
```

Neste exemplo, o operador `>=` compara se `valor1` é maior ou igual a `valor2`, retornando verdadeiro.

### Menor ou igual que (<=)

O operador de menor ou igual que (`<=`) é utilizado para comparar se um valor é menor ou igual a outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 <= valor2); // false
```

Neste exemplo, o operador `<=` compara se `valor1` é menor ou igual a `valor2`, retornando falso.

### Operador Ternário (?)

O operador ternário (`?`) é utilizado para realizar uma operação condicional, retornando um valor de acordo com uma condição. Ele é uma forma simplificada de escrever uma estrutura condicional if-else.

Exemplo:

```javascript
let idade = 18;
let podeDirigir = (idade >= 18) ? "Pode dirigir" : "Não pode dirigir";
console.log(podeDirigir); // "Pode dirigir"
```

Neste exemplo, o operador ternário `?` verifica se a `idade` é maior ou igual a 18. Se for, retorna a string "Pode dirigir". Caso contrário, retorna a string "Não pode dirigir".

Os operadores de comparação em JavaScript são fundamentais para a criação de expressões condicionais e tomada de decisões em um programa. É importante utilizá-los corretamente e de acordo com as boas práticas de código, visando garantir a legibilidade e manutenção do código.

## Operadores Lógicos

Claro, segue abaixo a tabela com os operadores lógicos em JavaScript:

| Operador | Descrição                                              |
|----------|--------------------------------------------------------|
| &&       | Operador "E". Retorna verdadeiro se ambos os operandos são verdadeiros. |
| \|\|      | Operador "OU". Retorna verdadeiro se um dos operandos é verdadeiro. |
| !        | Operador "NÃO". Inverte o valor do operando. Retorna verdadeiro se o operando é falso e vice-versa. |

E aqui estão exemplos de uso de cada um desses operadores:

### Operador "E" (&&)

O operador "E" (`&&`) é utilizado para avaliar se duas ou mais expressões são verdadeiras.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
if (valor1 > 5 && valor2 < 10) {
  console.log("valor1 é maior que 5 e valor2 é menor que 10");
}
```

Neste exemplo, o operador `&&` avalia se `valor1` é maior que 5 e se `valor2` é menor que 10. Se as duas condições forem verdadeiras, a mensagem "valor1 é maior que 5 e valor2 é menor que 10" é exibida no console.

### Operador "OU" (\|\|)

O operador "OU" (`||`) é utilizado para avaliar se pelo menos uma das expressões é verdadeira.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
if (valor1 > 10 || valor2 < 10) {
  console.log("Pelo menos uma das condições é verdadeira");
}
```

Neste exemplo, o operador `||` avalia se `valor1` é maior que 10 ou se `valor2` é menor que 10. Se pelo menos uma das condições for verdadeira, a mensagem "Pelo menos uma das condições é verdadeira" é exibida no console.

### Operador "NÃO" (!)

O operador "NÃO" (`!`) é utilizado para inverter o valor de uma expressão.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
if (!(valor1 < valor2)) {
  console.log("valor1 não é menor que valor2");
}
```

Neste exemplo, o operador `!` inverte o resultado da expressão `valor1 < valor2`, que seria falsa neste caso. Dessa forma, a mensagem "x não é menor que y" é exibida no console.

Os operadores lógicos em JavaScript são fundamentais para a criação de expressões condicionais mais complexas, que envolvem a avaliação de múltiplas condições. É importante utilizá-los corretamente e de acordo com as boas práticas de código, visando garantir a legibilidade e manutenção do código.

## Operadores de Incremento e Decremento

Os operadores de incremento e decremento em JavaScript permitem que você adicione ou subtraia um valor de uma variável em uma unidade, são eles:

| Operador | Descrição |
| --- | --- |
| ++ | Operador de incremento, adiciona 1 ao valor da variável |
| -- | Operador de decremento, subtrai 1 do valor da variável |

### Operador de Incremento (++)

O operador de incremento (`++`) é usado para adicionar 1 ao valor de uma variável.

Exemplo:

```javascript
let valor1 = 5;
valor1++;
console.log(valor1); // Saída: 6
```

Neste exemplo, o valor de `valor1` é incrementado em 1 através do operador `++`.

### Operador de Decremento (--)

O operador de decremento (`--`) é usado para subtrair 1 do valor de uma variável.

Exemplo:

```javascript
let valor1 = 5;
valor1--;
console.log(valor1); // Saída: 4
```

Neste exemplo, o valor de `valor1` é decrementado em 1 através do operador `--`.

### Utilizando Operadores em Expressões

Os operadores de incremento e decremento também podem ser usados em expressões.

Exemplo:

```javascript
let valor1 = 5;
let valor2 = valor1++ + 2;
console.log(valor2); // Saída: 7
console.log(valor1); // Saída: 6
```

Neste exemplo, o operador de incremento `++` é usado após a variável `valor1` na expressão `valor1++ + 2`. O valor de `valor1` é incrementado em 1, mas a adição é realizada antes do incremento, resultando em `valor2` com valor 7 e `valor1` com valor 6.

Os operadores de incremento e decremento são muito úteis em JavaScript e podem ser usados para facilitar a escrita de código e melhorar sua legibilidade. É importante, no entanto, usá-los com moderação e ter cuidado com seu uso em expressões mais complexas, para evitar erros ou comportamentos inesperados. Além disso, é importante seguir as convenções de boas práticas de código em relação à nomenclatura das variáveis e à clareza do código.

## Conclusão

Os operadores em JavaScript são fundamentais para escrever um código limpo e eficiente. Eles permitem que você realize operações matemáticas, lógicas e de atribuição em variáveis. Lembre-se, o uso de nomes descritivos para as variáveis ajuda a tornar o código mais legível e fácil de entender.
