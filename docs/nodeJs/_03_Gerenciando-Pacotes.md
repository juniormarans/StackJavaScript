## 3. Instale os Pacotes, Bibliotecas e Frameworks necessários

Embora os pacotes, bibliotecas e frameworks possam ter algumas semelhanças, eles são diferentes em sua finalidade e escopo, entenda melhor:

- **Pacote:** Um pacote é um conjunto de arquivos que podem ser facilmente compartilhados e reutilizados entre diferentes projetos em uma determinada linguagem de programação. Esses pacotes geralmente contêm módulos de código que fornecem funcionalidades específicas, como a manipulação de arquivos, a criação de servidores web, a integração com serviços externos e muito mais.

- **Biblioteca:** Uma biblioteca, por sua vez, é um conjunto de código pré-escrito que fornece funções ou classes reutilizáveis para realizar tarefas específicas em um projeto. Essas funções ou classes podem ser incorporadas diretamente no código do projeto em questão. As bibliotecas geralmente são projetadas para serem usadas em conjunto com outras bibliotecas ou com o código personalizado do projeto para fornecer uma solução completa.

- **Framework:** Já um framework é uma estrutura abrangente que fornece uma base para o desenvolvimento de software em geral. Ele inclui não apenas pacotes e bibliotecas, mas também convenções e padrões que orientam o processo de desenvolvimento. Os frameworks geralmente são voltados para a criação de um tipo específico de software, como aplicativos web, aplicativos móveis, jogos, etc

Os pacotes, bibliotecas e frameworks são gerenciados pelo sistema de gerenciamento de pacotes da linguagem de programação em questão (por exemplo, npm para Node.js, pip para Python) e podem ser instalados facilmente em um projeto com o comando apropriado.

### Instale os pacotes necessários para criar uma API RESTful em Node.js

Há várias razões pelas quais é benéfico utilizar pacotes, bibliotecas e frameworks no desenvolvimento de software:

1. Reutilização de código: Os pacotes e frameworks já têm um código escrito e testado que pode ser reutilizado para adicionar funcionalidades ao seu projeto. Isso economiza tempo e esforço para o desenvolvedor.

2. Aumento da produtividade: Os pacotes e frameworks permitem que os desenvolvedores trabalhem mais rapidamente, uma vez que não precisam escrever o código do zero. Eles podem se concentrar em implementar a lógica de negócios específica do projeto.

3. Padronização: Os pacotes e frameworks fornecem padrões e convenções para o desenvolvimento, tornando o código mais consistente e fácil de entender para outros desenvolvedores.

4. Gerenciamento de dependências: Os pacotes e frameworks geralmente gerenciam suas próprias dependências, garantindo que todas as bibliotecas necessárias sejam instaladas corretamente e em suas versões adequadas.

5. Segurança: Os pacotes e frameworks são desenvolvidos e mantidos por uma comunidade de desenvolvedores, o que significa que eles são frequentemente revisados e atualizados para corrigir quaisquer problemas de segurança.

6. Suporte: Os pacotes e frameworks geralmente têm documentação detalhada e uma comunidade de desenvolvedores pronta para ajudar em caso de problemas.

Em resumo, o uso de pacotes e frameworks pode economizar tempo, aumentar a produtividade, garantir a qualidade do código e melhorar a segurança do software.

Existem diversos pacotes que podem ser utilizados para criar uma API RESTful em Node.js. Alguns dos mais populares incluem:

### Framework Express

O Express é um framework para construção de aplicações web em Node.js. Foi criado por TJ Holowaychuk em 2010 e rapidamente se tornou um dos frameworks mais populares para desenvolvimento web em Node.js.

Desde sua criação, o Express passou por várias atualizações e melhorias significativas, evoluindo para se tornar uma das ferramentas mais usadas para desenvolvimento web em Node.js.

Algumas das principais evoluções do Express são:

- Versão 1.x: lançada em 2010, a primeira versão do Express foi desenvolvida por TJ Holowaychuk em resposta à falta de um framework de aplicação web simples e flexível para Node.js na época. A versão 1.x foi baseada em outro framework para Node.js chamado Connect, que fornecia middleware para a construção de aplicativos web. O Express expandiu a funcionalidade do Connect e tornou-se o framework mais popular para o desenvolvimento web em Node.js.

- Versão 2.x: lançada em 2011, a versão 2.x do Express introduziu suporte para roteamento, que permitiu que os desenvolvedores criassem rotas personalizadas para seus aplicativos. Isso tornou o Express ainda mais flexível e poderoso para construção de aplicativos web.

- Versão 3.x: lançada em 2012, a versão 3.x do Express trouxe melhorias significativas no desempenho e segurança do framework. Além disso, a versão 3.x adicionou suporte para middleware de aplicativos, o que permitiu que os desenvolvedores criassem aplicativos compostos de vários aplicativos menores.

- Versão 4.x: lançada em 2014, a versão 4.x do Express é a versão mais recente e popular do framework até o momento. Ela introduziu várias melhorias e recursos novos, incluindo uma nova API de roteamento, melhor suporte para middleware, melhorias na manipulação de erros e muito mais. A versão 4.x também apresentou melhorias significativas no desempenho e estabilidade do framework.

O Express continua a evoluir e ser atualizado com frequência, acompanhando as necessidades dos desenvolvedores web em constante mudança e mantendo-se como uma das ferramentas mais populares é um framework para Node.js que fornece recursos avançados para criar APIs RESTful e aplicativos web em geral, pode ser instalado através do `npm` com o comando:

  ```bash
  npm i express

  ```

### Pacote Body-parser

O `body-parser` é um middleware do Node.js usado para extrair os dados enviados pelo cliente no corpo (body) da requisição HTTP. Em outras palavras, ele é responsável por analisar o corpo da requisição e converter seus dados em um objeto JavaScript utilizável pela aplicação.

Quando um cliente envia uma requisição HTTP com dados no corpo, esses dados são geralmente codificados em um dos formatos mais comuns, como JSON, URL-encoded ou multipart. O `body-parser` é capaz de analisar e extrair esses dados independentemente do formato utilizado.

O `body-parser` é fácil de usar e pode ser adicionado como middleware em um aplicativo Express, por exemplo. É comum utilizá-lo em conjunto com o método `POST` do protocolo HTTP, que é utilizado para enviar dados do cliente para o servidor. Com o `body-parser`, é possível acessar esses dados no corpo da requisição dentro do código do servidor.

Vale lembrar que o `body-parser` foi integrado ao próprio Express a partir da versão 4.16.0, portanto, não é mais necessário instalá-lo separadamente se você estiver usando uma versão mais recente do Express. é um pacote que analisa o corpo das solicitações HTTP e extrai os dados enviados pelos clientes para o servidor em formato JSON ou URL-encoded, pode ser instalado através do `npm` com o comando:

  ```bash
  npm i body-parser 

  ```

### CORS e Biblioteca cors

O CORS um mecanismo de segurança implementado pelos navegadores web para proteger os usuários de requisições maliciosas feitas por scripts em sites diferentes.

No contexto de APIs Node.js, o CORS é geralmente implementado através do uso de uma biblioteca, como o `cors` ou o `helmet`, que adiciona os cabeçalhos CORS apropriados às respostas HTTP enviadas pelo servidor. O pacote `cors` é uma das bibliotecas mais comuns utilizadas em projetos Node.js para lidar com o controle de acesso HTTP e permite que os desenvolvedores configurem facilmente as políticas CORS que sua API seguirá.

para instalar o cors execute o camando:

  ```bash
  npm i cors 

  ```

Ao final desta etapa você terá a seguinte estrutura de diretório:

```tree
nome-do-projeto/
  |- node_modules/
  |- package-lock.json
  |- package.json

```

- `node_modules/`: é o diretório onde os pacotes de terceiros instalados pelo npm são armazenados.
- `package-lock.json`: é um arquivo gerado automaticamente pelo npm para garantir que as dependências do projeto sejam instaladas com a mesma versão, mesmo que o arquivo `package.json` tenha um caractere curinga `^` em suas dependências.
