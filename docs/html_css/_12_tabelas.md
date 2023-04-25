# Tabelas

As tabelas HTML são usadas para exibir dados em linhas e colunas. As tabelas são compostas de células que são organizadas em linhas e colunas.

```html
  <table>
    <tr>
      <th>Nome</th>
      <th>Email</th>
    </tr>
    <tr>
      <td>João</td>
      <td>joao@example.com</td>
    </tr>
    <tr>
      <td>Maria</td>
      <td>maria@example.com</td>
    </tr>
  </table>
```

Neste exemplo, a tag `<table>` é usada para criar a tabela. As linhas da tabela são criadas com a tag `<tr>`, que representa uma linha. As células da tabela são criadas com a tag `<td>`, que representa uma célula de dados. As células de cabeçalho da tabela são criadas com a tag `<th>`, que representa uma célula de cabeçalho.

A primeira linha da tabela contém as células de cabeçalho. A segunda e terceira linhas contêm as células de dados.

Além disso, as tabelas HTML suportam alguns atributos adicionais, como border, que define a largura da borda da tabela, e cellpadding e cellspacing, que definem o espaçamento entre as células da tabela.

## Mais tags de tabelas

As tags `<thead>`, `<tbody>` e `<tfoot>` são usadas para dividir uma tabela HTML em seções separadas, tornando-a mais fácil de ler e compreender.

A tag `<thead>` é usada para criar um cabeçalho de tabela, que normalmente inclui os títulos das colunas. A tag `<tbody>` é usada para criar o corpo da tabela, que contém as linhas e células de dados. A tag `<tfoot>` é usada para criar um rodapé de tabela, que normalmente inclui resumos e totais.

```html
  <table>
    <thead>
      <tr>
        <th>Produto</th>
        <th>Preço</th>
        <th>Quantidade</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Maçãs</td>
        <td>$2.00</td>
        <td>10</td>
      </tr>
      <tr>
        <td>Bananas</td>
        <td>$1.50</td>
        <td>15</td>
      </tr>
      <tr>
        <td>Laranjas</td>
        <td>$2.50</td>
        <td>5</td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td>Total</td>
        <td></td>
        <td>30</td>
      </tr>
    </tfoot>
  </table>
```

Neste exemplo, a tag `<thead>` é usada para criar o cabeçalho da tabela com as células de cabeçalho `<th>`. A tag `<tbody>` é usada para criar o corpo da tabela com as células de dados `<td>`. A tag `<tfoot>` é usada para criar o rodapé da tabela com a célula Total.

Note que a célula de preço na tag `<tfoot>` está em branco, já que não faz sentido somar preços.

Ao dividir a tabela em seções com essas tags, é possível aplicar estilos diferentes a cada seção usando CSS, tornando a tabela mais estilizada e fácil de ler.

As tabelas HTML são frequentemente usadas para exibir dados tabulares, como informações de contato, preços de produtos e horários de eventos. É importante lembrar que as tabelas HTML devem ser usadas apenas para dados tabulares e não para formatação de layout. Para isso, é recomendado o uso de CSS.
