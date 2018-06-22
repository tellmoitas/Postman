# Postman com JSON Server

Desenvolver um aplicativo muitas vezes exige algum tipo de integração com outro sistema já existente. 

Postman é uma ferramenta que dá suporte a documentação das requisições feitas pela API. Ele possui ambiente para a documentação, execução e testes de APIs e requisições em geral. 

O objetivo deste texto é explicar de uma maneira simples e prática como:

* Preparar o ambiente
* Fazer requisições POST, GET e DELETE
* Criar Coleções
* Criar Pastas
* Criar Requests
* Adicionar Parâmetros
* Adicionar Headers
* Criar e popular variáveis de ambiente/globais


## Preparar o ambiente

* Criar um arquivo db.json
* Instalar o json-server
* Iniciar o json-server
* Fazer requisições POST, GET e DELETE

### Criar um arquivo db.json

Crie um arquivo db.json

```json
{
  "candidatos": [
    {
      "id": 1,
      "telefone": 987654321,
      "nome": "Lula"
    },
    {
      "telefone": 987654321,
      "nome": "Dilma",
      "id": 2
    },
    {
      "telefone": 987654321,
      "nome": "Sergio Moro",
      "id": 3
    }
  ]
}
```

### Instalar o json-server

O **json-server** é uma ferramenta bastante interessante em nosso dia a dia para poder testar API de uma forma muito simples

O **json-server** é uma rest API para podermos testar, trazer dados, alterar esses dados, etc. 

Ele permite que a gente faça isso de uma forma muito simples.

Acesse o prompt e digite:

````
$ npm install -g json-server
````

### Iniciar o json-server

````
$ json-server --watch db.json
````

## Fazer requisições POST, GET, DELETE

Ao usarmos o Postaman estaremos acessando diretamente o ```db.json```

#### Usando GET
Vamos verificar os candidados que estão cadastrados

````http://localhost:3000/candidatos````

Resposta:

![Candidatos](/images/get-candidatos.png)

#### Usando POST

````http://localhost:3000/candidatos````

Ao usar o POST é necessário passar os parametros na requisição, desta forma:

![Candidatos](/images/post-candidatos.png)

ou desta forma:

![Candidatos](/images/post-candidatos.png)

Note que após o envio da requisição,  o arquivo db.json foi alterado

![Candidatos](/images/code-post-candidatos.png)

Verifique os candidados que estão cadastrados

````http://localhost:3000/candidatos````

#### DELETE

Iremos excluir o candidato que acabamos de inserir, informando o id do candidato ````/4```` após o endpoint.

````http://localhost:3000/candidatos/4````


Verifique os candidados que estão cadastrados

````http://localhost:3000/candidatos````


## Criar Coleções
* Clique no ícone da pastinha
* Digite o nome da coleção
* Clique em Create

## Criar Pastas
* Clique no ícone de reticências
* Clique em Add Folder
* Digite o nome da pasta
* Clique em Create

## Criar Requests
### Para criar uma request
* Digite a url da API
* Selecione o método HTTP que será utilizado. 
### Para salvar uma request
* Clique em **Save**, que fica ao lado do botão Save.
#### No formulário aparecer:
* Escolha a coleção e a pasta que deseja salvar a request 
* Clique novamente em **Save**.

## Adicionar Parâmetros

## Adicionar Headers
## Criar e popular variáveis de ambiente/globais

