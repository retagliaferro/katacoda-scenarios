#### Portainer
Solução para gerenciamento de recursos como imagens e containers Docker, networks e volumes   

- **-p:** Porta a porta do container para o host <HOST:CONTAINER>;
- **-d:** Container seja executado como um processo daemon;
- **--name:** Nome do container;
- **-v:** Criar um mapeamento de volume entre o host e o container;
- **--restart:** Caso o container encerrar, o ele ira subir sozinho;

`docker volume create portainer_data`{{execute}} <br>
`docker run -d -p 8000:8000 -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer`{{execute}}

- Acessar o Portainer
https://[[HOST_SUBDOMAIN]]-9000-[[KATACODA_HOST]].environments.katacoda.com


#### Docker run
Baixar e docker um imagem do meu repositório de imagens.

- **-p:** Porta a porta do container para o host <HOST:CONTAINER>;
- **-d:** Container seja executado como um processo daemon;
- **--name:** Nome do container;

`docker login`{{execute}} <br>
`docker run --name meucontainer -p 8080:80 -d retagliaferro/phpinfokubernetes:1.0`{{execute}} <br>

https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com