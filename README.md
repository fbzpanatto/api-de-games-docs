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
Caso essa resposta aconteca, isso significa que aconteceu alguma falha durante o processo de autenticacao da requisicao. Motivos: Token invalido, Token expirado.
### GET /games/:id
