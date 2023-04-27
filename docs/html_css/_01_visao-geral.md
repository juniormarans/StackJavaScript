## HTML

HTML, ou Hypertext Markup Language, é uma linguagem de marcação utilizada para criar e estruturar documentos na World Wide Web. Essa linguagem é composta por uma série de elementos que definem como o conteúdo de um documento deve ser exibido em um navegador da web.

Os elementos HTML são compostos por tags, que são identificadas por colchetes angulares. Essas tags são usadas para definir a estrutura do documento, como títulos, parágrafos, imagens, links e outros elementos que compõem uma página da web.

A estrutura e o conteúdo de um documento HTML são interpretados por um navegador da web, que utiliza as informações fornecidas pelas tags para renderizar a página de forma adequada. Isso permite que os usuários possam acessar e visualizar o conteúdo de páginas da web de maneira consistente e padronizada.

Em resumo, HTML é uma linguagem de marcação fundamental para a criação de páginas da web, permitindo que os desenvolvedores criem documentos bem estruturados e formatados para serem visualizados em navegadores da web.

### Como funciona uma página web

Uma página web é composta por uma série de elementos interconectados que trabalham em conjunto para fornecer uma experiência de usuário consistente e interativa. Esses elementos incluem o código HTML que define a estrutura e o conteúdo da página, o CSS que define a aparência visual da página e o JavaScript que fornece interatividade e dinamicidade à página.

Quando um usuário acessa uma página web, o navegador da web faz uma solicitação ao servidor que hospeda o site, enviando as informações necessárias para exibir a página. O servidor, por sua vez, envia a página ao navegador, que começa a processá-la.

Primeiramente, o navegador interpreta o código HTML e constrói a estrutura da página, criando uma árvore de elementos que representam o conteúdo e a hierarquia da página. Em seguida, o navegador aplica o CSS para definir a aparência visual da página, definindo o estilo, a cor, o tamanho e outras características visuais dos elementos na página.

Depois, o navegador executa qualquer código JavaScript incluído na página, permitindo que a página interaja com o usuário ou realize tarefas dinâmicas, como carregar conteúdo adicional ou fazer solicitações ao servidor.

Finalmente, o navegador exibe a página na tela do usuário, combinando todos os elementos processados para criar a visualização final da página. Durante todo o processo, o navegador monitora as interações do usuário com a página, permitindo que a página seja atualizada ou modificada dinamicamente, conforme necessário.

Uma página web funciona através de uma combinação de elementos HTML, CSS e JavaScript que são processados pelo navegador da web para fornecer uma experiência interativa e consistente aos usuários.

### Os fundamentos do HTML

HTML é uma linguagem de marcação usada para definir a estrutura e o conteúdo de páginas da web. O HTML é composto por três conceitos fundamentais: tags, elementos e atributos.

As tags são os blocos básicos de construção do HTML. Elas são identificadas por colchetes angulares (< >) e são usadas para criar elementos HTML. Existem dois tipos de tags: as tags de abertura e as tags de fechamento. As tags de abertura indicam o início de um elemento HTML, enquanto as tags de fechamento indicam o seu fim. Além disso, há também as tags auto-fecháveis, que não requerem uma tag de fechamento.

Os elementos são as estruturas de dados que compõem uma página da web. Eles são definidos usando tags e geralmente incluem um conjunto de atributos que especificam suas características e comportamentos. Um elemento pode conter texto, imagens, outros elementos ou qualquer combinação desses.

Os atributos são usados para definir as propriedades de um elemento. Eles são definidos dentro da tag de abertura e geralmente têm um valor associado que define o comportamento ou a aparência do elemento. Existem vários tipos de atributos, como os atributos de estilo, que definem o estilo visual do elemento, e os atributos de ação, que especificam o comportamento interativo do elemento.

Tags, elementos e atributos são conceitos fundamentais do HTML que permitem aos desenvolvedores criar e estruturar páginas da web de forma consistente e padronizada. Tags são blocos básicos de construção do HTML, elementos são as estruturas de dados que compõem a página e atributos definem as propriedades e comportamentos desses elementos.

### Estrutura básica de uma página html

A estrutura básica de uma página HTML é composta por uma série de elementos que definem a estrutura e o conteúdo da página. Essa estrutura segue um padrão comum, que inclui as seguintes seções principais:

**Doctype:** a primeira linha de uma página HTML é o doctype, que informa ao navegador a versão do HTML sendo usada na página.

**HTML:** em seguida, vem a tag HTML, que envolve todo o conteúdo da página. Essa tag contém dois atributos principais: lang, que define o idioma da página, e dir, que define a direção do texto.

**Head:** a seção head é usada para incluir informações sobre a página, como o título da página, metadados, scripts, folhas de estilo e outras informações importantes. Essa seção não é exibida na página em si, mas fornece informações importantes para o navegador e os mecanismos de busca.

**Body:** a seção body é onde o conteúdo real da página é definido. Ela contém todos os elementos visíveis na página, como títulos, parágrafos, imagens, links e outros elementos.

A estrutura básica de uma página HTML é essencial para garantir a correta renderização da página pelos navegadores da web. Além disso, seguir esse padrão ajuda os desenvolvedores a criar páginas consistentes e padronizadas, facilitando a manutenção e a atualização do conteúdo da página no futuro.

```html
  <!DOCTYPE html>
  <html lang="pt-br">
    <head>
      <meta charset="UTF-8">
      <title>Minha Página HTML</title>
    </head>
    <body>
      <h1>Bem-vindo à minha página HTML!</h1>
      <p>Esta é uma página HTML básica.</p>
    </body>
  </html>
```

Nesse exemplo, a página começa com a declaração do doctype, seguida da tag HTML, que define o idioma da página como português do Brasil. A seção head inclui a meta tag que define o conjunto de caracteres da página como UTF-8 e o título da página. A seção body inclui o conteúdo real da página, que consiste em um cabeçalho h1 e um parágrafo simples.

### Como Rodar um código html

Para rodar um código HTML, você precisa de um navegador da web, como o Google Chrome, Mozilla Firefox, Safari, ou outro.

- Abra um editor de texto simples, como o Bloco de Notas (no Windows) ou o TextEdit (no macOS).
- Digite o código HTML no editor de texto, ou copie e cole o código de um arquivo existente.
- Salve o arquivo com a extensão ".html" (por exemplo, "meu_arquivo.html").
- Abra o arquivo HTML em um navegador da web, clicando duas vezes no arquivo salvo ou arrastando-o para a janela do navegador.

O navegador da web deve exibir o conteúdo HTML conforme definido no código. Se o arquivo HTML contém imagens ou outros arquivos externos, certifique-se de que eles estejam no mesmo diretório do arquivo HTML ou que os caminhos estejam corretos.
