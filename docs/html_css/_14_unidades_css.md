## Unidades do CSS

As unidades de medida em CSS são usadas para definir o tamanho e a posição dos elementos na página. Existem vários tipos de unidades, cada um com um propósito específico

### Pixels (px)

O pixel é a unidade de medida mais comum em CSS. É uma unidade fixa e refere-se a um único pixel na tela. Por exemplo, a propriedade font-size: 16px; define o tamanho da fonte como 16 pixels.

```css
  div {
    width: 200px;
    height: 100px;
    font-size: 16px;
  }
```

### Porcentagem (%)

A unidade de medida em porcentagem é relativa ao tamanho do elemento pai. Por exemplo, a propriedade width: 50%; define a largura do elemento como metade do tamanho do elemento pai.

```css
  .parent {
    width: 400px;
    height: 200px;
  }

  .child {
    width: 50%;
    height: 100px;
  }
```

### Em (em)

O "em" é uma unidade de medida relativa ao tamanho da fonte do elemento pai. Por exemplo, font-size: 1.2em; define a fonte do elemento como 1,2 vezes maior do que a fonte do elemento pai.

```css
  .parent {
    font-size: 16px;
  }

  .child {
    font-size: 1.2em;
  }
```

### Rem (rem)

O "rem" é uma unidade de medida relativa ao tamanho da fonte do elemento raiz, geralmente o elemento HTML. Por exemplo, font-size: 1.2rem; define a fonte do elemento como 1,2 vezes maior do que a fonte do elemento raiz.

```css
  html {
    font-size: 16px;
  }

  .child {
    font-size: 1.2rem;
  }
```

### Viewport Width (vw) e Viewport Height (vh)

Essas unidades de medida são relativas ao tamanho da janela do navegador. Por exemplo, width: 50vw; define a largura do elemento como metade da largura da janela do navegador.

```css
  div {
    width: 50vw;
    height: 50vh;
  }
```

### Unidades Absolutas (cm, mm, in, pt)

Essas unidades são absolutas e são baseadas em medidas físicas, como polegadas (in), centímetros (cm) e pontos (pt). No entanto, essas unidades podem ser menos úteis para a web, pois as medidas físicas podem variar em diferentes dispositivos.

```css
  div {
    width: 5cm;
    height: 2in;
  }
```

É importante escolher a unidade certa para o tipo de propriedade que você está definindo, a fim de obter a aparência desejada.
