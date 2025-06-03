# LSPET

# Aplicação Web de Gerenciamento de Adoção de Animais

Esta aplicação web permite o gerenciamento do cadastro, atualização, listagem e remoção de animais disponíveis para adoção. A aplicação utiliza um banco de dados H2 para persistência e expõe **endpoints RESTful** para facilitar a comunicação com os usuários.

## Funcionalidades

- **Cadastro de animais**: Adicionar animais disponíveis para adoção, com informações como nome, espécie, idade, entre outros.
- **Atualização de animais**: Atualizar informações dos animais cadastrados, permitindo que os dados sejam modificados conforme necessário.
- **Listagem de animais**: Visualizar todos os animais disponíveis para adoção.
- **Remoção de animais**: Excluir animais do banco de dados quando não estiverem mais disponíveis para adoção.
- **Cadastro adotantes**: Adiconar possiveis adontantes para os animais.
- **Remoção de adotantes**: excluir Possiveis adotantes no banco de dados.
-**Listar Adotantes**: mostrar os Adotantes cadastrados 
## Tecnologias Utilizadas

- **Back-end**: Java com Spring Boot
- **Banco de Dados**: H2 (Banco de dados em memória para persistência)
- **API**: Endpoints RESTful utilizando Spring Web
- 
  ### Front-End
- **HTML** e **CSS** para a estrutura e estilo da interface
- **Angular** para criação de componentes dinâmicos e comunicação com a API REST

## Como Rodar a Aplicação Localmente

### Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas:

- [JDK 11 ou superior](https://adoptopenjdk.net/)
- [Maven](https://maven.apache.org/) (opcional, se não usar o Spring Boot Plugin)
- [IDE Java](https://www.jetbrains.com/idea/) (opcional)
- [Node.js](https://nodejs.org/) e [Angular CLI](https://angular.io/cli)

### Passos para Execução

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu-usuario/nome-do-repositorio.git
    ```

2. Navegue até o diretório do projeto:
    ```bash
    cd nome-do-repositorio
    ```

3. Compile e execute a aplicação com o Maven:
    ```bash
    mvn spring-boot:run
    ```

4. A aplicação será iniciada na porta  **9090**. Acesse a aplicação através de `http://localhost:9090`.

## Endpoints

### 1. **Cadastrar Animal**

- **Método**: POST
- **Endpoint**: `/animais`
- **Corpo da Requisição**:
    ```json
    {
        "nome": "Rex",
        "especie": "Cachorro",
        "idade": 3,
        "descricao": "Animal amigável e saudável"
    }
    ```

### 2. **Atualizar Animal**

- **Método**: PUT
- **Endpoint**: `/animais/{id}`
- **Corpo da Requisição**:
    ```json
    {
        "nome": "Rex Atualizado",
        "especie": "Cachorro",
        "idade": 4,
        "descricao": "Animal muito brincalhão"
    }
    ```

### 3. **Listar Animais**

- **Método**: GET
- **Endpoint**: `/animais`

### 4. **Remover Animal**

- **Método**: DELETE
- **Endpoint**: `/animais/{id}`
  

### 5. **Cadastrar Adotante**

- **Método**: POST
- **Endpoint**: `/Adotante`
- **Corpo da Requisição**:
    ```json
    {
        "nomeAdotante": "Joel",
       "telefone":"61986568767",
       "endereco":"Rua orquidea",
        "documento":"3434567",
    }
    ```
### 6. **Atualizar Adotante**
     **Método**: PUT
- **Endpoint**: `/Adotante`
- **Corpo da Requisição**:
    ```json
    {
        "nome": "joel Atualizado",
        "telefone": "84543278",
        "endereco": "rua margarida",
        "documento": "3434567"
    }
    ```

    ### 7. **Listar Adotante**

- **Método**: GET
- **Endpoint**: `/Adotante`
- 
### 6. **Remover Adotante**

- **Método**: DELETE
- **Endpoint**: `/Adotante/{id}`
  
    

## Banco de Dados

A aplicação utiliza o banco de dados H2 em memória, que é automaticamente configurado e inicializado com a aplicação. Os dados não são persistidos após o encerramento da aplicação, uma vez que o H2 é um banco de dados volátil.

## Contribuições

Se você deseja contribuir para o projeto, fique à vontade para fazer um **fork** do repositório e enviar um **pull request** com suas alterações.

## Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

