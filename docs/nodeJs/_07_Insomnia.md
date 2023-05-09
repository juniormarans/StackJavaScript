## Insomnia

Insomnia é uma ferramenta de cliente REST que permite testar APIs HTTP. Com Insomnia, você pode enviar requisições HTTP para servidores e analisar as respostas.

### Instalando o Insomnia

Para começar, você precisa baixar e instalar o Insomnia em seu computador. Você pode fazer o download do Insomnia em seu [site oficial](https://insomnia.rest/download) ou através de gerenciadores de pacotes como o NPM.

```bash
# Add to sources
echo "deb [trusted=yes arch=amd64] https://download.konghq.com/insomnia-ubuntu/ default all" \
    | sudo tee -a /etc/apt/sources.list.d/insomnia.list

# Refresh repository sources and install Insomnia
sudo apt-get update
sudo apt-get install insomnia
```

### Criando uma requisição

- Para criar uma nova requisição, clique em "New Request" na barra lateral do Insomnia.
- Selecione o metódo GET.
- Insira a URL <https://viacep.com.br/ws/78048135/json/>
- Aperte Send

A resposta esperada é:

{
  "cep": "78048-135",
  "logradouro": "Avenida República do Líbano",
  "complemento": "(Lot Rodoviária Parque)",
  "bairro": "Despraiado",
  "localidade": "Cuiabá",
  "uf": "MT",
  "ibge": "5103403",
  "gia": "",
  "ddd": "65",
  "siafi": "9067"
}

Você pode adicionar mais cabeçalhos ou parâmetros de consulta, dependendo da API que estiver utilizando. Você também pode utilizar outros métodos HTTP, como POST, PUT ou DELETE. O Insomnia permite configurar todos esses detalhes na criação de sua requisição.

### Salvar e importar requisições

Se você precisa reutilizar uma requisição que já criou, pode salvá-la clicando em "Save" na barra superior do Insomnia. Para importar uma requisição, clique em "Import/Export" e selecione o arquivo JSON que contém a requisição.

### Requisições da Api

1. Requisição do tipo get para retornar todos os clientes

- clique em "New Request" na barra lateral do Insomnia.
- Selecione o metódo GET.
- Insira a URL <http://localhost:3000/api/v1/cliente/>.

2. Requisição do tipo get para retornar um clientes, nescessario passar o id

- clique em "New Request" na barra lateral do Insomnia.
- Selecione o metódo GET.
- Insira a URL <http://localhost:3000/api/v1/cliente/1>.

3. Requisição do tipo post para criar um clientes

- clique em "New Request" na barra lateral do Insomnia.
- Selecione o metódo POST.
- Insira a URL <http://localhost:3000/api/v1/cliente>.
- Selecione no body a opção json.
- Insira os dados no formato json.

```json
  {
    "nome": "Maria", 
    "email": "jose@email", 
    "senha": 123
  }
```

4. Requisição do tipo put para editar um clientes, nescessario passar o id

- clique em "New Request" na barra lateral do Insomnia.
- Selecione o metódo PUT.
- Insira a URL <http://localhost:3000/api/v1/cliente/1>.
- Selecione no body a opção json.
- Insira os dados de edição no formato json.

```json
  {
    "nome": "Jose", 
    "email": "maria@email", 
    "senha": 123456
  }
```

5. Requisição do tipo delete para deletar um clientes, nescessario passar o id

- clique em "New Request" na barra lateral do Insomnia.
- Selecione o metódo DELETE.
- Insira a URL <http://localhost:3000/api/v1/cliente/1>.
