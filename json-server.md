# Postman com JSON Server

O **json-server** é uma ferramenta bastante interessante em nosso dia a dia para poder testar API de uma forma muito simples

O **json-server** é uma rest API para podermos testar, trazer dados, alterar esses dados, etc. 

Ele permite que a gente faça isso de uma forma muito simples.

## Passo a passo
* Criar um arquivo db.json
* Instalar o json-server
* Iniciar o json-server
* Fazer requisições POST, GET, DELETE, ...

### Antes da Instalação

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

### Instalando o Json Server

````
$ npm install -g json-server
````

### Iniciando o json-server

````
$ json-server --watch db.json
````

### Usando o Postman e salvando diretamente em ```db.json```

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


