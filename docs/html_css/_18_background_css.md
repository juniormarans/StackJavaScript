## Backgrounds CSS

As propriedades de background em CSS são utilizadas para definir a aparência do fundo de um elemento. Existem várias propriedades que podem ser utilizadas para definir backgrounds em CSS.

### background-color

Define a cor de fundo do elemento.

```css
  background-color: white;
```

### background-image

Define uma imagem para ser usada como background.

```css
  background-image: url("paisagem.jpg");
```

### background-repeat

Define como a imagem de fundo deve se repetir. Os valores podem ser repeat (repete a imagem horizontal e verticalmente), repeat-x (repete a imagem apenas horizontalmente) ou repeat-y (repete a imagem apenas verticalmente).

```css
  background-repeat: repeat-x;
```

### background-position

Define a posição da imagem de fundo. Os valores podem ser representados por coordenadas, como "left top" (posiciona a imagem no canto superior esquerdo), "center center" (posiciona a imagem no centro) ou "right bottom" (posiciona a imagem no canto inferior direito)

```css
  background-position: center center;
```

### background-size

Define o tamanho da imagem de fundo. Os valores podem ser representados em pixels, em porcentagem ou com as palavras-chave "auto" (mantém a proporção original da imagem) ou "cover" (ajusta a imagem para preencher todo o elemento, cortando qualquer excesso)

```css
  background-size: cover;
```

### Exercícios de Fixação

- 17 - Crie um arquivo HTML com um elemento `<div>`, defina uma imagem de fundo para a `<div>`, repita a imagem horizontalmente, posicione a imagem no centro da `<div>`.
