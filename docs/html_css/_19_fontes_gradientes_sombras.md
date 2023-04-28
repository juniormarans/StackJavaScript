## Fontes

As fontes em CSS são definidas através da propriedade font-family, que especifica a família da fonte a ser usada para o elemento HTML selecionado. Também podemos definir outras propriedades relacionadas às fontes, como tamanho, cor, estilo e peso.

```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>Exemplo de fonte CSS</title>
      <link rel="stylesheet" type="text/css" href="estilos.css">
    </head>
    <body>
      <p>Este é um exemplo de texto com a fonte padrão.</p>
    </body>
  </html>
```

```css
  body {
    font-family: Arial, sans-serif;
  }
```

## Gradientes

Duas formas de criar gradientes são com o linear-gradient e radial-gradient.

### Linear Gradient

```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>Exemplo de linear gradient CSS</title>
      <link rel="stylesheet" type="text/css" href="estilos.css">
    </head>
    <body>
      <div class="exemplo">
        <h1>Exemplo de linear gradient</h1>
        <p>Este é um exemplo de um gradiente linear em CSS.</p>
      </div>
    </body>
  </html>
```

```css
  .exemplo {
    background: linear-gradient(to bottom right, #ff8c00, #ff69b4);
    padding: 20px;
  }
```

Nesse exemplo, usamos o linear-gradient para criar um gradiente que vai do canto superior esquerdo ao canto inferior direito da `<div>`. As cores usadas são #ff8c00 e #ff69b4. Também adicionamos um espaçamento interno à `<div>` com a propriedade padding.

### Radial Gradient

```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>Exemplo de radial gradient CSS</title>
      <link rel="stylesheet" type="text/css" href="estilos.css">
    </head>
    <body>
      <div class="exemplo">
        <h1>Exemplo de radial gradient</h1>
        <p>Este é um exemplo de um gradiente radial em CSS.</p>
      </div>
    </body>
  </html>
```

```css
  .exemplo {
    background: radial-gradient(circle, #ff8c00, #ff69b4);
    padding: 20px;
  }
```

Nesse exemplo, usamos o radial-gradient para criar um gradiente radial que começa no centro da `<div>` e se espalha em todas as direções. As cores usadas são #ff8c00 e #ff69b4. Também adicionamos um espaçamento interno à `<div>` com a propriedade padding.

### Shadow

```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>Exemplo de shadow CSS</title>
      <link rel="stylesheet" type="text/css" href="estilos.css">
    </head>
    <body>
      <div class="exemplo">
        <h1>Exemplo de shadow</h1>
        <p>Este é um exemplo de uma sombra em CSS.</p>
      </div>
    </body>
  </html>
```

```css
  .exemplo {
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
    padding: 20px;
  }
```

Nesse exemplo, usamos a propriedade box-shadow para adicionar uma sombra à `<div>`. A sombra é criada com um deslocamento horizontal de 2 pixels, um deslocamento vertical de 2 pixels, um raio de 5 pixels e uma opacidade de 0.3. Também adicionamos um espaçamento interno à `<div>` com a propriedade padding.

### Gradient e Shadow combinados

```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>Exemplo de gradient e shadow CSS</title>
      <link rel="stylesheet" type="text/css" href="estilos.css">
    </head>
    <body>
      <div class="exemplo">
        <h1>Exemplo de gradient e shadow combinados</h1>
        <p>Este é um exemplo de um gradiente com sombra em CSS.</p>
      </div>
    </body>
  </html>
```

```css
  .exemplo {
    background: linear-gradient(to bottom right, #ff8c00, #ff69b4);
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
    padding: 20px;
  }
```

Nesse exemplo, combinamos o gradiente linear com a sombra. A `<div>` tem um gradiente que vai do canto superior esquerdo ao canto inferior direito, com as cores #ff8c00 e #ff69b4. Além disso, tem uma sombra com um deslocamento horizontal de 2 pixels, um deslocamento vertical de 2 pixels, um raio de 5 pixels e uma opacidade de 0.3. Também adicionamos um espaçamento interno à `<div>` com a propriedade padding.

### Exercícios de Fixação

- 19 - Crie uma página HTML com um título e um parágrafo. Adicione um estilo CSS para aplicar um gradiente linear de cima para baixo com as cores #ffcccc e #ff6666 ao fundo do body.

- 20 - Crie uma página HTML com um título e um parágrafo. Adicione um estilo CSS para aplicar um gradiente radial ao fundo do body com as cores #f9f9f9 e #333333.

- 21 - Crie uma página HTML com um título e um parágrafo. Adicione um estilo CSS para aplicar uma sombra de 5 pixels com deslocamento horizontal e vertical de 2 pixels e uma opacidade de 0,3 ao título.
