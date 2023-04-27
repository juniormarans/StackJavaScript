## Normalização de Css

Normalização de css é um conjunto de regras que redefine as propriedades de todos os elementos HTML para um estado consistente em diferentes navegadores. Isso ajuda a garantir que a aparência do site seja consistente em diferentes plataformas e navegadores.

O reset é geralmente colocado no início do arquivo CSS para que as propriedades dos elementos possam ser definidas a partir de uma base comum. Há várias formas de fazer o reset em CSS, mas geralmente envolve a definição das propriedades de margem, preenchimento, borda e fonte para zero ou valores padrão

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

html, body {
  height: 100%;
}

body {
  background-color: #f0f0f0;
}
```

Neste exemplo, todas as propriedades de margem e preenchimento são definidas como zero para todos os elementos, e o modelo de caixa é definido como "border-box", o que significa que a largura e a altura dos elementos incluem a borda e o preenchimento. A fonte padrão é definida como Arial ou uma fonte sem serifa, para garantir que a fonte seja consistente em diferentes navegadores.

As propriedades de altura e largura também são definidas como 100% para o elemento html e o corpo, para garantir que o site ocupe toda a janela do navegador. A cor de fundo do corpo é definida como #f0f0f0 para dar um fundo cinza claro ao site.

O reset de CSS é uma boa prática para garantir a consistência na aparência do site em diferentes navegadores e plataformas. No entanto, é importante lembrar que o reset não é uma solução universal e pode não ser adequado para todos os projetos, pois pode afetar a aparência de elementos personalizados e de terceiros.
