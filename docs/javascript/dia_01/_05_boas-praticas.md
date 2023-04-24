
# Formatação e Indentação de Código em JavaScript

A `formatação` e `indentação` de código em JavaScript são importantes para a `legibilidade` e `manutenção` do código. Quando o código é organizado de maneira consistente e estruturada, é mais fácil para outros desenvolvedores entenderem o código e fazerem alterações.

## Princípios de Formatação de Código em JavaScript

Os `princípios de formatação` de código em JavaScript incluem a `consistência`, a `clareza` e a `simplicidade`. A `consistência` é importante para que o código seja organizado de maneira previsível e fácil de entender. Isso pode ser alcançado usando um conjunto de regras de formatação que se aplicam a todo o código. A `clareza` refere-se à legibilidade do código, ou seja, a facilidade de compreender o que cada instrução faz. Isso pode ser alcançado usando nomes de variáveis descritivos, comentários claros e código bem organizado. A `simplicidade` envolve manter o código o mais simples possível, eliminando instruções desnecessárias e mantendo o código fácil de entender.

A escolha de `nomes descritivos` para variáveis em JavaScript é uma prática importante que ajuda a tornar o código mais `legível` e `fácil` de entender. Uma `variável descritiva` é aquela que possui um nome que descreve claramente o que a variável representa ou armazena.

A seguir, estão alguns exemplos de `variáveis descritivas` em JavaScript, demonstrando como a escolha de nomes pode ser significativa para a compreensão do código:

```javascript
// Exemplo 1: Variáveis descritivas para armazenar dados do usuário
let nomeUsuario = "Maria"; // variável para armazenar o nome do usuário
let idadeUsuario = 30; // variável para armazenar a idade do usuário
let emailUsuario = "maria@email.com"; // variável para armazenar o e-mail do usuário
```

No exemplo acima, os nomes das `variáveis` são claramente `descritivos` e indicam o tipo de informação que cada variável está armazenando. Isso torna o código mais fácil de entender, especialmente para outros desenvolvedores que podem precisar trabalhar com esse código.

```javascript
// Exemplo 2: Variáveis descritivas para cálculos matemáticos
let valorTotal = 50.00; // variável para armazenar o valor total da compra
let quantidadeProdutos = 3; // variável para armazenar a quantidade de produtos comprados
let valorFrete = 10.00; // variável para armazenar o valor do frete

let valorFinal = valorTotal + (quantidadeProdutos * 5) + valorFrete; // cálculo do valor final
```

Nesse exemplo, os `nomes das variáveis` refletem as informações que elas representam, tornando o código mais `fácil de entender`. Além disso, a escolha de nomes `descritivos` ajuda a `prevenir erros`, como a utilização incorreta de uma variável.

Em resumo, a escolha de `nomes descritivos` para variáveis em JavaScript é uma `prática importante` que pode ajudar a tornar o código mais `legível` e `fácil` de entender. Ao escolher `nomes descritivos`, os desenvolvedores podem facilitar o processo de `leitura` e `manutenção` do código, bem como prevenir erros de programação.

## Princípios de Indentação de Código em JavaScript

Os princípios de `indentação` de código em JavaScript incluem a `hierarquia` e a `clareza`. A `hierarquia` refere-se à estruturação do código em blocos, funções e outras estruturas. Cada `nível da hierarquia` deve ser indentado para que seja fácil de entender a estrutura do código. A `clareza` refere-se à legibilidade do código, ou seja, a facilidade de entender a relação entre as instruções. Isso pode ser alcançado usando uma `indentação` consistente e adequada, que torne claro quais instruções pertencem a quais blocos de código.

### Exemplos Práticos

Aqui estão alguns exemplos práticos de formatação e indentação de código em JavaScript:

#### Exemplo 1: Formatação de código

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

#### Exemplo 2: Indentação de código

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

## Tipos de comentários em JavaScript e sua aplicação

`Comentários` são uma parte importante da programação em JavaScript. Eles ajudam os desenvolvedores a entender o código e a manter a `documentação` do projeto. Existem dois tipos principais de comentários em JavaScript: `comentários de uma linha` e `comentários de várias linhas`. Além disso, existem comentários especiais chamados `JSDoc` que são usados para documentar o código e gerar documentação automática.

### Comentários de uma linha

`Comentários de uma linha` são usados para incluir anotações curtas em uma única linha de código. Eles começam com `//` e são ignorados pelo interpretador JavaScript. Os comentários de uma linha são usados para explicar o que o código faz, ou para deixar uma nota para outro desenvolvedor. Veja o exemplo abaixo:

```javascript
// Define uma variável chamada 'idade' com o valor de 20
let idade = 20;
```

### Comentários de várias linhas

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

### Comentários JSDoc

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
