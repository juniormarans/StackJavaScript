## Introdução

A programação orientada a objetos (POO) é um paradigma de programação em que os objetos são os principais componentes. Em POO, os objetos são criados a partir de classes, que são como "plantas baixas" para os objetos. Uma classe define as propriedades e os métodos que um objeto pode ter. Em JavaScript, podemos criar classes e objetos usando a sintaxe de classe.

## Definição de classe

Para criar uma classe em JavaScript, usamos a palavra-chave `class`. No exemplo abaixo, definimos uma classe chamada `Carro`. A classe tem um construtor que inicializa as propriedades marca, modelo e ano. Também definimos um **método** acelerar, que simplesmente imprime uma mensagem no console.

```javascript
class Carro {
  constructor(marca, modelo, ano) {
    this.marca = marca;
    this.modelo = modelo;
    this.ano = ano;
  }

  acelerar() {
    console.log(`O ${this.modelo} está acelerando!`);
  }
}
```

Neste exemplo, definimos uma classe chamada `Carro`. A classe tem um construtor que inicializa as propriedades `marca`, `modelo` e `ano`. Também definimos um método `acelerar`, que simplesmente é uma função que é definida dentro de uma classe e pode ser invocada em instâncias dessa classe. As classes são uma sintaxe de programação orientada a objetos introduzida no ECMAScript 2015 (ES6) e fornecem uma maneira mais clara e fácil de criar objetos em JavaScript.

## Instanciação de objetos

Uma instância de classe em JavaScript é um **objeto** criado a partir de uma classe. Quando você instancia uma classe, você está criando um novo objeto que herda os métodos e propriedades da classe. Em outras palavras, uma instância de classe é uma cópia única da classe que contém seus próprios valores de propriedades.

Para criar uma instância da classe `Carro`, usamos a palavra-chave `new`. Aqui está um exemplo:

```javascript
let meuCarro = new Carro("Ford", "Mustang", 2022);
```

Neste exemplo, criamos um novo objeto `meuCarro` que é uma instância da classe `Carro`. Passamos três argumentos para o construtor da classe para definir as propriedades do carro.

Podemos acessar as propriedades e métodos do objeto da seguinte maneira:

```javascript
console.log(meuCarro.marca); // Ford
console.log(meuCarro.acelerar()); // O Mustang está acelerando!
```

## Encapsulamento

O encapsulamento é o conceito de ocultar a complexidade de implementação de um objeto e expor apenas o que é necessário para o uso externo. Em JavaScript, não há suporte nativo para encapsulamento, mas é possível simular esse conceito usando funções construtoras e closures.

Aqui está um exemplo de como podemos simular o encapsulamento em JavaScript:

```javascript
function ContaBancaria(saldoInicial) {
  let saldo = saldoInicial;

  this.getSaldo = function() {
    return saldo;
  };

  this.depositar = function(valor) {
    saldo += valor;
  };

  this.sacar = function(valor) {
    if (saldo >= valor) {
      saldo -= valor;
    } else {
      console.log("Saldo insuficiente");
    }
  };
}

let minhaConta = new ContaBancaria(1000);

console.log(minhaConta.getSaldo()); // 1000

minhaConta.depositar(500);

console.log(minhaConta.getSaldo()); // 1500

minhaConta.sacar(2000); // Saldo insuficiente

minhaConta.sacar(1000);

console.log(minhaConta.getSaldo()); // 500
```

Neste exemplo, temos uma função construtora `ContaBancaria` que simula uma conta bancária. A variável `saldo` é declarada dentro da função e não é exposta ao código externo. Em vez disso, expomos métodos públicos para acessar e manipular o saldo da conta bancária: `getSaldo`, `depositar` e `sacar`.

## Herança

Herança é um conceito importante na programação orientada a objetos, e em JavaScript podemos implementá-lo usando a palavra-chave `extends`. Quando uma classe estende outra classe, ela herda suas propriedades e métodos. Aqui está um exemplo:

```javascript
class Animal {
  constructor(nome) {
    this.nome = nome;
  }

  fazerBarulho() {
    console.log(`${this.nome} está fazendo barulho.`);
  }
}

class Cachorro extends Animal {
  constructor(nome, raca) {
    super(nome);
    this.raca = raca;
  }

  latir() {
    console.log(`${this.nome} (${this.raca}) está latindo.`);
  }
}
```

Neste exemplo, temos duas classes: `Animal` e `Cachorro`. A classe `Cachorro` estende a classe `Animal` usando a palavra-chave `extends`. Isso significa que a classe `Cachorro` herda a propriedade `nome` e o método `fazerBarulho` da classe `Animal`.

Além disso, a classe `Cachorro` tem sua própria propriedade `raca` e seu próprio método `latir`. Observe que o método `latir` usa a propriedade `nome` da classe `Animal`, bem como a propriedade `raca` da classe `Cachorro`.

Agora, vamos criar um objeto `meuCachorro` que é uma instância da classe `Cachorro`:

```javascript
let meuCachorro = new Cachorro("Fido", "Labrador Retriever");
```

Podemos acessar as propriedades e métodos do objeto da seguinte maneira:

```javascript
console.log(meuCachorro.nome); // Fido
console.log(meuCachorro.raca); // Labrador Retriever
console.log(meuCachorro.fazerBarulho()); // Fido está fazendo barulho.
console.log(meuCachorro.latir()); // Fido (Labrador Retriever) está latindo.
```

## Polimorfismo

Polimorfismo é outro conceito importante na programação orientada a objetos. Em JavaScript, podemos implementar o polimorfismo usando a mesma assinatura de método em várias classes diferentes. Aqui está um exemplo:

```javascript
class Animal {
  constructor(nome) {
    this.nome = nome;
  }

  fazerBarulho() {
    console.log(`${this.nome} está fazendo barulho.`);
  }
}

class Cachorro extends Animal {
  constructor(nome, raca) {
    super(nome);
    this.raca = raca;
  }

  fazerBarulho() {
    console.log(`${this.nome} (${this.raca}) está latindo.`);
  }
}

class Gato extends Animal {
  constructor(nome, cor) {
    super(nome);
    this.cor = cor;
  }

  fazerBarulho() {
    console.log(`${this.nome} (${this.cor}) está miando.`);
  }
}
```

Neste exemplo, temos três classes: `Animal`, `Cachorro` e `Gato`. Todas essas classes têm um método `fazerBarulho`, mas cada uma delas o implementa de maneira diferente. Quando chamamos o método `fazerBarulho` em um objeto, o JavaScript chama o método correto, dependendo do tipo do objeto.

Agora, vamos criar um exemplo de uso do polimorfismo com as classes `Cachorro` e `Gato`:

```javascript
const cachorro = new Cachorro('Rex', 'Golden Retriever');
const gato = new Gato('Miau', 'preto');

cachorro.fazerBarulho(); // Saída: "Rex (Golden Retriever) está latindo."
gato.fazerBarulho(); // Saída: "Miau (preto) está miando."
```

Observe que mesmo chamando o mesmo método `fazerBarulho`, a saída é diferente para cada objeto, pois cada classe implementa esse método de forma diferente.

## Métodos estáticos

Em JavaScript, também podemos definir métodos estáticos em uma classe. Métodos estáticos são métodos que pertencem à classe em si, em vez de pertencerem a uma instância da classe. Aqui está um exemplo:

```javascript
class Utilitarios {
  static formatarNumero(numero) {
    return numero.toLocaleString("pt-BR");
  }
}

console.log(Utilitarios.formatarNumero(1000)); // 1.000
```

Neste exemplo, definimos um método estático chamado `formatarNumero` na classe `Utilitarios`. Esse método não é acessível a partir de instâncias da classe, apenas a partir da própria classe.

---

- A programação orientada a objetos é um paradigma importante para a escrita de código estruturado e reutilizável. Em JavaScript, podemos utilizar classes, herança, encapsulamento, polimorfismo e outros conceitos da orientação a objetos para criar código mais legível e organizado. Com esses conceitos em mente, podemos criar soluções mais eficientes e escaláveis para nossos projetos em JavaScript.

---

## Pacotes

Um pacote em JavaScript é um conjunto de código que pode ser facilmente compartilhado entre projetos. Se você está trabalhando em um projeto que usa um conjunto de funcionalidades que você gostaria de reutilizar em outros projetos, pode ser útil criar um pacote para essas funcionalidades. Neste artigo, vamos ver como criar um pacote em JavaScript para uso interno, ou seja, que não será publicado no registro de pacotes do NPM.

O primeiro passo para criar um pacote em JavaScript é criar uma nova pasta com o nome que desejar para o seu pacote. Você pode criar essa pasta em qualquer lugar do seu computador. Por exemplo, você pode criar uma pasta chamada "meu-pacote" em sua área de trabalho.

Dentro da pasta que você acabou de criar, execute o comando "npm init" no terminal. Isso irá criar um arquivo "package.json" para gerenciar as dependências do seu pacote. Siga as instruções na linha de comando para preencher as informações do seu pacote, como o nome, versão, descrição, etc. Essas informações podem ser alteradas posteriormente.

```bash
cd meu-pacote
npm init
```

Agora que o projeto está inicializado, é hora de começar a escrever o código que você deseja incluir no pacote. Este pode ser um único arquivo ou vários arquivos em um diretório. Para este exemplo, vamos criar uma função simples que calcula a soma de dois números.

Crie um novo arquivo chamado "minhas-funcoes.js" dentro da pasta "meu-pacote" e adicione o seguinte código:

```javascript
module.exports = {
  soma: function(a, b) {
    return a + b;
  }
};
```

Crie um arquivo "index.js" na raiz da pasta do seu pacote. Este arquivo será a entrada do seu pacote e irá exportar as funcionalidades que você deseja disponibilizar. No nosso caso, vamos exportar a função "soma" que acabamos de criar.

```javascript
const minhasFuncoes = require('./minhas-funcoes');

module.exports = {
  soma: minhasFuncoes.soma
};
```

Agora que você criou o pacote, é hora de testá-lo. Para fazer isso, crie um novo projeto em um diretório separado e adicione o seu pacote como uma dependência.

```bash
mkdir meu-projeto
cd meu-projeto
npm init
npm install ../meu-pacote
```

Em seguida, crie um arquivo "index.js" em seu novo projeto e importe a função "soma" do seu pacote.

```javascript
const meuPacote = require('meu-pacote');

console.log(meuPacote.soma(2, 3)); // Output: 5
```

Execute o arquivo "index.js" usando o Node.js.

```bash
node index.js
```

Se o output for "5", isso significa que o seu pacote está funcionando corretamente.

Criar um pacote em JavaScript pode ser uma maneira útil de reutilizar código em vários projetos. Neste artigo, você aprendeu a criar um pacote em JavaScript para uso interno, sem publicá-lo no registro de pacotes do NPM. Lembre-se de que este é apenas um exemplo simples e que há muitas maneiras de criar pacotes mais complexos e robustos em JavaScript.
