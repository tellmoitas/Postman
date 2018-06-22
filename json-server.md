# Postman com Json-server

O Json Server é uma ferramenta bastante interessante em nosso dia a dia para poder testar API de uma forma muito simples

O Json Server é uma rest API para podermos testar, trazer dados, alterar esses dados, etc. 

Ele permite que a gente faça isso de uma forma muito simples.

## Passo a passo
* Criar um arquivo db.json
* Instalar o json-server
* Iniciar o json-server
* Fazer requisições POST, GET, DELETE

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

#### GET
````http://localhost:3000/candidatos````

Resposta:

![Candidatos](/images/get-candidatos.png)

#### POST
````http://localhost:3000/candidatos````

#### DELETE
````http://localhost:3000/candidatos````

