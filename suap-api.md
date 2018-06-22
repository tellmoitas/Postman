# Acessando a API do Suap

Utilizaremos o Postaman para acessar a API do SUAP.

A documentação da API está disponível nesta url: ```https://suap.ifrn.edu.br/api/docs/```


## POST - Obtendo o token

A primeira coisa que você precisa saber é que, para acessar os recusros disponibilizados pela API você precisará de um TOKEN.

O TOKEN é obtido apartir desta url: ```https://suap.ifrn.edu.br/api/v2/autenticacao/token/```

![Obtendo o token](/images/token_suap.png)

* Selecione **POST**
* Digite a url
* Selecione a opção **raw**
* Digite o código abaixo, substituindo com os seus dados
  ```json
  {
    "username": "DIGITE SUA MATRICULA AQUI",
    "password": "DIGITE SUA SENHA AQUI"
  }
  ```
* Escolha o tipo de dado como **JSON (aplication/json)**
* Clique no botão **SEND**

Na mesma janela você receberá a resposta de sua requisição.

**COPIE O TOKEN, SEM AS ASPAS**

## GET - Acessando meus dados

Vamos usar uma dos recursos oferecidos pela API através da url: ```https://suap.ifrn.edu.br/api/v2/minhas-informacoes/meus-dados/```

![Obtendo o token](/images/meus-dados-suap.png)

* Selecione **GET**
* Digite a url
* Selecione a opção **Headers**
* No primeiro campo, digite **Authorization** 
### Aqui está o macete
* No segundo campo, digite JWT antes do TOKEN **(Aprendi este macete, com Felipe Pontes)**
* Clique no botão **SEND**


