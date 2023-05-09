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

- **Express:** é um framework para Node.js que fornece recursos avançados para criar APIs RESTful e aplicativos web em geral, pode ser instalado através do `npm` com o comando:

  ```bash
  npm i express

  ```

- **Body-parser:** é um pacote que analisa o corpo das solicitações HTTP e extrai os dados enviados pelos clientes para o servidor em formato JSON ou URL-encoded, pode ser instalado através do `npm` com o comando:

  ```bash
  npm i body-parser 

  ```

- **Cors:** é um pacote que permite configurar as políticas de segurança do CORS (Cross-Origin Resource Sharing) para sua API.

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
