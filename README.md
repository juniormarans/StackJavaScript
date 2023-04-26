# Fluxo de trabalho geral

As dependências são gerenciadas com [Poetry](https://python-poetry.org/), acesse lá e instale.

De `./` você pode instalar todas as dependências com:

```bash
poetry shell && poetry install

```

----

## **Diretório Raiz**

- Em seguida, abra seu editor em `./`, para que você veja um diretório `./docs/` com seu código dentro. Dessa forma, seu editor poderá encontrar todas as importações, etc. Certifique-se de que seu editor use o ambiente que você acabou de criar com o Poetry.

- **gitignore** arquivo de configuração usado pelo sistema de controle de versão Git para especificar quais arquivos e pastas devem ser ignorados durante o processo de versionamento do projeto.
- **LICENSE**  contém a licença de uso de um software ou projeto, definindo os termos e condições em que o software pode ser utilizado, modificado e distribuído.
- **mkdocs.yml** arquivo de configuração usado pelo MkDocs,
- **pyproject.lock** contém informações precisas sobre as dependências e versões exatas utilizadas pelo projeto em um determinado momento, garantindo que a mesma configuração de dependências seja reproduzida em diferentes máquinas.
- **"pyproject.toml** arquivo de configuração que é usado por algumas ferramentas de desenvolvimento em Python, como o "poetry" e o "flit", para definir as configurações do projeto.

### **docs**

- o nível onde se encontra toda documentação encapsula os módulos do aplicativo `./docs/`

### **Dependências**

- Todas as dependências podem ser encontradas no diretório `./` (o arquivo `pyproject.toml` e `requiriments.txt`)