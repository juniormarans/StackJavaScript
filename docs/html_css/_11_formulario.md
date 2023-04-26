# Formulário

É possível criar formulários para coletar informações do usuário. Os formulários são criados usando a tag `<form>` e podem conter vários tipos de campos, como campos de texto, botões, caixas de seleção e botões de opção.

```html
  <form>
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome"><br>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br>

    <label for="mensagem">Mensagem:</label>
    <textarea id="mensagem" name="mensagem"></textarea><br>

    <input type="submit" value="Enviar">
  </form>
```

O formulário possui três campos: um campo de texto para o nome do usuário, um campo de e-mail e uma caixa de texto para a mensagem. Cada campo é criado usando a tag `<input>` ou a tag `<textarea>`, e o atributo "type" é usado para especificar o tipo de campo. O atributo "id" é usado para identificar exclusivamente cada campo, e o atributo "name" é usado para enviar os valores do campo para o servidor quando o formulário é enviado.

O botão de envio é criado usando a tag `<input>` com o atributo "type" definido como "submit". Quando o usuário clica no botão, o formulário é enviado para o servidor para processamento. Também é possível criar botões de resetar usando a tag `<input>` com o atributo "type" definido como "reset".

É possível estilizar os formulários usando CSS, e também é possível adicionar validação de formulário usando JavaScript para garantir que os usuários preencham os campos corretamente antes de enviar o formulário.

## Exercícios de Fixação

- 08 - Crie um formulário de cadastro de usuário com os seguintes campos: nome, sobrenome, e-mail, telefone e senha. Adicione um botão para enviar o formulário e outro para limpar os campos.

- 09 - Crie um formulário de contato com os seguintes campos: nome, e-mail, assunto e mensagem. Adicione um botão para enviar o formulário e outro para limpar os campos.
