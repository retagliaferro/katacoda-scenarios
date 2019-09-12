#### Docker pull
Baixa a imagem no host.

`clear`{{execute}} <br>
`docker pull nginx`{{execute}} <br>
`clear`{{execute}} <br>
`docker pull httpd`{{execute}}

#### Docker run
Comando para executar um container. Se a imagem não existir no host, o Docker baixa a imagem e depois executa.

- **-p:** Porta a porta do container para o host <HOST:CONTAINER>;
- **-d:** Container seja executado como um processo daemon;
- **--name:** Nome do container;

`clear`{{execute}} <br>
`docker run --name nginx -p 80:80 -d nginx`{{execute}}

- Acessar nginx
https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com



#### Docker run
Comando para executar um container. Se a imagem não existir no host, o Docker baixa a imagem e depois executa.

- **-p:** Porta a porta do container para o host <HOST:CONTAINER>;
- **-d:** Container seja executado como um processo daemon;
- **--name:** Nome do container;

`clear`{{execute}} <br>
`docker run --name apache -p 81:80 -d httpd`{{execute}}

- Acessar Apache
https://[[HOST_SUBDOMAIN]]-81-[[KATACODA_HOST]].environments.katacoda.com

### Docker ps

- Exibi os containers que estão em execução no momento

`clear`{{execute}} <br>
`docker ps`{{execute}}

- Exibi os containers que estão em execução no momento e os parados.

`docker ps -a`{{execute}}


### Docker stats

Exibi as informações de consumo de recursos do host relacionado ao containers.

- **CONTAINER:** ID do Container;
- **CPU %:** uso de CPU em porcentagem;
- **MEM USAGE / LIMIT:** Memória usada/Limite que você pode ter setado;
- **MEM:** uso de memória em porcentagem;
- **NET I/O:** I/O de Internet;
- **BLOCK IO:** Outros processos de I/O;

`clear`{{execute}} <br>
`docker stats`{{execute}}


### Docker logs

Exibi os logs dos containers

- **-f:** Saída continua dos logs

`clear`{{execute}} <br>
`docker logs nginx -f`{{execute}}

### Docker stop

Comando que encerra o container.

`clear`{{execute}} <br>
`docker ps`{{execute}} <br>
`docker ps -q`{{execute}} <br>
`docker stop nginx`{{execute}} <br>
`docker ps`{{execute}} <br>

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

### Docker start

Comando que inicia o container parado.

`clear`{{execute}} <br>
`docker ps`{{execute}} <br>
`docker ps -q`{{execute}} <br>
`docker start nginx`{{execute}} <br>
`docker ps`{{execute}} <br>

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com

#### Docker run

Criar um container Alpine com interatividade com o bash. 

- **-p:** Container seja executado como um processo daemon;
- **-i:** Interativo;
- **-t:** Abrir um terminal (tty);
- **Name:** Nome do container;
- **--host:** Hostname do container;
- **/bin/bash:** Bash que sera executado no container;

`clear`{{execute}} <br>
`docker run -t -i  --hostname host-alpine --name alpine-opus alpine /bin/sh`{{execute}}

##### Sair do container
-Para sair do container sem encerrar o processo do container `CRTL + p + q`<br>
`exit`{{execute}} <br>

##### Docker attach
Comando para retornar dentro do container

`clear`{{execute}} <br>
`docker start alpine-opus`{{execute}}  <br>
`docker attach alpine-opus`{{execute}} <br>
`hostname`{{execute}}  <br>
`ifconfig`{{execute}} <br>
`apk add nginx`{{execute}}  <br>
`apk add curl wget`{{execute}} <br>
`exit`{{execute}}

##### Docker inspect
Comando que retornar um json com todas as informações relacionadas ao container.

`clear`{{execute}}  <br>
`docker start alpine-opus`{{execute}}  <br>
`docker inspect alpine-opus`{{execute}}  <br>

##### Docker exec
Comando que executa comandos de fora (host) para dentro do container.

`clear`{{execute}} <br>
`docker exec alpine-opus ls -l /`{{execute}}  <br>
`docker exec alpine-opus hostname`{{execute}}  <br>

##### Docker rm
Comando que excluir o container

`clear`{{execute}} <br>
`docker rm -f alpine-opus`{{execute}}  <br>
`docker ps`{{execute}}  <br>

##### Docker rmi
Comando que excluir uma imagem do host local

`clear`{{execute}} <br>
`docker rmi -f alpine`{{execute}}  <br>
`docker ps`{{execute}}  <br>