# Introdução a CSS

CSS (Cascading Style Sheets) é uma linguagem de estilo utilizada para descrever a aparência e o layout de páginas da web. Ele trabalha em conjunto com HTML e JavaScript para criar efeitos visuais, como cores, fontes, tamanhos, margens, espaçamentos, posicionamentos e outros elementos de design.

CSS foi desenvolvido para permitir a separação do conteúdo e da apresentação em uma página da web, o que facilita o desenvolvimento e a manutenção do código. Em vez de codificar a aparência diretamente em cada elemento HTML, as propriedades de estilo são definidas em uma folha de estilo CSS separada, que é então aplicada a todos os elementos HTML que compartilham as mesmas características.

A linguagem CSS é composta de regras, que definem como um elemento HTML deve ser estilizado. Uma regra CSS é composta por um seletor, que identifica o elemento HTML que será estilizado, e um bloco de declarações, que define as propriedades de estilo que serão aplicadas ao elemento.

```css
  /*Seletor*/
  h1 {
    /*Bloco de declarações*/
    color: blue;
    font-size: 24px;
    text-align: center;
  }
```

Neste exemplo, a regra CSS define um estilo para todos os elementos `<h1>` na página. As declarações definem a cor do texto como azul, o tamanho da fonte como 24 pixels e o alinhamento do texto como centralizado.

Também  é possível incluir estilos CSS diretamente na página HTML usando a tag `<style>` no cabeçalho da página ou diretamente em um elemento HTML usando o atributo "style".

```html
  <!DOCTYPE html>
  <html>
    <head>
      <style>
        h1 {
          color: blue;
          font-size: 24px;
        }
      </style>
    </head>
    <body>
      <h1>Este é um cabeçalho com estilo definido em uma tag &lt;style&gt;.</h1>
      <p style="color: red;">Este é um parágrafo com estilo definido em um atributo "style".</p>
    </body>
  </html>
```

Neste exemplo, a tag `<style>` é usada para definir as regras CSS para os elementos HTML na página. O atributo "style" é usado para definir o estilo diretamente em um elemento HTML específico.

## Importando arquivos css

Para importar um arquivo CSS em uma página HTML, é necessário incluir uma tag `<link>` no cabeçalho da página HTML. A tag `<link>` é usada para carregar um arquivo externo, como um arquivo CSS, e conectá-lo à página HTML.

O atributo rel define o tipo de relacionamento entre a página HTML e o arquivo CSS e deve ser definido como "stylesheet". O atributo href especifica o caminho do arquivo CSS que será carregado.

Para importar um arquivo CSS armazenado no mesmo diretório da página HTML, o caminho do arquivo CSS pode ser especificado simplesmente pelo nome do arquivo.

```html
  <link rel="stylesheet" href="estilo.css">
```

Para importar um arquivo CSS armazenado em um diretório diferente, o caminho do arquivo CSS deve ser especificado de acordo com a estrutura de diretórios.

```html
  <link rel="stylesheet" href="css/estilo.css">
```

Essa tag `<link>` deve ser adicionada dentro da seção `<head>` da página HTML.

```html
  <!DOCTYPE html>
  <html>
    <head>
      <link rel="stylesheet" href="estilo.css">
      <title>Minha página HTML</title>
    </head>
    <body>
      <p>Olá, mundo!</p>
    </body>
  </html>
```

Dessa forma, a página HTML pode ser estilizada com as regras CSS definidas no arquivo importado.

## Identificação de elementos

Existem várias maneiras de identificar um elemento HTML, como nome da tag, classe e ID, e cada uma delas tem sua própria forma de referência em CSS.

### Identificação por nome de tag

Para identificar um elemento usando a tag, basta referenciar o nome da tag.

```html
  <p>Este é um parágrafo.</p>
```

Para referenciar um elemento HTML por nome de tag em CSS, basta escrever o nome da tag sem aspas.

```css
  p {
    font-size: 16px;
    color: #333;
  }
```

O código acima define um estilo para todos os elementos `<p>` da página.

### Identificação por classe

 A classe é um atributo que pode ser atribuído a um elemento e permite que os elementos sejam agrupados e estilizados em conjunto. Para identificar um elemento usando a classe, basta referenciar o nome da classe.

```html
  <p class="destaque">Este é um parágrafo destacado.</p>
```

 Para referenciar um elemento HTML por classe em CSS, use o seletor de classe, que é um ponto seguido pelo nome da classe.

```css
  .destaque {
    font-weight: bold;
    color: blue;
  }
```

O código acima define um estilo para todos os elementos com a classe "destaque".

### Identificação por ID

O ID é um atributo que é atribuído a um único elemento e é usado para identificá-lo de forma exclusiva. Para identificar um elemento usando o ID, basta referenciar o nome do ID

```html
  <p id="paragrafo1">Este é um parágrafo com ID.</p>
```

Para referenciar um elemento HTML por ID em CSS, use o seletor de ID, que é uma hashtag seguida pelo nome do ID.

```css
  #paragrafo1 {
    background-color: yellow;
  }
```

O código acima define um estilo para o elemento com o ID "paragrafo1".

A escolha do método de identificação de elemento HTML depende do contexto e das necessidades específicas do desenvolvedor. Além disso, é importante lembrar que a especificidade dos seletores CSS é levada em consideração quando vários estilos se aplicam ao mesmo elemento, o que pode levar a conflitos e resultados inesperados se não for gerenciado corretamente.
