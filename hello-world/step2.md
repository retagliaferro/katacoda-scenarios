#### Docker pull
Baixa a imagem no host

`docker pull nginx`{{execute}} <br>
`docker pull httpd`{{execute}}

#### Docker run
Comando para executar um container. Se a imagem não existir no host, o Docker baixa a imagem e depois executa

- **-p:** Porta a porta do container para o host <HOST:CONTAINER>;
- **-d:** Container seja executado como um processo daemon;
- **--name:** Nome do container;

`docker run --name nginx -p 4040:80 -d nginx`{{execute}}
- Acessar nginx
https://[[HOST_SUBDOMAIN]]-4040-[[KATACODA_HOST]].environments.katacoda.com

### Docker ps

Exibi os containers que estão em execução

`docker ps`{{execute}}


### Docker stats

Exibi quanto o container está consumindo de recursos do host

`clear`{{execute}} <br>
`docker stats nginx`{{execute}}


### Docker logs

Exibi o log container

- **-f:** Saída continua dos logs

`clear`{{execute}} <br>
`docker stats nginx -f`{{execute}}

### Docker stop

Comando que encerra o container.

`docker ps`{{execute}} <br>
`docker ps -q`{{execute}}<br>
`docker stop nginx`{{execute}}

### Docker start

Comando que inicia o container parado.

`docker ps`{{execute}} <br>
`docker ps -q`{{execute}} <br>
`docker start nginx`{{execute}}

#### Docker run para httpd

`docker run --name httpd -p 4040:80 -d httpd`{{execute}}
- Acessar httpd
https://[[HOST_SUBDOMAIN]]-4040-[[KATACODA_HOST]].environments.katacoda.com

- Comando que encerra o container.

`docker ps`{{execute}} <br>
`docker ps -q`{{execute}}<br>
`docker stop httpd`{{execute}}

#### Docker run

Criar um container Ubuntu com interatividade com o bash. 

- **-p:** Container seja executado como um processo daemon;
- **-i:** Interativo
- **-t:** Abrir um terminal (tty)
- **Name:** Nome do container;
- **--host:** Hostname do container;
- **/bin/bash:** Bash que sera executado no container;

`docker run -t -i  --hostname ubuntu-opus-1 --name ubuntu-opus ubuntu /bin/bash`{{execute}}

##### Docker run
-Para sair do container sem encerrar o processo do container
    CRTL + p + q```bash
```