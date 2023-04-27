## Posicionando

O posicionamento de imagens em uma página HTML é importante para aprimorar a aparência visual e a legibilidade da página. Existem várias maneiras de posicionar uma imagem em uma página HTML.

### Imagem Alinhada

O alinhamento da imagem é a maneira mais comum de posicionar uma imagem em uma página HTML. A imagem pode ser alinhada à esquerda, à direita ou centralizada.

```html
  <img src="imagem.jpg" style="float: left;">
  <p>Esta é uma imagem alinhada à esquerda.</p>

  <img src="imagem.jpg" style="float: right;">
  <p>Esta é uma imagem alinhada à direita.</p>

  <img src="imagem.jpg" style="display: block; margin: 0 auto;">
  <p>Esta é uma imagem centralizada.</p>
```

### Imagem como Fundo

A imagem pode ser usada como fundo de uma seção ou de toda a página HTML. É possível definir a posição da imagem no fundo, bem como a repetição da imagem no fundo.

```html
  <style>
    body {
      background-image: url("imagem.jpg");
      background-position: center;
      background-repeat: no-repeat;
    }
  </style>
  <p>Esta é uma página com imagem de fundo.</p>
```

### Imagem como Link

Uma imagem pode ser transformada em um link, de modo que, quando clicada, a imagem direciona o usuário para outra página ou seção.

```html
  <a href="https://exemplo.com">
    <img src="imagem.jpg">
  </a>
  <p>Esta imagem é um link para outro site.</p>
```

### Exercícios de Fixação

- 04 - Criando uma imagem de fundo responsiva: Crie uma imagem de fundo que se ajuste ao tamanho da tela do dispositivo. Use a tag background-image para definir a imagem de fundo e a tag background-size para ajustar o tamanho da imagem.

- 05 - Posicionando um elemento no rodapé da página: Crie um layout onde um elemento de texto esteja sempre posicionado no rodapé da página. Use a tag position para posicionar o elemento no rodapé e a tag bottom para alinhar o elemento à parte inferior da página.
