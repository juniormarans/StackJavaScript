## TypeScript

TypeScript é um superset do JavaScript que adiciona recursos de tipagem estática e outras funcionalidades à linguagem. Ele foi desenvolvido pela Microsoft e é uma escolha popular para grandes projetos JavaScript.

### Configuração

Para começar a usar TypeScript, você precisa configurar um ambiente de desenvolvimento. Você pode instalar o TypeScript globalmente usando o npm com o seguinte comando:

```bash
npm install -g typescript
```

Depois de instalado, você pode criar um arquivo `.ts` e compilá-lo usando o comando `tsc`. Por exemplo, crie um arquivo `app.ts` com o seguinte código:

```typescript
function dizerOla(nome: string) {
  console.log(`Olá, ${nome}!`);
}

dizerOla('TypeScript'); // Olá, TypeScript!
```

Em seguida, compile o arquivo `app.ts` usando o comando `tsc app.ts`. Isso irá gerar um arquivo `app.js` que pode ser executado normalmente no Node.js ou em um navegador.

### Tipos básicos

Uma das principais funcionalidades do TypeScript é a tipagem estática. Isso significa que você pode especificar o tipo de dados que uma variável pode armazenar e o TypeScript irá verificar se você está usando a variável corretamente em tempo de compilação. Aqui estão alguns tipos básicos em TypeScript:

```typescript
// Números
let numero: number = 10;

// Strings
let texto: string = 'Olá';

// Booleanos
let booleano: boolean = true;

// Arrays
let lista: number[] = [1, 2, 3];
let lista2: Array<string> = ['a', 'b', 'c'];

// Tuplas
let tupla: [string, number] = ['olá', 10];

// Enums
enum Cor {
  Vermelho,
  Verde,
  Azul,
}
let cor: Cor = Cor.Vermelho;

// Any
let qualquerValor: any = 'olá';
```

Observe que você pode usar a sintaxe `let nomeVariavel: tipoVariavel = valor` para especificar o tipo de uma variável.

### Funções

As funções em TypeScript podem ter tipos de argumento e tipo de retorno especificados. Aqui está um exemplo:

```typescript
function somar(valor1: number, valor2: number): number {
  return valor1 + valor2;
}
```

Observe que o tipo de retorno é especificado após os tipos dos argumentos usando a sintaxe `function nomeFuncao(arg1: tipoArg1, arg2: tipoArg2): tipoRetorno`.

### Interfaces

As interfaces são uma maneira de definir tipos personalizados em TypeScript. Por exemplo, você pode definir uma interface para um objeto com propriedades específicas:

```typescript
interface Pessoa {
  nome: string;
  idade: number;
}

function cumprimentar(pessoa: Pessoa) {
  console.log(`Olá, ${pessoa.nome}! Você tem ${pessoa.idade} anos.`);
}

let alice: Pessoa = { nome: 'Alice', idade: 30 };
cumprimentar(alice); // Olá, Alice! Você tem 30 anos.
```

Observe que a função `cumprimentar` espera um objeto do tipo `Pessoa`.

### Classes

As classes em TypeScript permitem definir objetos com propriedades e métodos. Aqui está um exemplo:

```typescript
class Animal {
  nome: string;
  constructor(nome: string) {
    this.nome = nome;
  }
  fazerBarulho() {
    console.log('Barulho genérico de animal');
  }
}

class Cachorro extends Animal {
  fazerBarulho() {
    console.log('Au au!');
  }
}

let cachorro: Cachorro = new Cachorro('Rex');
console.log(cachorro.nome); // 'Rex'
cachorro.fazerBarulho(); // 'Au au!'
```

Observe que a classe `Cachorro` herda da classe `Animal` usando a sintaxe `class nomeClasse extends nomeClassePai`. A classe `Cachorro` sobrescreve o método `fazerBarulho` da classe `Animal`.
