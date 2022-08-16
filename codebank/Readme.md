# Imersão FullCycle 9 - CodeBank

![Imersão Full Stack && Full Cycle](/assets/fullcycle.png "Imersão FullCycle")

## Instruções

Execute `docker compose up -d` para levantar os containers dentro da pasta raiz "codebank"

Vá em [localhost:9000](http://localhost:9000) para acessar o pgAdmin com essas [credenciais](#pgadmin)

Crie um novo server para o banco de dados com essas [configurações](#database-connection)

Crie as tabelas para o banco de dados executando essas [queries](/codebank/db.sql)

Entre no container da aplicação go, o nome provavelmente será "codebank-app-1" e execute o comando `go run main.go`

## pgAdmin

username: admin@user.com

password: 123456

## Database Connection

name: db

host: db

port: 5432

database: codebank

username: postgres

password: root
