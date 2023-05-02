## Seletores

Os seletores CSS são utilizados para selecionar elementos HTML com base em suas características ou atributos.

### Seletor de elemento

Seleciona todos os elementos HTML que correspondem ao nome do elemento.

```css
  p {
    font-size: 16px;
    color: #333;
  }
```

### Seletor de classe

Seleciona todos os elementos HTML que possuem a mesma classe. A classe é definida no HTML utilizando o atributo "class".

```css
  .destaque {
    font-weight: bold;
    color: red;
  }
```

### Seletor de ID

Seleciona um único elemento HTML que possui o mesmo ID. O ID é definido no HTML utilizando o atributo "id".

```css
  #cabecalho {
    background-color: #eee;
    height: 100px;
  }
```

### Seletor de atributo

Seleciona todos os elementos HTML que possuem o atributo especificado.

```css
  input[type='text'] {
    border: 1px solid #ccc;
    padding: 5px;
  }
```

### Seletor de descendência

Seleciona todos os elementos filhos de um determinado elemento pai.

```css
  ul li {
    list-style: none;
    margin: 5px 0;
  }
```

### Seletores de pseudo-classes

Os seletores de pseudo-classes CSS permitem selecionar elementos HTML que estão em um estado específico ou que possuem características específicas que não são representadas no HTML.

#### Pseudo-classe "hover"

Seleciona um elemento HTML quando o cursor do mouse é posicionado sobre ele.

```css
  a:hover {
    text-decoration: underline;
  }
```

#### Pseudo-classe "active"

Seleciona um elemento HTML quando ele está sendo clicado.

```css
  button:active {
    background-color: #ccc;
    color: #fff;
  }
```

#### Pseudo-classe "focus"

Seleciona um elemento HTML quando ele está em foco.

```css
  input:focus {
    border: 2px solid blue;
  }
```

### seletor de pseudo elementos

letores de pseudo-elementos CSS permitem selecionar elementos HTML que não existem no código HTML, mas que são gerados pelo navegador.

#### Pseudo-elemento "before"

Insere conteúdo antes do elemento selecionado.

```css
  .icon:before {
    content: url(icon.png);
  }
```

#### Pseudo-elemento "after"

Insere conteúdo depois do elemento selecionado.

```css
  .quote:after {
    content: '"';
  }
```

#### Pseudo-elemento "first-letter"

seleciona a primeira letra de um elemento.

```css
  p:first-letter {
    font-size: 2em;
    font-weight: bold;
  }
```
