# JavaScript

JavaScript é uma linguagem de programação de alto nível, dinâmica e interpretada. Ela foi criada por Brendan Eich em 1995 enquanto trabalhava na Netscape Communications Corporation, e atualmente é uma das linguagens mais populares do mundo. JavaScript é amplamente utilizada para criar e manipular conteúdo dinâmico em páginas da web, permitindo que desenvolvedores adicionem interatividade a sites e aplicativos da web.

A linguagem JavaScript é baseada em objetos e é executada no lado do cliente, ou seja, no navegador do usuário. Ela é usada para criar animações, validar formulários, atualizar conteúdo dinamicamente e realizar diversas outras funcionalidades que melhoram a experiência do usuário na web. Além disso, JavaScript também é utilizada em outras áreas, como no desenvolvimento de aplicativos de desktop, servidores web e até mesmo na criação de jogos.

JavaScript é uma linguagem de programação bastante versátil e tem uma sintaxe relativamente simples, o que torna mais fácil para os iniciantes aprenderem. Ela também possui uma grande variedade de bibliotecas e frameworks disponíveis, que ajudam a simplificar o processo de desenvolvimento de aplicativos da web.

## Como Rodar Um Código JavaScript

Escolha um ambiente para rodar seu código JavaScript. Existem várias opções para rodar um código JavaScript, dependendo do seu propósito. Algumas opções incluem:

- Usar o console do navegador: Para rodar código JavaScript no navegador, abra o console de desenvolvedor pressionando F12 e selecione a guia "Console". Digite seu código JavaScript diretamente no console e pressione Enter para rodar.
- Usar o Node.js: O Node.js é uma plataforma para rodar código JavaScript no lado do servidor. Para usar o Node.js, você precisa instalar o software primeiro.
- Usar um ambiente de desenvolvimento integrado (IDE): Existem muitos IDEs disponíveis para programação em JavaScript, como Visual Studio Code, Atom, Sublime Text, etc. Eles têm recursos avançados de depuração e autocompletar.

### Utilizando o console do navegador

Passo 1: Crie um arquivo HTML
Crie um novo arquivo HTML em qualquer editor de texto. Cole o seguinte código HTML no arquivo:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu tutorial JavaScript</title>
</head>
<body>
    <h1>Meu tutorial JavaScript</h1>
    <script>
        // Seu código JavaScript aqui
    </script>
</body>
</html>
```

Salve o arquivo com o nome descritivo do que ele faz, por exemplo "saudacao.html".

Passo 2: Adicione seu código JavaScript
dentro da tag `<script>` no arquivo HTML, adicione seu código JavaScript. Por exemplo, o seguinte código exibe um alerta na tela:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu tutorial JavaScript</title>
</head>
<body>
    <h1>Meu tutorial JavaScript</h1>
    <script>
        console.log("Olá, mundo!");
    </script>
</body>
</html>
```

Salve o arquivo.

Passo 3: Abra o arquivo HTML no navegador
Abra o arquivo HTML no navegador, clicando duas vezes no arquivo, arrastando e soltando sobre um navegador ou usando o menu "Abrir arquivo" do navegador. O código JavaScript será executado automaticamente.

## executar JavaScript com o Node.js

Passo 1: Abra o terminal do seu sistema operacional.

Passo 2: Navegue até o diretório onde o seu arquivo JavaScript está localizado usando o comando `cd`.

Por exemplo, se o seu arquivo está na pasta `Documentos` dentro do diretório pessoal do seu usuário, você pode navegar até lá com o seguinte comando:

```bash
cd ~/Documentos
```

Passo 3: Execute o código JavaScript usando o comando `node` seguido do nome do arquivo.

Por exemplo, se o seu arquivo se chama `meuCodigo.js`, o comando para executá-lo seria:

```bash
node meuCodigo.js
```

Passo 4: O resultado da execução do código será exibido no terminal.

Se o seu código tem saída de dados usando `console.log`, ela será exibida no terminal após a execução do comando.

Por exemplo, se o seu código contém o seguinte comando:

```javascript
console.log("Hello, world!");
```

A saída será exibida no terminal assim que o comando `node meuCodigo.js` for executado:

```bash
Hello, world!
```

Pronto! Agora você já sabe como executar um código JavaScript com o Node.js. É importante lembrar que, para usar módulos externos em seu código, você precisa instalar as dependências com o gerenciador de pacotes do Node.js, o `npm`.
