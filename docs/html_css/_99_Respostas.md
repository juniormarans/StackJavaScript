# Respostas

## Atividade 01

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Perfil</title>
  </head>
  <body>
    <div>
      <img src="perfil.jpg" alt="Imagem de perfil">
      <h1>Nome do usuário</h1>
      <p>Uma breve descrição sobre mim...</p>
      <h2>Interesses:</h2>
      <p>- Interesse 1</p>
      <p>- Interesse 2</p>
      <p>- Interesse 3</p>
    </div>
  </body>
</html>
```

## Atividade 02

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Lista de Tarefas</title>
  </head>
  <body>
    <div>
      <h1>Minha Lista de Tarefas</h1>
      <div>
        <input type="checkbox" id="tarefa1" name="tarefa1" value="tarefa1">
        <label for="tarefa1">Tarefa 1</label>
      </div>
      <div>
        <input type="checkbox" id="tarefa2" name="tarefa2" value="tarefa2">
        <label for="tarefa2">Tarefa 2</label>
      </div>
      <div>
        <input type="checkbox" id="tarefa3" name="tarefa3" value="tarefa3">
        <label for="tarefa3">Tarefa 3</label>
      </div>
    </div>
  </body>
</html>
```

## Atividade 03

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Produto</title>
  </head>
  <body>
    <div>
      <img src="produto.jpg" alt="Imagem do produto">
      <h1>Nome do Produto</h1>
      <p>Preço: R$99,99</p>
      <p>Descrição do Produto...</p>
    </div>
  </body>
</html>
```

## Atividade 04

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Imagem de fundo responsiva</title>
    <style>
      body {
      background-image: url('imagem.jpg');
      background-size: cover;
      background-repeat: no-repeat;
      }
    </style>
  </head>
  <body>
    <div>
      <h1>Conteúdo da página...</h1>
      <p>Texto da página...</p>
    </div>
  </body>
</html>
```

## Atividade 05

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Elemento no rodapé da página</title>
    <style>
      body {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      margin: 0;
      padding: 0;
      }
      .conteudo {
      flex: 1;
      padding: 20px;
      }
      .rodape {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      background-color: #ddd;
      padding: 10px;
      }
    </style>
  </head>
  <body>
    <div class="conteudo">
      <h1>Conteúdo da página...</h1>
      <p>Texto da página...</p>
    </div>
    <div class="rodape">
      <p>Este é o rodapé da página</p>
    </div>
  </body>
</html>
```

## Atividade 06

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Menu Horizontal</title>
    <style>
      .menu {
      display: flex;
      list-style: none;
      padding: 0;
      margin: 0;
      background-color: #ddd;
      }
      .menu li {
      flex-grow: 1;
      text-align: center;
      }
      .menu a {
      display: block;
      padding: 10px;
      text-decoration: none;
      color: #333;
      }
    </style>
  </head>
  <body>
    <nav>
      <ul class="menu">
        <li><a href="#">Página 1</a></li>
        <li><a href="#">Página 2</a></li>
        <li><a href="#">Página 3</a></li>
        <li><a href="#">Página 4</a></li>
      </ul>
    </nav>
  </body>
</html>
```

## Atividade 07

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Empresa de Tecnologia</title>
  </head>
  <body>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#sobre-nos">Sobre Nós</a></li>
      <li><a href="#servicos">Serviços</a></li>
      <li><a href="#produtos">Produtos</a></li>
      <li><a href="#contato">Contato</a></li>
    </ul>
  </nav>
  <main>
    <section id="home">
      <h1>Bem-vindo à Empresa de Tecnologia</h1>
      <p>Conheça nossos produtos e serviços de tecnologia, voltados para a transformação digital dos nossos clientes.</p>
    </section>
    <section id="sobre-nos">
      <h2>Sobre Nós</h2>
      <p>Somos uma empresa de tecnologia focada em soluções inovadoras, que busca a excelência no atendimento e na entrega de projetos para nossos clientes.</p>
    </section>
    <section id="servicos">
      <h2>Serviços</h2>
      <ul>
        <li>Desenvolvimento de Software</li>
        <li>Desenvolvimento Web</li>
        <li>Consultoria em TI</li>
      </ul>
    </section>
    <section id="produtos">
      <h2>Produtos</h2>
      <p>Conheça nossos produtos tecnológicos, voltados para a transformação digital dos nossos clientes.</p>
    </section>
    <section id="contato">
      <h2>Contato</h2>
      <p>Entre em contato conosco para saber mais sobre nossos produtos e serviços de tecnologia.</p>
    </section>
  </main>
  </body>
</html>
```

## Atividade 08

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Cadastro de Usuário</title>
  </head>
  <body>
    <h1>Cadastro de Usuário</h1>
    <form>
      <label for="nome">Nome:</label>
      <input type="text" id="nome" name="nome" required>
      <label for="sobrenome">Sobrenome:</label>
      <input type="text" id="sobrenome" name="sobrenome" required>
      <label for="email">E-mail:</label>
      <input type="email" id="email" name="email" required>
      <label for="telefone">Telefone:</label>
      <input type="tel" id="telefone" name="telefone" required>
      <label for="senha">Senha:</label>
      <input type="password" id="senha" name="senha" required>
      <button type="submit">Enviar</button>
      <button type="reset">Limpar</button>
    </form>
  </body>
</html>
```

## Atividade 09

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Formulário de Contato</title>
  </head>
  <body>
    <h1>Formulário de Contato</h1>
    <form>
      <label for="nome">Nome:</label>
      <input type="text" id="nome" name="nome" required>
      <label for="email">E-mail:</label>
      <input type="email" id="email" name="email" required>
      <label for="assunto">Assunto:</label>
      <input type="text" id="assunto" name="assunto" required>
      <label for="mensagem">Mensagem:</label>
      <textarea id="mensagem" name="mensagem" required></textarea>
      <button type="submit">Enviar</button>
      <button type="reset">Limpar</button>
    </form>
  </body>
</html>
```

## Atividade 10

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Tabela de Alunos</title>
  </head>
  <body>
    <h1>Tabela de Alunos</h1>
    <table>
      <thead>
        <tr>
          <th>Nome</th>
          <th>Sobrenome</th>
          <th>Idade</th>
          <th>Média</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>João</td>
          <td>Silva</td>
          <td>18</td>
          <td>8.5</td>
        </tr>
        <tr>
          <td>Maria</td>
          <td>Santos</td>
          <td>19</td>
          <td>7.2</td>
        </tr>
        <tr>
          <td>Lucas</td>
          <td>Souza</td>
          <td>20</td>
          <td>9.1</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```

## Atividade 11

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Tabela de Produtos</title>
  </head>
  <body>
    <h1>Tabela de Produtos</h1>
    <table>
      <thead>
        <tr>
          <th>Produto</th>
          <th>Preço</th>
          <th>Disponibilidade</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Camisa</td>
          <td>R$ 50,00</td>
          <td>Em estoque</td>
        </tr>
        <tr>
          <td>Calça</td>
          <td>R$ 80,00</td>
          <td>Esgotado</td>
        </tr>
        <tr>
          <td>Sapato</td>
          <td>R$ 120,00</td>
          <td>Em estoque</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```

## Atividade 12

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Tabela de Funcionários</title>
  </head>
  <body>
  <h1>Tabela de Funcionários</h1>
  <table>
    <thead>
      <tr>
        <th>Nome</th>
        <th>Cargo</th>
        <th>Salário</th>
        <th>Data de Admissão</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>João Silva</td>
        <td>Analista de Sistemas</td>
        <td>R$ 5.000,00</td>
        <td>01/01/2021</td>
      </tr>
      <tr>
        <td>Maria Santos</td>
        <td>Coordenadora de Marketing</td>
        <td>R$ 7.500,00</td>
        <td>15/05/2019</td>
      </tr>
      <tr>
        <td>Lucas Souza</td>
        <td>Gerente de Vendas</td>
        <td>R$ 10.000,00</td>
        <td>10/10/2018</td>
      </tr>
    </tbody>
  </table>
  </body>
</html>
```
