# Navegação

A navegação em HTML é uma parte importante da criação de sites e permite que os usuários acessem diferentes páginas e seções do site com facilidade. Existem várias maneiras de criar navegação em HTML, incluindo links de texto, menus de navegação e barras de navegação. Aqui estão alguns exemplos de como criar navegação em HTML.

## Links de texto

Links de texto são usados para criar links clicáveis para outras páginas ou seções do site. Eles são criados usando a tag `<a>` e o atributo href para especificar o URL da página de destino.

```html
  <a href="https://www.exemplo.com">Link para o site exemplo</a>
```

O código acima cria um link de texto clicável que leva o usuário para a página principal do site exemplo

## Menus de navegação

Menus de navegação são usados para mostrar uma lista de links de texto para diferentes seções do site, geralmente na parte superior ou na lateral da página. Eles são criados usando a tag `<ul>` e as tags `<li>` para cada item de menu, junto com as tags `<a>` e href para criar links clicáveis.

```html
  <ul>
    <li><a href="https://www.exemplo.com/home">Home</a></li>
    <li><a href="https://www.exemplo.com/sobre">Sobre</a></li>
    <li><a href="https://www.exemplo.com/produtos">Produtos</a></li>
    <li><a href="https://www.exemplo.com/contato">Contato</a></li>
  </ul>
```

O código acima cria um menu de navegação com quatro links de texto para diferentes seções do site.

## Barras de navegação

Barras de navegação são semelhantes aos menus de navegação, mas geralmente incluem mais elementos, como um logotipo e um formulário de pesquisa. Elas são criadas usando a tag `<nav>` e as mesmas tags `<ul>`, `<li>`, `<a>` e href usadas em menus de navegação.

```html
  <nav>
    <ul>
      <li><a href="https://www.exemplo.com"><img src="logo.png" alt="Logo"></a></li>
      <li><a href="https://www.exemplo.com/home">Home</a></li>
      <li><a href="https://www.exemplo.com/sobre">Sobre</a></li>
      <li><a href="https://www.exemplo.com/produtos">Produtos</a></li>
      <li><a href="https://www.exemplo.com/contato">Contato</a></li>
      <li>
        <form action="https://www.exemplo.com/pesquisa">
          <input type="text" placeholder="Pesquisar">
          <button type="submit">Buscar</button>
        </form>
      </li>
    </ul>
  </nav>
```

O código acima cria uma barra de navegação com um logotipo, links de texto para diferentes seções do site e um formulário de pesquisa.

É importante lembrar que a navegação pode ser personalizada com CSS para mudar a aparência dos links de texto, menus e barras de navegação.
