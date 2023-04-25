# Tags e Elementos

A marcação é feita através de tags, que são elementos com nomes específicos e que envolvem o conteúdo da página para atribuir um significado específico. Cada tag pode ter atributos, que fornecem informações adicionais sobre a tag e seu conteúdo.

Os atributos são pares de valores que especificam propriedades adicionais de uma tag HTML. Eles fornecem informações como cor, tamanho, alinhamento, link de destino e outras propriedades que ajudam a definir a aparência e o comportamento dos elementos da página.

Os atributos permitem que os desenvolvedores controlem vários aspectos do comportamento e da aparência dos elementos HTML. Eles podem ser usados para definir a largura e a altura de imagens, especificar o destino de um link, definir o estilo de um elemento usando CSS, entre outras funcionalidades.

Os desenvolvedores web usam tags e atributos HTML para criar documentos que possam ser interpretados e renderizados pelos navegadores. A linguagem HTML é essencial para a criação de páginas web, pois fornece a estrutura básica para a exibição de conteúdo em um navegador da web.

Para mais informações de tags acesse o link:
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element]

Para mais informações de atributos acesse o link:
[https://developer.mozilla.org/pt-BR/docs/Web/HTML/Attributes]

## Títulos e Sub-títulos

Para organizar e estruturar o conteúdo de uma página, é comum utilizar os títulos e sub-títulos HTML.

Existem seis níveis de títulos HTML, que vão do `<h1>` ao `<h6>`. O `<h1>` é o título mais importante e deve ser usado para o título principal da página, enquanto o `<h6>` é o título menos importante. Os títulos e sub-títulos são importantes para ajudar os usuários a entender a hierarquia de informação da página e para auxiliar os mecanismos de busca a entenderem o conteúdo da página.

```html
  <h1>Título principal da página</h1>
  <h2>Sub-título da seção</h2>
  <h3>Sub-título de uma sub-seção</h3>
  <h4>Sub-título de uma sub-seção menor</h4>
  <h5>Sub-título de uma sub-seção ainda menor</h5>
  <h6>Sub-título de uma sub-seção muito pequena</h6>
```

Ao utilizar os títulos e sub-títulos HTML, é importante lembrar que eles não devem ser usados apenas para mudar o tamanho ou estilo do texto. Eles devem ser utilizados para indicar a importância e a hierarquia do conteúdo da página.

## Parágrafo

Em HTML, o parágrafo é definido pela tag `<p>`. Essa tag é usada para separar blocos de texto e criar parágrafos na página. Os navegadores geralmente exibem o texto dentro de uma tag `<p>` com um espaço em branco antes e depois do parágrafo.

```html
  <p>Este é um exemplo de parágrafo em HTML. Ele contém várias frases que são separadas por pontos finais. O texto dentro de um parágrafo pode incluir formatação, como negrito, itálico, sublinhado e outros elementos HTML.</p>
```

Os parágrafos em HTML são úteis para separar e organizar o conteúdo em uma página. É importante lembrar que, para garantir a acessibilidade da página, é recomendável usar parágrafos curtos e dividir o conteúdo em seções bem definidas. Além disso, é importante usar a tag `<p>` para criar parágrafos, em vez de adicionar quebras de linha ou espaços em branco, para garantir que o conteúdo seja apresentado de forma consistente em diferentes dispositivos e navegadores.

## Comentários

Em HTML, é possível adicionar comentários no código para fornecer informações adicionais ou anotações que não são exibidas na página web. Os comentários em HTML são úteis para documentar o código e explicar sua funcionalidade para outros desenvolvedores ou para si mesmo no futuro.

Para adicionar um comentário em HTML, você pode usar a tag `<!-- -->`. Tudo o que estiver dentro dos símbolos `<!-- e -->` será tratado como um comentário e não será exibido na página web.

```html
  <!-- Este é um comentário em HTML. Ele não será exibido na página web, mas pode ser útil para documentar o código ou fornecer anotações adicionais. -->
```

Os comentários em HTML são úteis para tornar o código mais fácil de entender e manter. Eles podem ser usados para explicar o propósito de uma seção de código, fornecer anotações para outros desenvolvedores ou para si mesmo no futuro, ou para desativar temporariamente uma seção de código sem precisar removê-la completamente.

## Identação

A identação em HTML é a prática de adicionar espaços em branco e quebras de linha para organizar e estruturar o código. A identação em HTML é uma boa prática de codificação e pode ajudar a tornar o código mais fácil de entender e manter.

```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>Título da página</title>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>
      <h1>Este é um título principal</h1>
      <p>Este é um exemplo de parágrafo em HTML.</p>
      <ul>
        <li>Item 1 da lista</li>
        <li>Item 2 da lista</li>
        <li>Item 3 da lista</li>
      </ul>
    </body>
  </html>
```

O código acima mostra uma página HTML simples com identação. Observe que as tags HTML dentro de outras tags HTML estão indentadas com dois espaços para facilitar a leitura e entender a hierarquia do código.

A identação em HTML é uma boa prática de codificação, pois torna o código mais fácil de ler e entender. Também ajuda a detectar erros de codificação e manter uma estrutura organizada do código. No entanto, é importante lembrar que a identação não afeta o funcionamento do código HTML. É apenas uma prática recomendada para tornar o código mais legível e fácil de manter.
