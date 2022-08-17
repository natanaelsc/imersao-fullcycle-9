# Imersão Full Stack & FullCycle - Codebank (Apache Kafka)

![Imersão Full Stack && Full Cycle](/assets/fullcycle.png "Imersão FullCycle")

## Descrição

Repositório do Apache Kafka (Backend)

## Configurar ```/etc/hosts```

A comunicação entre as aplicações se dá de forma direta através da rede da máquina. Para isto é necessário configurar um endereços que todos os containers Docker consigam acessar.

Acrescente no seu ```/etc/hosts``` (para Windows o caminho é ```C:\Windows\system32\drivers\etc\hosts```):

```txt
127.0.0.1 host.docker.internal
```

Em todos os sistemas operacionais é necessário abrir o programa para editar o *hosts* como Administrator da máquina ou root.

### Rodar a aplicação

Execute os comandos:

```txt
docker-compose up -d
```

Quando parar os containers do Kafka, lembre-se antes de rodar o **docker-compose up**, rodar o **docker-compose down** para limpar o armazenamento, senão lançará erro ao subir novamente.

### Para Windows

Lembrar de instalar o WSL2 e Docker. Vejo o vídeo: [https://www.youtube.com/watch?v=usF0rYCcj-E](https://www.youtube.com/watch?v=usF0rYCcj-E)

Siga o guia rápido de instalação: [https://github.com/codeedu/wsl2-docker-quickstart](https://github.com/codeedu/wsl2-docker-quickstart) 