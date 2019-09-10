## DOCKER

### O que é DOCKER

**Docker** é uma plataforma Open Source escrito em Go, que é uma linguagem de programação de alto desempenho desenvolvida dentro do Google, que facilita a criação e administração de ambientes isolados.

### Help
Exibi os possiveis comandos e a forma de executá-los.

`docker help`{{execute}}

#### Docker version
Mostrar as informações da versão do Docker

`docker version`{{execute}}

### Docker info

Comando para verificarmos as informações do Docker Host.

`docker info`{{execute}}

### Docker images

Lista as imagens que temos no nosso host.
- **Repository:** repositório;
- **TAG:** tag utilizada no repositório;
- **IMAGE ID:** o id na nossa imagem;
- **Created:** data de quando nós criamos a nossa imagem;
- **Size:** tamanho da imagem;

`docker images`{{execute}}

### Docker search

Para que possamos procurar uma imagem, nós podemos utilizar o comando a baixo com o parâmetro nome Ex.: ubuntu, dotnetcore, node … etc, assim ele irá buscar as imagens que são **compatíveis com o nosso server/host** que para esse exemplo estamos utilizando o Linux.

`docker search nginx`{{execute}} <br>
`docker search apache`{{execute}} <br>