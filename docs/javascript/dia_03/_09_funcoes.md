# Funções

Uma função em JavaScript é um bloco de código que executa uma tarefa específica. As funções são usadas para modularizar o código, tornando-o mais fácil de ler e manter. As funções também são usadas para reutilizar código, permitindo que você escreva uma vez e use várias vezes em seu programa.

Sintaxe de Função em JavaScript

A sintaxe básica de uma função em JavaScript é a seguinte:

```javascript
function nome_da_funcao(parametro1, parametro2, ..., parametroN) {
   // Bloco de código que executa a tarefa da função
}
```

Onde:

- `nome_da_funcao`: é o nome que você escolhe para sua função.
- `parametro1, parametro2, ..., parametroN`: são os parâmetros opcionais que você pode passar para a função. Os parâmetros são usados para receber valores que a função irá processar.
- `Bloco de código que executa a tarefa da função`: é o código que a função irá executar quando for chamada.

Por exemplo, vamos criar uma função simples que recebe dois parâmetros e retorna a soma desses parâmetros:

```javascript
function somar(valor1, valor2) {
   return valor1 + valor2;
}
```

Chamando uma Função em JavaScript

Uma vez que você tenha criado uma função, você pode chamá-la em qualquer lugar em seu programa. Para chamar uma função, você simplesmente usa seu nome seguido por parênteses com os argumentos (se houver) que você deseja passar para a função.

Por exemplo, para chamar a função `somar` que criamos anteriormente, você pode fazer o seguinte:

```javascript
var resultado = somar(2, 3);
console.log(resultado); // Saída: 5
```

O que aconteceu aqui é que chamamos a função `somar` passando os valores `2` e `3` como argumentos. A função `somar` então retorna a soma desses valores, que é `5`, que é atribuído à variável `resultado`. Em seguida, imprimimos o resultado usando a função `console.log`.

Retorno de Valores em Funções em JavaScript

As funções em JavaScript podem retornar valores usando a palavra-chave `return`. Quando uma função encontra a palavra-chave `return`, ela interrompe a execução e retorna um valor para quem chamou a função.

Por exemplo, considere a seguinte função que verifica se um número é par ou ímpar:

```javascript
function par_ou_impar(numero) {
   if(numero % 2 === 0) {
      return "par";
   } else {
      return "ímpar";
   }
}
```

Podemos chamar essa função e armazenar o resultado em uma variável:

```javascript
var resultado = par_ou_impar(3);
console.log(resultado); // Saída: "ímpar"
```

Parâmetros de Funções em JavaScript

As funções em JavaScript podem receber parâmetros para processar valores específicos. Os parâmetros são passados ​​para a função como argumentos quando a função é chamada. Os parâmetros são opcionais e você pode passar quantos parâmetros desejar.

Por exemplo, a função `somar` que criamos anteriormente recebe dois parâmetros. Você pode passar qualquer valor para esses parâmetros, desde que correspondam ao tipo de dados que a função espera.

```javascript
function somar(valor1, valor2) {
   return valor1 + valor2;
}

var resultado = somar(2, 3);
console.log(resultado); // Saída: 5
```

Aqui, a função `somar` espera dois parâmetros, `valor1` e `valor2`, que são usados ​​para somar os valores e retornar o resultado.

## Funções Anônimas em JavaScript

Em JavaScript, você pode criar funções anônimas, que são funções que não possuem nome. As funções anônimas são usadas em situações em que você precisa passar uma função como argumento para outra função.

Por exemplo, a função `setTimeout` em JavaScript espera uma função como argumento para ser executada após um certo período de tempo.

```javascript
setTimeout(function() {
   console.log("Executado após 3 segundos");
}, 3000);
```

Aqui, passamos uma função anônima como argumento para `setTimeout`. A função será executada após 3 segundos e imprimirá a mensagem "Executado após 3 segundos" no console.

Funções são uma parte fundamental de JavaScript e são usadas para modularizar o código, tornando-o mais fácil de ler e manter. As funções também são usadas para reutilizar código, permitindo que você escreva uma vez e use várias vezes em seu programa. Até agora, discutimos a sintaxe básica de uma função em JavaScript, como chamar funções, retornar valores e usar funções anônimas. Com uma compreensão sólida de como as funções funcionam em JavaScript, você estará pronto para escrever código mais complexo e eficiente em JavaScript.

## CALLBACK

Em JavaScript, um callback é uma função que é passada como argumento para outra função e é executada quando essa função é concluída. O termo "callback" é usado porque a função passada é "chamada de volta" para executar uma ação adicional.

Callbacks são comuns em JavaScript porque a linguagem permite o uso de funções como valores de variáveis, tornando-as cidadãos de primeira classe na linguagem. Isso significa que as funções podem ser tratadas como qualquer outra variável, incluindo passá-las como argumentos para outras funções.

Callbacks são frequentemente usados para lidar com tarefas assíncronas em JavaScript, como fazer chamadas de API ou ler arquivos, onde é necessário esperar uma resposta antes de executar uma ação adicional. Em vez de bloquear a execução do programa enquanto espera pela resposta, o código pode continuar executando e chamar o callback quando a resposta for recebida.

Por exemplo, a função `setTimeout()` em JavaScript é um exemplo comum de uma função que usa callbacks. A função `setTimeout()` recebe dois argumentos: uma função de callback e um tempo em milissegundos. A função de callback é executada depois que o tempo especificado passa:

```javascript
setTimeout(function() {
  console.log('Essa mensagem será exibida após 3 segundos');
}, 3000);
```

Nesse exemplo, uma função anônima é passada como um callback para a função `setTimeout()`. Essa função de callback será chamada após um atraso de 3 segundos.

Callbacks são uma parte fundamental do modelo de programação assíncrona em JavaScript, e são amplamente usados em bibliotecas e frameworks populares, como jQuery, React, Node.js, entre outros.

## PROMISE

Em JavaScript, `Promise` é um objeto que representa a eventual conclusão (ou falha) de uma operação assíncrona e seu resultado. A ideia básica é que, em vez de esperar que uma operação assíncrona seja concluída antes de continuar a execução do código, podemos criar uma promessa que será resolvida posteriormente com o resultado da operação.

A promessa pode estar em um de três estados: pendente, resolvida ou rejeitada. Quando a promessa está pendente, a operação assíncrona ainda está em andamento. Quando a operação é concluída com sucesso, a promessa é resolvida com o resultado da operação. Se a operação falhar, a promessa é rejeitada com um motivo de erro.

As promessas podem ser usadas para simplificar o código em comparação com o uso de callbacks. Em vez de aninhar várias funções de callback, podemos encadear várias promessas em uma cadeia, usando os métodos `then()` e `catch()`. O método `then()` é usado para lidar com a resolução bem-sucedida da promessa, enquanto o método `catch()` é usado para lidar com a rejeição da promessa.

Abaixo, segue um exemplo simples de como usar uma promessa em JavaScript:

```javascript
function multiplica_por_dois(valor) {
  return new Promise((resolve, reject) => {
    if (typeof valor === 'number') {
      resolve(valor * 2);
    } else {
      reject(new Error('O argumento não é um número.'));
    }
  });
}

multiplica_por_dois(4)
  .then(result => {
    console.log(result); // Resultado: 8
  })
  .catch(error => {
    console.error(error.message);
  });
```

Neste exemplo, a função `multiplica_por_dois()` retorna uma nova promessa que é resolvida com o resultado da multiplicação por dois do argumento passado. Se o argumento não for um número, a promessa é rejeitada com um objeto de erro.

Fora da função, usamos o método `then()` para acessar o valor resolvido da promessa e imprimir o resultado da multiplicação. Também usamos o método `catch()` para lidar com quaisquer erros que possam ocorrer na execução da promessa.

Em resumo, as promessas são objetos que representam a conclusão (ou falha) de uma operação assíncrona e seu resultado. Elas são usadas para simplificar o código em comparação com o uso de callbacks e podem ser encadeadas em uma cadeia usando os métodos `then()` e `catch()`.

## ASYNC/AWAIT

Em JavaScript, `async`/`await` é uma forma de lidar com tarefas assíncronas que simplifica a sintaxe em relação ao uso de callbacks e promessas. `async` é uma palavra-chave que pode ser usada para declarar uma função assíncrona, que retorna uma promessa que será resolvida com o valor retornado pela função. `await` é uma palavra-chave que pode ser usada dentro de uma função assíncrona para aguardar a resolução de uma promessa antes de continuar a execução do código.

O uso de `async`/`await` pode tornar o código mais legível e fácil de manter em comparação com o uso de callbacks ou promessas. Em vez de aninhar várias funções de callback ou encadear várias promessas, o código pode ser escrito de forma mais sequencial, parecendo com código síncrono. Isso pode tornar o código mais fácil de entender e depurar.

Veja um exemplo simples abaixo para ilustrar o uso de `async`/`await` em JavaScript:

```javascript
async function fetchUserData(userId) {
  const response = await fetch(`https://api.example.com/users/${userId}`);
  const userData = await response.json();
  return userData;
}

fetchUserData(123)
  .then(userData => {
    console.log(`Nome do usuário: ${userData.name}`);
  })
  .catch(error => {
    console.error(error);
  });
```

Neste exemplo, a função `fetchUserData()` é declarada com a palavra-chave `async`. Dentro da função, usamos `await` para aguardar a resposta da API antes de transformar a resposta em um objeto JSON. A função retorna o objeto JSON, que é resolvido como um valor de promessa quando a função é concluída.

Fora da função, chamamos a função `fetchUserData()` passando um ID de usuário como argumento. Em seguida, usamos o método `then()` para acessar o valor resolvido da promessa e imprimir o nome do usuário. Também usamos o método `catch()` para lidar com quaisquer erros que possam ocorrer na execução da função assíncrona.

Em resumo, `async`/`await` é uma forma mais elegante e fácil de ler e escrever código assíncrono em JavaScript. Algumas situações comuns em que você pode querer usar `async`/`await` em vez de callbacks ou promessas são:

1. Fazer requisições assíncronas de dados em uma API;
2. Ler ou gravar arquivos em um sistema de arquivos;
3. Acessar bancos de dados;
4. Executar tarefas assíncronas em segundo plano;
5. Executar tarefas assíncronas complexas que dependem de outras operações assíncronas.

Além disso, o uso de `async`/`await` pode tornar o código mais legível e fácil de manter em comparação com o uso de callbacks ou promessas. Em vez de aninhar várias funções de callback ou encadear várias promessas, o código pode ser escrito de forma mais sequencial, parecendo com código síncrono. Isso pode tornar o código mais fácil de entender e depurar.

No entanto, é importante lembrar que o uso excessivo de `async`/`await` pode levar a problemas de desempenho, pois a execução de uma função assíncrona pode bloquear a execução do thread principal do aplicativo. Portanto, é importante avaliar cuidadosamente a complexidade da tarefa assíncrona e se a abordagem `async`/`await` é a melhor para ela.
