# Imersão Full Stack & FullCycle - Codebank

![Imersão Full Stack && Full Cycle](/assets/fullcycle.png "Imersão FullCycle")

## Instruções

Na [raiz](/codebank/) da pasta execute no terminal o comando `docker compose up -d` para levantar os containers.

### pgAdmin

Acesse o [pgAdmin](http://localhost:9001) na porta [9001](http://localhost:9001) com as credenciais abaixo.

```txt
username: admin@user.com
password: 123456
```

### Conexão Banco de Dados

Crie uma nova conexão para o banco de dados com as configurações abaixo.

```txt
name: db
host: db
port: 5432
database: codebank
username: postgres
password: root
```

Crie as tabelas para o banco de dados executando essas [queries](/codebank/db.sql).

Entre no container da aplicação executando no terminal o comando `docker exec -it codebank-app-1 bash`, o nome do container provavelmente será "codebank-app-1", caso contrário altere de acordo com o nome gerado pelo docker. Execute o comando `go run main.go`, será baixado os pacotes na primeira vez. Após isso, se sucesso, será mostrado no terminal "Rodando gRPC Server".

Para fazer requisições e testar o app no modo cliente, abra outra aba do terminal, entre novamente no container da aplicação e execute o comando `evans -r repl -p=50052`, entre com `call Payment` para acessar o [PaymentService](/codebank/infrastructure/grpc/protofile/payment.proto) e digite as seguintes informações baseada no credit_card registrado no banco de dados.

```txt
name = John Doe
number = 1234567890123456
expirationMonth = 01
expirationYear = 2025
cvv = 555
amount = 100
store = CodeStore
description = carrinho
```
