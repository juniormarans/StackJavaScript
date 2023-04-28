## Cores Css

As cores em CSS podem ser definidas de várias maneiras, desde nomes de cores predefinidos até valores RGB, HEX e HSL.

### Nome de cor

As cores mais comuns têm nomes predefinidos em CSS.

```css
  color: red;
```

### Valor RGB

As cores também podem ser definidas por seus valores RGB (Red, Green, Blue). Cada valor de cor é representado por um número entre 0 e 255.

```css
  color: rgb(0, 100, 0);
```

### Valor HEX

As cores também podem ser definidas por valores HEX, que são representados por um conjunto de seis caracteres alfanuméricos. Cada dois caracteres representam um valor RGB, com um valor variando entre 00 e FF

```css
  color: #0000FF;
```

### Transparência

As cores em CSS também podem ser definidas com transparência. Isso pode ser útil para criar efeitos de camadas e sobreposições. A transparência é representada por um valor alfa, que varia entre 0 (totalmente transparente) e 1 (totalmente opaco).

```css
  color: rgba(0, 0, 255, 0.5);
```

### Cores HSL

As cores HSL (Hue, Saturation, Lightness) em CSS são definidas por um modelo de cor que utiliza três valores: o matiz (hue), a saturação (saturation) e a luminosidade (lightness).

O valor de matiz é representado por um ângulo, que varia de 0 a 360 graus, e representa a cor propriamente dita. A saturação é representada por um valor percentual entre 0% e 100%, e indica a intensidade ou pureza da cor. A luminosidade também é representada por um valor percentual entre 0% e 100%, e indica o brilho da cor.

```css
  color: hsl(0, 100%, 50%);
```

Também é possível definir a cor utilizando a função hsla(), que permite definir um valor alfa para transparência.

```css
  color: hsla(0, 100%, 50%, 0.5);
```

### Exercícios de Fixação

- 16 - Crie um arquivo HTML com um elemento `<div>`, defina a cor de fundo da `<div>` como amarela, defina a cor do texto da `<div>` como verde, defina a cor da borda da `<div>` como azul.
