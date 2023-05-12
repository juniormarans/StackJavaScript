## Conceitos Básicos

JavaScript é uma linguagem de programação de alto nível, dinâmica e interpretada, criada por Brendan Eich em 1995 enquanto trabalhava na Netscape Communications Corporation. Hoje em dia, ela é uma das linguagens mais populares do mundo e é amplamente utilizada para criar e manipular conteúdo dinâmico em páginas da web, permitindo que desenvolvedores adicionem interatividade a sites e aplicativos da web.

A linguagem JavaScript é baseada em objetos e é executada no lado do cliente, ou seja, no navegador do usuário. Ela é usada para criar animações, validar formulários, atualizar conteúdo dinamicamente e realizar diversas outras funcionalidades que melhoram a experiência do usuário na web. Além disso, JavaScript também é utilizada em outras áreas, como no desenvolvimento de aplicativos de desktop, servidores web e até mesmo na criação de jogos.

Apesar de sua origem estar associada ao desenvolvimento de páginas web, o JavaScript não é limitado a ser executado apenas em navegadores da web. Por exemplo, o Node.js é um ambiente de tempo de execução do JavaScript baseado em servidor, que permite que o código JavaScript seja executado no lado do servidor. O Node.js é capaz de executar código JavaScript sem a necessidade de um navegador da web, permitindo que os desenvolvedores criem aplicativos web completos no lado do servidor.

Além disso, o JavaScript também pode ser usado no desenvolvimento de aplicativos desktop e móveis por meio de tecnologias como Electron, React Native e Ionic.

Uma das vantagens do JavaScript é a sua sintaxe relativamente simples, o que torna mais fácil para iniciantes aprenderem. Ela também possui uma grande variedade de bibliotecas e frameworks disponíveis, que ajudam a simplificar o processo de desenvolvimento de aplicativos da web.

Em resumo, o JavaScript é uma linguagem de programação extremamente versátil e amplamente utilizada em diferentes áreas. Ela é executada no lado do cliente, mas também pode ser executada no lado do servidor e em outras plataformas. A linguagem possui uma sintaxe relativamente simples e muitas ferramentas disponíveis, o que a torna uma ótima escolha para iniciantes e desenvolvedores experientes.

---

### Como Rodar Um Código JavaScript

O interpretador de JavaScript é um programa que executa o código escrito na linguagem de programação JavaScript. Ele é responsável por analisar e interpretar o código fonte escrito em JavaScript, gerando uma representação interna do código que pode ser executada pelo computador. Existem algumas opções para rodar um código JavaScript, dependendo do seu propósito. Algumas opções incluem:

- Usar o console do navegador: Para rodar código JavaScript no navegador, abra o console de desenvolvedor pressionando F12 e selecione a guia "Console". Digite seu código JavaScript diretamente no console e pressione Enter para rodar.
- Usar o Node.js: O Node.js é uma plataforma para rodar código JavaScript no lado do servidor. Para usar o Node.js, você precisa instalar o software primeiro.
- Usar um ambiente de desenvolvimento integrado (IDE): Existem muitos IDEs disponíveis para programação em JavaScript, como Visual Studio Code, Atom, Sublime Text, etc. Eles têm recursos avançados de depuração e autocompletar.

#### Utilizando o console do navegador

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

#### Executando JavaScript com o Nodejs

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

### Sintaxe Javascript

A sintaxe do JavaScript é a estrutura e a ordem corretas que devem ser seguidas para escrever código em JavaScript. Algumas das principais características da sintaxe do JavaScript incluem:

1. Case sensitive: o JavaScript diferencia maiúsculas de minúsculas. Por exemplo, a variável "nome" é diferente da variável "Nome".

2. Espaço em branco: espaço em branco é um símbolo léxico que inclui caracteres de espaço, tabulação e quebra de linha. Eles são utilizados para melhorar a legibilidade do código e não afetam o comportamento do programa. Espaços em branco são ignorados pelo interpretador JavaScript.

3. Ponto-e-vírgula: é usado para indicar o final de uma instrução. Embora seja opcional em algumas situações, é recomendado usá-lo para evitar possíveis erros.

4. Comentários: o JavaScript suporta comentários de uma linha (iniciando com //) e comentários de várias linhas (iniciando com '/*' e terminando com '*/'). Os comentários são úteis para documentar o código e para desativar temporariamente partes do código.

5. Variáveis: as variáveis são usadas para armazenar valores que podem ser usados posteriormente no código. Elas são declaradas usando var, let ou const, seguido pelo nome da variável.

6. Constantes: constantes são valores que não mudam durante a execução do programa. Em JavaScript, é possível criar constantes utilizando a palavra reservada const. Elas devem ser declaradas e inicializadas ao mesmo tempo e não podem ter seu valor alterado posteriormente. Exemplo: const PI = 3.1415.

7. Tipos de dados: o JavaScript tem diferentes tipos de dados, como string, número, booleano, objeto, função e assim por diante.

8. Operadores: o JavaScript tem vários operadores, como aritméticos (+, -, *, /), de atribuição (=), de comparação (==, !=, <, >), lógicos (&&, ||) e assim por diante. Os operadores são usados para realizar cálculos e comparações.

9. Separadores: separadores são utilizados para separar elementos na linguagem. Em JavaScript, existem vários tipos de separadores, incluindo ; (ponto e vírgula), , (vírgula), () (parênteses), {} (chaves) e [] (colchetes).

10. : o JavaScript tem estruturas de controle, como if/else, switch, for, while e do/while, que são usadas para controlar o fluxo do programa.

Essas são algumas das principais características da sintaxe do JavaScript. É importante seguir as regras de sintaxe para garantir que o código seja executado corretamente. Além disso, é importante manter o código organizado e bem estruturado para facilitar a leitura e manutenção do mesmo.

### Espaço em branco

O espaço em branco (ou white space) em JavaScript refere-se a qualquer caractere em branco que aparece no código, como espaços, tabs e quebras de linha. Em outras palavras, é qualquer caractere que não seja visível quando o código é exibido na tela.

O espaço em branco é geralmente ignorado pelo interpretador de JavaScript, o que significa que ele não tem nenhum efeito no comportamento do código em si. Em vez disso, o espaço em branco é usado apenas para tornar o código mais legível para os programadores.

Por exemplo, o código abaixo tem a mesma funcionalidade, mas o segundo exemplo é mais legível devido ao uso de espaço em branco:

```javascript
let numero=5;
if(numero<10){
console.log("O número é menor que 10");
}
```

```javascript
let numero = 5;
if (numero < 10) {
  console.log("O número é menor que 10");
}
```

Em resumo, o espaço em branco em JavaScript é usado para melhorar a legibilidade do código e é ignorado pelo interpretador durante a execução do programa.

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

### Tipos de identificadores em JavaScript

Variáveis e constantes são elementos fundamentais em qualquer linguagem de programação, incluindo JavaScript. Variáveis são usadas para armazenar valores que podem ser alterados durante a execução do programa, enquanto as constantes são usadas para armazenar valores que não podem ser alterados.

As palavras-chave `var`, `let` e `const` são usadas em JavaScript para declarar identificadores que servem para armazenar valores. A partir da versão ES6 (ECMAScript 2015), foram introduzidas as palavras-chave `let` e `const`, que possuem escopo de bloco. Isso significa que uma variável declarada com `let` ou `const` só pode ser acessada dentro do bloco de código em que foi declarada. Um bloco de código é uma seção delimitada por chaves, como um loop, uma instrução if ou uma função. Esse recurso é importante para evitar problemas de conflito de nomes e para tornar o código mais seguro e previsível.

A diferença entre `let` e `const` é que as variáveis ​​`let` podem ser reatribuídas dentro do seu escopo, enquanto as constantes ​​`const` não podem ser reatribuídas. Isso torna `const` útil para declarar identificadores ou valores que não devem ser alterados.

Para declarar um identificador em JavaScript, você pode usar as palavras-chave `var`, `let` ou `const`, seguida pelo nome da variável e, opcionalmente, um valor inicial. Aqui estão alguns exemplos:

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

#### Tipos de dados não primitivos (Tipos estruturados)

Os tipos de dados não primitivos são aqueles que são definidos pelo usuário ou são objetos. Eles são mutáveis, o que significa que seus valores podem ser alterados depois de definidos. Os tipos de dados não primitivos em JavaScript são:

- **Arrays**: são usados para representar coleções ordenadas de valores. Podem conter qualquer tipo de dado, inclusive outros arrays. Exemplo:

  ```javascript
  let numeros = [1, 2, 3];
  let nomes = ["João", "Maria", "Pedro"];
  let misto = [[1, 2, 3], ["João", "Maria", "Pedro"], 2, "Marcos"];
  ```

- **Objetos**: são coleções de pares de chave-valor, em que cada chave é uma string e o valor pode ser qualquer tipo de dado, incluindo outros objetos. Para criar um objeto em JavaScript, você pode usar a sintaxe de objeto literal, que é colocar as chaves e valores dentro de chaves `{}`:

```js
const pessoa = {
  nome: "João",
  idade: 30,
  endereco: {
    rua: "Av. Paulista",
    numero: 100,
    cidade: "São Paulo"
  }
};
```

Além desses tipos estruturados básicos, JavaScript também oferece outras formas de definir estruturas mais complexas, como classes e funções construtoras, que permitem criar objetos com métodos e propriedades personalizados.Essas são apenas algumas das maneiras de definir tipos estruturados em JavaScript. Existem muitas outras, incluindo as bibliotecas e frameworks populares, como React e Vue, que fornecem maneiras de definir componentes reutilizáveis e estruturas de dados personalizadas.

- **Funções**: são usadas para agrupar um conjunto de ações em um bloco de código reutilizável. Podem ser declaradas com ou sem parâmetros. Exemplo:

  ```javascript
  function saudacao(nome) {
    console.log("Olá, " + nome + "!");
  }

  saudacao("João"); // imprime "Olá, João!"
  ```

- **JSON**: Embora o formato de dados JSON seja frequentemente usado em aplicações JavaScript e possa ser facilmente representado como objetos JavaScript, o JSON em si não é um tipo estruturado de JavaScript.

O JSON (JavaScript Object Notation) é um formato de dados que pode ser usado por qualquer linguagem de programação que possa analisar texto. Enquanto isso, um objeto `{}` em JavaScript é um tipo de dados nativo da linguagem, que pode ser usado para representar dados estruturados de forma programática.

- Sintaxe: O JSON tem uma sintaxe específica que é diferente da sintaxe usada para criar objetos JavaScript. Os objetos em JavaScript são definidos usando a sintaxe de chaves `{}` e pares de chave-valor, enquanto o JSON é definido usando apenas texto em um formato específico.

- Métodos: O JSON é um formato de dados independente que é usado para representar informações em diferentes linguagens de programação, incluindo JavaScript. Embora haja alguns métodos JavaScript nativos que permitem trabalhar com JSON (como `JSON.stringify()` e `JSON.parse()`), esses métodos não estão disponíveis para objetos JavaScript.

- Flexibilidade: Os objetos em JavaScript são muito mais flexíveis do que o JSON. Em um objeto JavaScript, você pode adicionar, remover e modificar propriedades e valores à vontade. No JSON, entretanto, você precisa seguir uma estrutura rígida e bem definida, para que possa ser interpretado corretamente por outras linguagens de programação.

- Armazenamento: Os objetos em JavaScript podem ser armazenados em variáveis, em memória ou em bancos de dados, enquanto o JSON é geralmente usado para transferir dados entre diferentes sistemas e aplicações. No entanto, o JSON também pode ser armazenado em arquivos, bancos de dados ou mesmo em variáveis JavaScript se necessário.

Suponha que temos um objeto JavaScript que representa um usuário:

```js
const usuario = {
  nome: 'Ana',
  idade: 28,
  endereco: {
    rua: 'Rua das Flores',
    numero: 123,
    cidade: 'São Paulo'
  }
};
```

Este objeto é representado usando a sintaxe de chaves `{}` e pode ser facilmente manipulado no código JavaScript. Por exemplo, podemos adicionar uma nova propriedade `email` ao objeto da seguinte forma:

```js
usuario.email = 'ana@gmail.com';
```

Agora, vamos supor que precisamos enviar os dados do usuário para um servidor. Nesse caso, podemos usar o formato JSON para representar esses dados em uma string de texto. Para fazer isso, podemos usar o método `JSON.stringify()` do JavaScript:

```js
const usuarioJSON = JSON.stringify(usuario);
```

Isso converterá o objeto JavaScript em uma string JSON:

```JSON
{
  "nome": "Ana",
  "idade": 28,
  "endereco": {
    "rua": "Rua das Flores",
    "numero": 123,
    "cidade": "São Paulo"
  },
  "email": "ana@gmail.com"
}
```

Observe que a sintaxe é diferente da usada em objetos JavaScript. Além disso, a propriedade `email` que adicionamos ao objeto original agora está incluída na string JSON.

Para converter a string JSON de volta para um objeto JavaScript, podemos usar o método `JSON.parse()`:

```js
const usuarioDeJSON = JSON.parse(usuarioJSON);
```

Isso converterá a string JSON de volta para um objeto JavaScript que pode ser manipulado no código da mesma forma que o objeto original:

```js
{
  nome: 'Ana',
  idade: 28,
  endereco: {
    rua: 'Rua das Flores',
    numero: 123,
    cidade: 'São Paulo'
  },
  email: 'ana@gmail.com'
}
```

Em resumo, a principal diferença entre um objeto JavaScript e um objeto JSON é a sintaxe usada para representá-los e a forma como eles são manipulados no código. O objeto JavaScript é um tipo de dados nativos da linguagem, enquanto o JSON é um formato de dados independente usado para representar dados estruturados em várias linguagens de programação, é amplamente utilizado para transmitir dados entre o cliente e o servidor em aplicações web. Ele é especialmente útil quando se trabalha com APIs (Application Programming Interfaces), pois permite que as aplicações transmitam e recebam dados de forma eficiente e fácil de ler e manipular. O JSON também é comumente usado para armazenar dados em bancos de dados NoSQL e em arquivos de configuração de aplicações.

Em resumo, JavaScript possui vários tipos de dados que são usados para representar diferentes tipos de valores. É importante entender os diferentes tipos de dados para poder trabalhar com eles corretamente em seus programas.

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

### Como trabalhar com coleções

Em JavaScript, uma coleção é uma estrutura de dados que pode armazenar vários valores ou objetos de dados em uma única variável. As coleções mais comuns em JavaScript são as Arrays e os Objetos.

Uma Array é uma coleção ordenada de valores, que podem ser números, strings, objetos ou outras Arrays. Os elementos em uma Array são numerados sequencialmente a partir do índice 0 e podem ser acessados por meio do índice.

Já um Objeto é uma coleção de pares de chave-valor, onde cada chave é uma string que identifica a propriedade do objeto, e cada valor pode ser qualquer tipo de dado JavaScript, incluindo outras coleções, como Arrays e Objetos.

Dessa forma, tipos estruturados em JavaScript se referem a um conjunto de tipos de dados que não são primitivos, ou seja, que não são simplesmente um valor único como um número ou uma string. Tipos estruturados incluem Arrays, Objetos e outros tipos de dados complexos que podem armazenar múltiplos valores.

A diferença entre coleções e tipos estruturados é que as coleções são estruturas de dados que podem armazenar uma ou mais instâncias de tipos estruturados, como Arrays e Objetos. Assim, uma coleção é uma instância de um tipo estruturado.

#### Manipulando Arrays

Para criar um array, você pode simplesmente usar o operador de colchetes [ ] e adicionar os elementos desejados separados por vírgulas. Por exemplo:

```javascript
let meuArray = [1, 2, 3, 4, 5];
```

- **Acessando elementos de um Array**: Você pode acessar elementos em um array usando o índice numérico do elemento. Lembre-se de que os índices começam em 0. Por exemplo:

```javascript
let meuArray = [1, 2, 3, 4, 5];
console.log(meuArray[0]); // retorna 1
```

- **Adicionando e removendo elementos de um Array**: Você pode adicionar elementos ao final de um array usando o método push() e remover elementos do final do array usando o método pop(). Você também pode adicionar elementos ao início do array usando o método unshift() e remover elementos do início do array usando o método shift(). Por exemplo:

```javascript
let meuArray = [1, 2, 3, 4, 5];
meuArray.push(6); // adiciona o elemento 6 ao final do array
console.log(meuArray); // retorna [1, 2, 3, 4, 5, 6]
meuArray.pop(); // remove o último elemento do array (o 6)
console.log(meuArray); // retorna [1, 2, 3, 4, 5]
meuArray.unshift(0); // adiciona o elemento 0 ao início do array
console.log(meuArray); // retorna [0, 1, 2, 3, 4, 5]
meuArray.shift(); // remove o primeiro elemento do array (o 0)
console.log(meuArray); // retorna [1, 2, 3, 4, 5]
```

- **Percorrendo um Array**: Você pode percorrer um array usando um loop for ou o método forEach(). O método forEach() executa uma função para cada elemento do array. Por exemplo:

```javascript
let meuArray = [1, 2, 3, 4, 5];
for (let i = 0; i < meuArray.length; i++) {
  console.log(meuArray[i]);
}
// ou
meuArray.forEach(function(elemento) {
  console.log(elemento);
});
```

Esses são apenas alguns exemplos de como manipular Arrays em JavaScript, consulte a documentação e saiba mais!

#### Manipulando objetos

Existem várias maneiras de criar objetos em JavaScript. Uma delas é usando a sintaxe literal de objeto, que é definida entre chaves {}:

```javascript
let pessoa = {
  nome: "João",
  idade: 30,
  endereco: {
    rua: "Rua A",
    cidade: "São Paulo"
  }
};
```

Este objeto tem três propriedades: `nome`, `idade` e `endereco`. A propriedade `endereco` é ela mesma um objeto, que tem duas propriedades: `rua` e `cidade`.

Outra forma de criar um objeto é usando o construtor de objetos `Object()`:

```javascript
let pessoa = new Object();
pessoa.nome = "João";
pessoa.idade = 30;
pessoa.endereco = new Object();
pessoa.endereco.rua = "Rua A";
pessoa.endereco.cidade = "São Paulo";
```

- **Acessando propriedades**: Para acessar as propriedades de um objeto, você pode usar a notação de ponto ou a notação de colchetes. A notação de ponto é mais comum e fácil de ler, mas a notação de colchetes é útil quando você precisa acessar uma propriedade cujo nome é armazenado em uma variável:

```javascript
console.log(pessoa.nome); // João
console.log(pessoa.endereco.cidade); // São Paulo

let propriedade = "idade";
console.log(pessoa[propriedade]); // 30
```

- **Alterando propriedades**: Você pode alterar o valor de uma propriedade de objeto atribuindo um novo valor à propriedade:

```javascript
pessoa.nome = "Maria";
pessoa.endereco.rua = "Rua B";
```

- **Adicionando propriedades**: Você pode adicionar novas propriedades a um objeto simplesmente atribuindo um valor a uma propriedade que ainda não existe:

```javascript
pessoa.telefone = "(11) 1234-5678";
```

- **Removendo propriedades**: Você pode remover uma propriedade de objeto usando o operador `delete`:

```javascript
delete pessoa.telefone;
```

**Percorrendo propriedades**: Para percorrer todas as propriedades de um objeto, você pode usar o laço `for...in`:

```javascript
for (let propriedade in pessoa) {
  console.log(propriedade + ": " + pessoa[propriedade]);
}
```

Este laço percorre todas as propriedades de `pessoa`, e em cada iteração, `propriedade` é uma string com o nome da propriedade, e `pessoa[propriedade]` é o valor da propriedade.

- **Verificando a existência de propriedades**: Você pode verificar se um objeto tem uma propriedade específica usando o operador `in`:

```javascript
console.log("nome" in pessoa); // true
console.log("telefone" in pessoa); // false
```

Você também pode verificar se um objeto tem uma propriedade própria (não herdada) usando o método `hasOwnProperty()`:

```javascript
console.log(pessoa.hasOwnProperty("nome")); // true
console.log(pessoa.hasOwnProperty("toString")); // false
```

### Uso das coleções dos pacotes

O uso de coleções dos pacotes JavaScript depende do pacote específico que você está utilizando. Geralmente, o pacote deve ser instalado usando um gerenciador de pacotes, como o npm, e importado no seu arquivo JavaScript usando a palavra-chave `require` ou `import`, dependendo da versão do JavaScript que você está usando.

existem pacotes integrados com o próprio ambiente de execução, como o navegador ou o Node.js, e geralmente não precisam ser instalados separadamente. Alguns exemplos de pacotes nativos incluem o Array, o Object e o Math.

Por exemplo, se você quiser usar a biblioteca Lodash, que fornece muitas funções úteis para trabalhar com coleções, você pode instalá-la usando o npm:

```js
npm install lodash
```

Em seguida, você pode importar a biblioteca no seu arquivo JavaScript usando o `require`:

```js
const _ = require('lodash');
```

A partir daí, você pode usar as funções da biblioteca para trabalhar com coleções. Por exemplo o pacote Immutable.js, que fornece estruturas de dados imutáveis para JavaScript, incluindo List, Map e Set. Para usar o Immutable.js, você pode instalá-lo usando o npm:

```bash
npm install immutable
```

Em seguida, você pode importar o pacote e usar as estruturas de dados imutáveis. Por exemplo, para criar um mapa imutável com algumas chaves e valores:

```js
import { Map } from 'immutable';

const map1 = Map({ a: 1, b: 2, c: 3 });
console.log(map1); // Output: Map { "a": 1, "b": 2, "c": 3 }
```

Você pode então usar as funções da biblioteca para manipular o mapa imutável, criando novas instâncias de mapa imutável a partir da original:

```js
const map2 = map1.set('b', 50);
console.log(map2); // Output: Map { "a": 1, "b": 50, "c": 3 }

const map3 = map2.delete('a');
console.log(map3); // Output: Map { "b": 50, "c": 3 }
```

Esses são apenas alguns exemplos de como usar coleções em pacotes JavaScript. Sempre consulte a documentação do pacote específico que você está usando para obter informações detalhadas sobre como usar suas coleções.

### Documentação de Programas JavaScript

A documentação de um programa JavaScript é um conjunto de informações escritas sobre o programa, incluindo como usar o programa, quais funções e métodos ele oferece, quais parâmetros essas funções e métodos aceitam, quais valores eles retornam, exemplos de uso e outros detalhes relevantes.

A documentação é essencial para ajudar outros desenvolvedores a entenderem e usarem o programa com facilidade, especialmente em projetos colaborativos. Além disso, a documentação também é uma ferramenta valiosa para ajudar os próprios desenvolvedores a lembrarem de como seu próprio código funciona e como usá-lo corretamente.

Em JavaScript, a documentação pode ser criada em diferentes formatos, incluindo arquivos de texto simples, arquivos Markdown, documentação HTML gerada automaticamente a partir de código-fonte, entre outros.

A documentação pode ser criada manualmente ou com a ajuda de ferramentas de documentação automatizadas, como o JSDoc ou o Docco. Com essas ferramentas, os desenvolvedores podem escrever comentários especiais em seu código que são usados para gerar a documentação automaticamente a partir do código-fonte. Isso ajuda a manter a documentação atualizada à medida que o código é atualizado e a reduzir o trabalho manual envolvido na criação de documentação.

- **Comentários JSDoc** são uma forma especializada de comentários em JavaScript que são usados para documentar o código. Eles são usados para documentar funções, variáveis, parâmetros e valores de retorno. Os comentários JSDoc começam com `/**` e terminam com `*/`. Os comentários JSDoc possuem uma sintaxe específica que permite especificar informações sobre as funções, variáveis e outros elementos do código.

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

Em resumo, a documentação é uma parte importante do processo de desenvolvimento de software e pode ajudar a melhorar a qualidade do código e a facilidade de uso do programa.

### Exercicios de fixação

1. Crie um programa que verifique se um número é par ou ímpar e imprima na tela.

2. Crie um programa que verifique se um número é positivo, negativo ou zero e imprima na tela.

3. Crie um programa que calcule a área de um triângulo com base e altura informadas pelo usuário e imprima na tela.

4. Crie um programa que calcule o perímetro de um quadrado com lado informado pelo usuário e imprima na tela.

5. Crie um programa que concatene duas strings informadas pelo usuário e imprima na tela.

Espero que esses exercícios sejam úteis para você praticar suas habilidades em JavaScript com declaração de variaveis, operadores lógicos, comparação, atribuição e aritméticos!

#### Respostas exercicios de fixação

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
