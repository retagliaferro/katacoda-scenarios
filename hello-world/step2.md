#### Docker pull
Baixa a imagem no host

`docker pull nginx`{{execute}}
`docker pull apache`{{execute}}

#### Docker run
Comando para executar um container. Se a imagem não existir no host, o Docker baixa a imagem e depois executa

- **-p:** Porta a porta do container para o host <HOST:CONTAINER>;
- **-p:** Container seja executado como um processo daemon;
- **Name:** Nome do container;

`docker run --name nginx -p 4040:80 -d nginx`{{execute}}
- Acessar nginx
https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

### Docker ps

Exibi os containers que estão em execução

`docker ps`{{execute}}

### Docker stop

Comando que encerra o container.

`docker ps`{{execute}}
`docker ps -q`{{execute}}
`docker stop nginx`{{execute}}

### Docker start

Comando que inicia o container parado.

`docker ps`{{execute}}
`docker ps -q`{{execute}}
`docker start nginx`{{execute}}
