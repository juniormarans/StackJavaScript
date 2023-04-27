## Conceitos Básicos

---

#### Como Rodar Um Código JavaScript

Escolha um ambiente para rodar seu código JavaScript. Existem várias opções para rodar um código JavaScript, dependendo do seu propósito. Algumas opções incluem:

- Usar o console do navegador: Para rodar código JavaScript no navegador, abra o console de desenvolvedor pressionando F12 e selecione a guia "Console". Digite seu código JavaScript diretamente no console e pressione Enter para rodar.
- Usar o Node.js: O Node.js é uma plataforma para rodar código JavaScript no lado do servidor. Para usar o Node.js, você precisa instalar o software primeiro.
- Usar um ambiente de desenvolvimento integrado (IDE): Existem muitos IDEs disponíveis para programação em JavaScript, como Visual Studio Code, Atom, Sublime Text, etc. Eles têm recursos avançados de depuração e autocompletar.

##### Utilizando o console do navegador

Passo 1: Crie um arquivo HTML
Crie um novo arquivo HTML em qualquer editor de texto. Cole o seguinte código HTML no arquivo:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu tutorial JavaScript</title>
</head>
<body>
    <h1>Meu tutorial JavaScript</h1>
    <script>
        // Seu código JavaScript aqui
    </script>
</body>
</html>
```

Salve o arquivo com o nome descritivo do que ele faz, por exemplo "saudacao.html".

Passo 2: Adicione seu código JavaScript
dentro da tag `<script>` no arquivo HTML, adicione seu código JavaScript. Por exemplo, o seguinte código exibe um alerta na tela:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu tutorial JavaScript</title>
</head>
<body>
    <h1>Meu tutorial JavaScript</h1>
    <script>
        console.log("Olá, mundo!");
    </script>
</body>
</html>
```

Salve o arquivo.

Passo 3: Abra o arquivo HTML no navegador
Abra o arquivo HTML no navegador, clicando duas vezes no arquivo, arrastando e soltando sobre um navegador ou usando o menu "Abrir arquivo" do navegador. O código JavaScript será executado automaticamente.

#### executar JavaScript com o Node.js

Passo 1: Abra o terminal do seu sistema operacional.

Passo 2: Navegue até o diretório onde o seu arquivo JavaScript está localizado usando o comando `cd`.

Por exemplo, se o seu arquivo está na pasta `Documentos` dentro do diretório pessoal do seu usuário, você pode navegar até lá com o seguinte comando:

```bash
cd ~/Documentos
```

Passo 3: Execute o código JavaScript usando o comando `node` seguido do nome do arquivo.

Por exemplo, se o seu arquivo se chama `meuCodigo.js`, o comando para executá-lo seria:

```bash
node meuCodigo.js
```

Passo 4: O resultado da execução do código será exibido no terminal.

Se o seu código tem saída de dados usando `console.log`, ela será exibida no terminal após a execução do comando.

Por exemplo, se o seu código contém o seguinte comando:

```javascript
console.log("Hello, world!");
```

A saída será exibida no terminal assim que o comando `node meuCodigo.js` for executado:

```bash
Hello, world!
```

Pronto! Agora você já sabe como executar um código JavaScript com o Node.js. É importante lembrar que, para usar módulos externos em seu código, você precisa instalar as dependências com o gerenciador de pacotes do Node.js, o `npm`.

### Tipos de Variáveis em JavaScript

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

#### Escopo de Variáveis em JavaScript

O escopo de variáveis em JavaScript define a visibilidade de uma variável dentro de um determinado bloco de código. Em outras palavras, o escopo determina onde a variável pode ser acessada e modificada dentro do programa.

Existem dois tipos de escopo de variáveis em JavaScript: escopo global e escopo local.

O escopo global é o escopo mais amplo, onde as variáveis são definidas fora de qualquer bloco de código, como funções ou loops. Variáveis globais podem ser acessadas e modificadas em qualquer parte do programa, o que pode levar a erros difíceis de depurar. Aqui está um exemplo de variável global:

##### Escopo Global

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

##### Escopo Local

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

##### Exemplo com Escopo global e local

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

### Palavras Reservadas

**Palavras reservadas** em JavaScript são termos que possuem significado especial na linguagem e que não podem ser utilizados como identificadores (nomes de variáveis, funções ou outros elementos do código). Essas palavras são reservadas para fins específicos, como estruturas de controle, declaração de variáveis, declaração de funções, entre outros.

As palavras reservadas em JavaScript incluem:

- `break`: usado para interromper a execução de um loop ou switch statement.
- `case`: usado em conjunto com o switch statement para avaliar uma expressão e executar o bloco de código correspondente.
- `catch`: usado em conjunto com o try statement para capturar exceções lançadas pelo bloco de código.
- `class`: introduz uma declaração de classe.
- `const`: define uma constante com um valor que não pode ser alterado.
- `continue`: usado para pular uma iteração de um loop.
- `debugger`: interrompe a execução do código para fins de depuração.
- `default`: usado em conjunto com o switch statement para executar um bloco de código padrão quando nenhuma das condições é atendida.
- `delete`: exclui uma propriedade de um objeto.
- `do`: inicia um loop do/while.
- `else`: usado em conjunto com um if statement para executar um bloco de código alternativo quando a condição não é atendida.
- `export`: exporta uma variável, função ou objeto de um módulo.
- `extends`: especifica uma classe pai para uma classe filho.
- `false`: representa o valor lógico falso.
- `finally`: usado em conjunto com o try statement para executar um bloco de código após a conclusão do bloco try/catch.
- `for`: inicia um loop for.
- `function`: define uma função.
- `if`: inicia um bloco de código condicional.
- `import`: importa uma variável, função ou objeto de outro módulo.
- `in`: usado para verificar se uma propriedade existe em um objeto.
- `instanceof`: usado para verificar se um objeto é uma instância de uma classe.
- `let`: define uma variável com escopo de bloco.
- `new`: cria uma nova instância de um objeto.
- `null`: representa um valor nulo.
- `return`: especifica o valor de retorno de uma função.
- `super`: chama um método na classe pai.
- `switch`: inicia um bloco de código de seleção múltipla.
- `this`: refere-se ao objeto atual.
- `throw`: lança uma exceção.
- `true`: representa o valor lógico verdadeiro.
- `try`: inicia um bloco de código que pode gerar exceções.
- `typeof`: retorna o tipo de uma variável ou expressão.
- `var`: define uma variável com escopo de função.
- `void`: retorna um valor vazio.
- `while`: inicia um loop while.
- `with`: adiciona um objeto ao escopo atual.

Ao criar código JavaScript, é importante evitar o uso de `palavras reservadas` como identificadores, pois isso pode causar erros e tornar o código mais difícil de entender.

### Tipos de dados em JavaScript

JavaScript possui vários tipos de dados, como números, strings, booleanos, arrays, objetos e muito mais. Cada tipo de dado é usado para representar um conjunto específico de valores e tem um conjunto específico de operações que podem ser realizadas com ele.

#### Tipos de dados primitivos

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

#### Tipos de dados não primitivos

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

### Formatação e Indentação de Código em JavaScript

A **formatação** e **indentação** de código em JavaScript são importantes para a **legibilidade** e **manutenção** do código. Quando o código é organizado de maneira consistente e estruturada, é mais fácil para outros desenvolvedores entenderem o código e fazerem alterações.

#### Princípios de Formatação de Código em JavaScript

Os **princípios de formatação** de código em JavaScript incluem a **consistência**, a **clareza** e a **simplicidade**. A **consistência** é importante para que o código seja organizado de maneira previsível e fácil de entender. Isso pode ser alcançado usando um conjunto de regras de formatação que se aplicam a todo o código. A **clareza** refere-se à legibilidade do código, ou seja, a facilidade de compreender o que cada instrução faz. Isso pode ser alcançado usando nomes de variáveis descritivos, comentários claros e código bem organizado. A **simplicidade** envolve manter o código o mais simples possível, eliminando instruções desnecessárias e mantendo o código fácil de entender.

A escolha de **nomes descritivos** para variáveis em JavaScript é uma prática importante que ajuda a tornar o código mais **legível** e **fácil** de entender. Uma **variável descritiva** é aquela que possui um nome que descreve claramente o que a variável representa ou armazena.

A seguir, estão alguns exemplos de **variáveis descritivas** em JavaScript, demonstrando como a escolha de nomes pode ser significativa para a compreensão do código:

```javascript
// Exemplo 1: Variáveis descritivas para armazenar dados do usuário
let nomeUsuario = "Maria"; // variável para armazenar o nome do usuário
let idadeUsuario = 30; // variável para armazenar a idade do usuário
let emailUsuario = "maria@email.com"; // variável para armazenar o e-mail do usuário
```

No exemplo acima, os nomes das **variáveis** são claramente **descritivos** e indicam o tipo de informação que cada variável está armazenando. Isso torna o código mais fácil de entender, especialmente para outros desenvolvedores que podem precisar trabalhar com esse código.

```javascript
// Exemplo 2: Variáveis descritivas para cálculos matemáticos
let valorTotal = 50.00; // variável para armazenar o valor total da compra
let quantidadeProdutos = 3; // variável para armazenar a quantidade de produtos comprados
let valorFrete = 10.00; // variável para armazenar o valor do frete

let valorFinal = valorTotal + (quantidadeProdutos * 5) + valorFrete; // cálculo do valor final
```

Nesse exemplo, os **nomes das variáveis** refletem as informações que elas representam, tornando o código mais **fácil de entender**. Além disso, a escolha de nomes **descritivos** ajuda a **prevenir erros**, como a utilização incorreta de uma variável.

Em resumo, a escolha de nomes descritivos para variáveis em JavaScript é uma `prática importante` que pode ajudar a tornar o código mais `legível` e `fácil` de entender. Ao escolher `nomes descritivos`, os desenvolvedores podem facilitar o processo de `leitura` e `manutenção` do código, bem como prevenir erros de programação.

#### Princípios de Indentação de Código em JavaScript

Os princípios de `indentação` de código em JavaScript incluem a `hierarquia` e a `clareza`. A `hierarquia` refere-se à estruturação do código em blocos, funções e outras estruturas. Cada `nível da hierarquia` deve ser indentado para que seja fácil de entender a estrutura do código. A `clareza` refere-se à legibilidade do código, ou seja, a facilidade de entender a relação entre as instruções. Isso pode ser alcançado usando uma `indentação` consistente e adequada, que torne claro quais instruções pertencem a quais blocos de código.

##### Exemplos Práticos

Aqui estão alguns exemplos práticos de formatação e indentação de código em JavaScript:

###### Exemplo 1: Formatação de código

```javascript
// código sem formatação
let a=2;let b=3;let c=a+b;console.log(c);

// código com formatação e usando nomes de variáveis descritivos
let valorInicial = 2;
let valorRecebido = 3;
let valorTotal = valorInicial + valorRecebido;
console.log(valorTotal);
```

O código formatado usando nomes de variáveis descritivos é muito mais fácil de ler e entender, com instruções separadas por linhas e com espaçamento adequado.

###### Exemplo 2: Indentação de código

```javascript
// código sem indentação
if (saldo == 0) {
let emprestimo = 2;
if (emprestimo == 2) {
let divida = 3;
console.log(divida);
}
}

// código com indentação
if (saldo == 0) {
  let emprestimo = 2;
  if (emprestimo == 2) {
    let divida = 3;
    console.log(divida);
  }
}
```

O `código indentado` torna a hierarquia mais clara, indicando qual bloco de código pertence a qual nível da hierarquia.

A `formatação` e `indentação` adequadas de código são importantes para que o código seja mais `legível` e `fácil` de entender. Quando o código é organizado de maneira `consistente` e `estruturada`, é mais fácil para outros desenvolvedores entenderem o código e fazerem alterações. Além disso, a `formatação` e a `indentação` adequadas podem ajudar a prevenir erros de sintaxe e tornar o processo de depuração mais fácil. Em resumo, a `formatação` e a `indentação` adequadas são fundamentais para um código JavaScript de qualidade.

#### Tipos de comentários em JavaScript e sua aplicação

`Comentários` são uma parte importante da programação em JavaScript. Eles ajudam os desenvolvedores a entender o código e a manter a `documentação` do projeto. Existem dois tipos principais de comentários em JavaScript: `comentários de uma linha` e `comentários de várias linhas`. Além disso, existem comentários especiais chamados `JSDoc` que são usados para documentar o código e gerar documentação automática.

##### Comentários de uma linha

`Comentários de uma linha` são usados para incluir anotações curtas em uma única linha de código. Eles começam com `//` e são ignorados pelo interpretador JavaScript. Os comentários de uma linha são usados para explicar o que o código faz, ou para deixar uma nota para outro desenvolvedor. Veja o exemplo abaixo:

```javascript
// Define uma variável chamada 'idade' com o valor de 20
let idade = 20;
```

##### Comentários de várias linhas

`Comentários de várias linhas` são usados para comentar blocos de código ou para incluir anotações mais longas. Eles começam com `/*` e terminam com `*/`. Comentários de várias linhas são úteis para explicar em mais detalhes como o código funciona. Veja o exemplo abaixo:

```javascript
/*
Esta função calcula o cubo de um número.
Para calcular o cubo, o número é multiplicado por si mesmo três vezes.
*/
function calcularCubo(numero) {
  return numero * numero * numero;
}
```

##### Comentários JSDoc

`Comentários JSDoc` são uma forma especializada de comentários em JavaScript que são usados para documentar o código. Eles são usados para documentar funções, variáveis, parâmetros e valores de retorno. Os comentários JSDoc começam com `/**` e terminam com `*/`. Os comentários JSDoc possuem uma sintaxe específica que permite especificar informações sobre as funções, variáveis e outros elementos do código.

Veja o exemplo abaixo:

```javascript
/**
 * Calcula a média de um conjunto de números.
 *
 * @param {number[]} numeros - O conjunto de números para calcular a média.
 * @returns {number} A média dos números fornecidos.
 */
function calcularMedia(numeros) {
  const total = numeros.reduce((soma, numero) => soma + numero, 0);
  return total / numeros.length;
}
```

O exemplo acima usa comentários JSDoc para documentar uma função que calcula a média de um conjunto de números. O comentário começa com `/**` e termina com `*/`. Os comentários JSDoc incluem informações sobre os parâmetros da função (`@param`) e o valor de retorno (`@returns`). Essas informações são usadas por ferramentas de documentação, como o JSDoc ou o DocumentJS, para gerar documentação automatizada para o código.

`Comentários` são uma parte importante da programação em JavaScript. Eles ajudam os desenvolvedores a entender o código e a manter a documentação do projeto. Existem dois tipos principais de comentários em JavaScript: `comentários de uma linha` e `comentários de várias linhas`. Além disso, existem comentários especiais chamados `comentários JSDoc`.

### Operadores JavaScript

Introdução

Operadores em JavaScript são usados para realizar operações matemáticas, lógicas e de atribuição em variáveis. Eles são ferramentas essenciais para escrever um código limpo e eficiente.

#### Operadores Aritméticos

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

##### Operador de Adição (+)

O operador de adição (`+`) é usado para adicionar dois valores.

Exemplo:

```javascript
let valor1 = 5;
let valor2 = 2;
let resultado = valor1 + valor2;
console.log(resultado); // Saída: 7
```

Neste exemplo, `valor1` e `valor2` são adicionados através do operador `+`, resultando em `resultado` com valor 7.

##### Operador de Subtração (-)

O operador de subtração (`-`) é usado para subtrair um valor de outro.

Exemplo:

```javascript
let valor1 = 5;
let valor2 = 2;
let resultado = valor1 - valor2;
console.log(resultado); // Saída: 3
```

Neste exemplo, `valor2` é subtraído de `valor1` através do operador `-`, resultando em `resultado` com valor 3.

##### Operador de Multiplicação (*)

O operador de multiplicação (`*`) é usado para multiplicar dois valores.

Exemplo:

```javascript
let valor1 = 5;
let valor2 = 2;
let resultado = valor1 * valor2;
console.log(resultado); // Saída: 10
```

Neste exemplo, `valor1` e `valor2` são multiplicados através do operador `*`, resultando em `resultado` com valor 10.

##### Operador de Divisão (/)

O operador de divisão (`/`) é usado para dividir um valor por outro.

Exemplo:

```javascript
let valor1 = 6;
let valor2 = 3;
let resultado = valor1 / valor2;
console.log(resultado); // Saída: 2
```

Neste exemplo, `valor1` é dividido por `valor2` através do operador `/`, resultando em `resultado` com valor 2.

##### Operador de Resto (%)

O operador de resto (`%`) é usado para obter o resto da divisão de um valor por outro.

Exemplo:

```javascript
let valor1 = 7;
let valor2 = 2;
let resultado = valor1 % valor2;
console.log(resultado); // Saída: 1
```

Neste exemplo, `valor1` é dividido por `valor2` através do operador `%`, resultando em `resultado` com valor 1, que é o resto da divisão.

##### Operador de Exponenciação (**)

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

#### Precedência de Operadores Aritméticos

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

#### Operadores de Atribuição em JavaScript

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

##### Atribuição Simples

O operador de atribuição simples (`=`) é utilizado para atribuir um valor a uma variável.

Exemplo:

```javascript
let valor = 10;
```

##### Atribuição com Adição

O operador de atribuição com adição (`+=`) é utilizado para somar um valor a uma variável.

Exemplo:

```javascript
let valor = 10;
valor += 5; // valor = 15
```

##### Atribuição com Subtração

O operador de atribuição com subtração (`-=`) é utilizado para subtrair um valor de uma variável.

Exemplo:

```javascript
let valor = 10;
valor -= 3; // valor = 7
```

##### Atribuição com Multiplicação

O operador de atribuição com multiplicação (`*=`) é utilizado para multiplicar uma variável por um valor.

Exemplo:

```javascript
let valor = 10;
valor *= 2; // valor = 20
```

##### Atribuição com Divisão

O operador de atribuição com divisão (`/=`) é utilizado para dividir uma variável por um valor.

Exemplo:

```javascript
let valor = 10;
valor /= 4; // valor = 2.5
```

##### Atribuição com Resto da Divisão

O operador de atribuição com resto da divisão (`%=`) é utilizado para obter o resto da divisão de uma variável por um valor.

Exemplo:

```javascript
let valor = 10;
valor %= 3; // valor = 1
```

##### Atribuição com Exponenciação

O operador de atribuição com exponenciação (`**=`) é utilizado para elevar uma variável a uma potência.

Exemplo:

```javascript
let valor = 2;
valor **= 3; // valor = 8
```

##### Atribuição com Deslocamento à Esquerda

O operador de atribuição com deslocamento à esquerda (`<<=`) é utilizado para deslocar os bits de uma variável para a esquerda.

Exemplo:

```javascript
let valor = 10;
valor <<= 2; // valor = 40
```

##### Atribuição com Deslocamento à Direita

O operador de atribuição com deslocamento à direita (`>>=`) é utilizado para deslocar os bits de uma variável para a direita.

Exemplo:

```javascript
let valor = 10;
valor >>= 1; // valor = 5
```

##### Atribuição com Deslocamento Sem Sinal

O operador de atribuição com deslocamento sem sinal (`>>>=`) é utilizado para deslocar os bits de uma variável para a direita, preenchendo os bits mais significativos com zero.

Exemplo:

```javascript
let valor = -10;
valor >>>= 1; // valor = 2147483643
```

##### Atribuição com AND Bit a Bit

O operador de atribuição com AND bit a bit (`&=`) é utilizado para realizar uma operação AND bit a bit entre uma variável e um valor.

Exemplo:

```javascript
let valor = 10;
valor &= 3; // valor = 2
```

#### Operadores de Comparação

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

##### Igualdade (==)

O operador de igualdade (`==`) é utilizado para comparar se dois valores são iguais. Ele realiza uma conversão de tipo antes da comparação, o que pode levar a resultados inesperados em alguns casos.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 == valor2); // true
```

Neste exemplo, o operador `==` compara se `valor1` é igual a `valor2`, mesmo que `valor2` seja uma string. Como o valor numérico da string "10" é igual a 10, a comparação retorna verdadeiro.

Para evitar resultados inesperados como este, é recomendado utilizar o operador de igualdade estrita (`===`) que não realiza conversão de tipo antes da comparação.

##### Igualdade Estrita (===)

O operador de igualdade estrita (`===`) é utilizado para comparar se dois valores são iguais, sem realizar conversão de tipo antes da comparação. Ele leva em consideração tanto o valor quanto o tipo dos valores.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 === valor2); // false
```

Neste exemplo, o operador `===` compara se `valor1` é igual a `valor2`, levando em consideração o tipo dos valores. Como `valor1` é do tipo `number` e `valor2` é do tipo `string`, a comparação retorna falso.

##### Desigualdade (!=)

O operador de desigualdade (`!=`) é utilizado para comparar se dois valores são diferentes. Assim como o operador de igualdade, ele realiza uma conversão de tipo antes da comparação.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 != valor2); // false
```

Neste exemplo, o operador `!=` compara se `valor1` é diferente de `valor2`. Como o valor numérico da string "10" é igual a 10, a comparação retorna falso.

##### Desigualdade Estrita (!==)

O operador de desigualdade estrita (`!==`) é utilizado para comparar se dois valores são diferentes, sem realizar conversão de tipo antes da comparação. Ele leva em consideração tanto o valor quanto o tipo dos valores.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = "10";
console.log(valor1 !== valor2); // true
```

Neste exemplo, o operador `!==` compara se `valor1` é diferente de `valor2`, levando em consideração o tipo dos valores. Como `valor1` é do tipo `number` e `valor2` é do tipo `string`, a comparação retorna verdadeiro.

##### Maior que (>)

O operador de maior que (`>`) é utilizado para comparar se um valor é maior do que outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 > valor2); // true
```

Neste exemplo, o operador `>` compara se `valor1` é maior do que `valor2`, retornando verdadeiro.

##### Menor que (<)

O operador de menor que (`<`) é utilizado para comparar se um valor é menor do que outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 < valor2); // false
```

Neste exemplo, o operador `<` compara se `valor1` é menor do que `valor2`, retornando falso.

##### Maior ou igual que (>=)

O operador de maior ou igual que (`>=`) é utilizado para comparar se um valor é maior ou igual a outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 >= valor2); // true
```

Neste exemplo, o operador `>=` compara se `valor1` é maior ou igual a `valor2`, retornando verdadeiro.

##### Menor ou igual que (<=)

O operador de menor ou igual que (`<=`) é utilizado para comparar se um valor é menor ou igual a outro.

Exemplo:

```javascript
let valor1 = 10;
let valor2 = 5;
console.log(valor1 <= valor2); // false
```

Neste exemplo, o operador `<=` compara se `valor1` é menor ou igual a `valor2`, retornando falso.

##### Operador Ternário (?)

O operador ternário (`?`) é utilizado para realizar uma operação condicional, retornando um valor de acordo com uma condição. Ele é uma forma simplificada de escrever uma estrutura condicional if-else.

Exemplo:

```javascript
let idade = 18;
let podeDirigir = (idade >= 18) ? "Pode dirigir" : "Não pode dirigir";
console.log(podeDirigir); // "Pode dirigir"
```

Neste exemplo, o operador ternário `?` verifica se a `idade` é maior ou igual a 18. Se for, retorna a string "Pode dirigir". Caso contrário, retorna a string "Não pode dirigir".

Os operadores de comparação em JavaScript são fundamentais para a criação de expressões condicionais e tomada de decisões em um programa. É importante utilizá-los corretamente e de acordo com as boas práticas de código, visando garantir a legibilidade e manutenção do código.

#### Operadores Lógicos

| Operador | Descrição                                              |
|----------|--------------------------------------------------------|
| &&       | Operador "E". Retorna verdadeiro se ambos os operandos são verdadeiros. |
| \|\|      | Operador "OU". Retorna verdadeiro se um dos operandos é verdadeiro. |
| !        | Operador "NÃO". Inverte o valor do operando. Retorna verdadeiro se o operando é falso e vice-versa. |

E aqui estão exemplos de uso de cada um desses operadores:

##### Operador "E" (&&)

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

##### Operador "OU" (\|\|)

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

##### Operador "NÃO" (!)

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

#### Operadores de Incremento e Decremento

Os operadores de incremento e decremento em JavaScript permitem que você adicione ou subtraia um valor de uma variável em uma unidade, são eles:

| Operador | Descrição |
| --- | --- |
| ++ | Operador de incremento, adiciona 1 ao valor da variável |
| -- | Operador de decremento, subtrai 1 do valor da variável |

##### Operador de Incremento (++)

O operador de incremento (`++`) é usado para adicionar 1 ao valor de uma variável.

Exemplo:

```javascript
let valor1 = 5;
valor1++;
console.log(valor1); // Saída: 6
```

Neste exemplo, o valor de `valor1` é incrementado em 1 através do operador `++`.

##### Operador de Decremento (--)

O operador de decremento (`--`) é usado para subtrair 1 do valor de uma variável.

Exemplo:

```javascript
let valor1 = 5;
valor1--;
console.log(valor1); // Saída: 4
```

Neste exemplo, o valor de `valor1` é decrementado em 1 através do operador `--`.

##### Utilizando Operadores em Expressões

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
Os operadores em JavaScript são fundamentais para escrever um código limpo e eficiente. Eles permitem que você realize operações matemáticas, lógicas e de atribuição em variáveis. Lembre-se, o uso de nomes descritivos para as variáveis ajuda a tornar o código mais legível e fácil de entender.

### Exercicios de fixação

1. Crie um programa que verifique se um número é par ou ímpar e imprima na tela.

2. Crie um programa que verifique se um número é positivo, negativo ou zero e imprima na tela.

3. Crie um programa que calcule a área de um triângulo com base e altura informadas pelo usuário e imprima na tela.

4. Crie um programa que calcule o perímetro de um quadrado com lado informado pelo usuário e imprima na tela.

5. Crie um programa que concatene duas strings informadas pelo usuário e imprima na tela.

Espero que esses exercícios sejam úteis para você praticar suas habilidades em JavaScript com declaração de variaveis, operadores lógicos, comparação, atribuição e aritméticos!

### Respostas exercicios de fixação

1. Crie um programa que verifique se um número é par ou ímpar e imprima na tela.

    ```javascript
    let numero = 7;
    let resto = numero % 2;
    let resultado = resto === 0 && 'par' || 'ímpar';
    console.log(resultado);
    ```

2. Crie um programa que verifique se um número é positivo, negativo ou zero e imprima na tela.

    ```javascript
    let numero = 5;
    let resultado = numero > 0 && 'positivo' || numero < 0 && 'negativo' || 'zero';
    console.log(resultado);
    ```

3. Crie um programa que calcule a área de um triângulo com base e altura informadas pelo usuário e imprima na tela.

    ```javascript
    let base = 5;
    let altura = 10;
    let area = (base * altura) / 2;
    console.log(area);
    ```

4. Crie um programa que calcule o perímetro de um quadrado com lado informado pelo usuário e imprima na tela.

    ```javascript
    let lado = 5;
    let perimetro = lado * 4;
    console.log(perimetro);
    ```

5. Crie um programa que concatene duas strings informadas pelo usuário e imprima na tela.

    ```javascript
    let string1 = 'Olá, ';
    let string2 = 'mundo!';
    let resultado = string1 + string2;
    console.log(resultado);
    ```

Espero que esses exercícios sejam úteis para você praticar suas habilidades em JavaScript com declaração de variaveis, operadores lógicos, comparação, atribuição e aritméticos!
