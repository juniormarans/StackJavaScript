# Elementos de Formulário

Elementos de formulário HTML são usados ​​para coletar informações do usuário, como nome, endereço, senha, etc.

## Label

A tag `<label>` em HTML é usada para associar um rótulo descritivo a um elemento de formulário, como um campo de texto ou uma caixa de seleção. Isso ajuda a tornar os formulários mais acessíveis e fáceis de usar para usuários com deficiência visual, pois permite que o rótulo seja lido em conjunto com o elemento de formulário correspondente.

O atributo "for" deve ser usado para especificar o ID do elemento de formulário correspondente. Por exemplo, se você tiver um campo de texto com o ID "nome" e quiser associar um rótulo a ele.

```html
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome">
```

## Input

O elemento HTML `<input>` é usado para coletar informações do usuário por meio de campos de entrada, como texto, senha, caixa de seleção, botão de opção, etc.

### Campo de texto

O campo de texto é usado para permitir que o usuário insira texto.

```html
  <input type="text" name="nome" placeholder="Digite seu nome">
```

### Campo de senha

O campo de senha é usado para coletar senhas do usuário. Os caracteres digitados são mascarados para impedir que sejam vistos por outras pessoas.

```html
  <input type="password" name="senha" placeholder="Digite sua senha">
```

### Caixa de seleção

A caixa de seleção é usada para permitir que o usuário selecione uma ou mais opções de uma lista de opções.

```html
  <input type="checkbox" name="aceitar-termos" id="aceitar-termos">
  <label for="aceitar-termos">Eu aceito os termos e condições</label>
```

### Botão de opção

O botão de opção é usado para permitir que o usuário selecione uma opção de uma lista de opções.

```html
  <input type="radio" name="genero" value="masculino" id="masculino">
  <label for="masculino">Masculino</label>
  <input type="radio" name="genero" value="feminino" id="feminino">
  <label for="feminino">Feminino</label>
```

### Botão de Verificação

O atributo "type" deve ser definido como "checkbox" para indicar que é um campo de seleção de caixa de verificação. O atributo "name" é usado para identificar o campo de entrada quando o formulário é enviado, e o atributo "value" é usado para especificar o valor que será enviado junto com o nome do campo.

```html
  <form>
    <input type="checkbox" name="opcao1" value="valor1"> Opção 1 <br>
    <input type="checkbox" name="opcao2" value="valor2"> Opção 2 <br>
    <input type="checkbox" name="opcao3" value="valor3"> Opção 3 <br>
  </form>
```

Quando o formulário é enviado, o nome da caixa de seleção selecionada será enviado junto com o valor correspondente. Se a caixa de seleção não estiver marcada, o nome da caixa de seleção não será enviado.

### Botão Input

O botão é usado para criar botões clicáveis.

```html
  <input type="submit" value="Enviar">
```

## Area de Texto

O elemento HTML `<textarea>` é usado para permitir que o usuário insira várias linhas de texto.

```html
  <textarea name="mensagem" rows="5" cols="40">
    Digite sua mensagem aqui
  </textarea>
```

Neste exemplo, o elemento `<textarea>` cria uma caixa de texto com 5 linhas e 40 colunas para o usuário inserir sua mensagem. O texto "Digite sua mensagem aqui" é o texto de preenchimento, que é exibido na caixa de texto até que o usuário comece a digitar.

O atributo name é usado para identificar o campo de texto ao enviar o formulário. Quando o formulário é enviado, o valor da caixa de texto é enviado como parte dos dados do formulário com o nome especificado no atributo name.

## Botão

Em HTML, existem vários tipos de botões que podem ser criados usando a tag `<button>`.

### Botão padrão

```html
  <button>Enviar</button>
```

### Botão com imagem

```html
  <button><img src="icone.png" alt="Ícone">Enviar</button>
```

### Botão com ícone

```html
  <button><i class="fas fa-envelope"></i>Enviar</button>
```

### Botão de envio de formulário

```html
  <input type="submit" value="Enviar">
```

### Botão de resetar formulário

```html
  <input type="reset" value="Limpar">
```

### Botão com função JavaScript

```html
  <button onclick="alert('Botão clicado')">Clique aqui</button>
```
