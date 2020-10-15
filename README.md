# API de Games
Esta API e utilizada para tal e tal...
## Endpoints
### GET /games
Esse endpoint e responsavel por retornar a listagem de todos os games cadastrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK! 200
Caso essa resposta aconteca, sera retornado a listagem de todos os games.
Exemplo de resposta:
```
[
  {
    "id": 23,
    "title": "Call of duty MW",
    "year": 2019,
    "price": 60
  },
  {
    "id": 45,
    "title": "Among Us",
    "year": 2017,
    "price": 10
  },
]
```
##### Falha na autenticacao! 401

Exemplo de resposta:

```
{
  "err": "Token Invalido"
}
```
Caso essa resposta aconteca, isso significa que aconteceu alguma falha durante o processo de autenticacao da requisicao. Motivos: Token invalido, Token expirado.

### POST /auth
Esse endpoint e responsavel por fazer o processo de login.
#### Parametros

Email e Senha

Exemplo:
```
{
  "email": "email do user cadastrado",
  "password": "senha"
}
```
#### Respostas
##### OK! 200
Caso essa resposta aconteca, sera retornado o token.
Exemplo de resposta:
```
{
  "token": "aisjdoiu3214ei21u3y4uihid.jue12e1e"
}
```
##### Falha na autenticacao! 401
Caso essa resposta aconteca, isso significa que aconteceu alguma falha durante o processe de autenticacao da requisicao. Motivos: senha ou email incorretos.

Exemplo de resposta:

```
{
  "err": "Credenciais Invalidas"
}
```
