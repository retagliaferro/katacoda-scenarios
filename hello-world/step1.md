## DOCKER

### O que é DOCKER
**O Docker** é uma plataforma open source escrito em Go que facilita a criação e administração de ambientes isolados.Ele possibilita o empacotamento de uma aplicação ou ambiente dentro de um container, se tornando portátil para qualquer outro host que contenha o Docker instalado. Então, você consegue criar, implantar, copiar e migrar de um ambiente para outro com maior flexibilidade.

### Help
Exibi os comandos e como executá-los.

`docker help`{{execute}}

#### Docker version
Exibi as informações da versão do Docker.

`docker version`{{execute}}

### Docker info

Comando para verificarmos as informações do Docker Host.

`docker info`{{execute}}

### Docker images

Lista as imagens que estão no nosso host.

- **Repository:** repositório;
- **TAG:** tag utilizada no repositório;
- **IMAGE ID:** o id na nossa imagem;
- **Created:** data de quando nós criamos a nossa imagem;
- **Size:** tamanho da imagem;

`docker images`{{execute}}

### Docker search

Para que possamos procurar uma imagem, nós podemos utilizar o comando search com o parâmetro nome Ex.: ubuntu, dotnetcore, node … etc, assim ele irá buscar as imagens que são **compatíveis com o nosso server/host**.

`docker search nginx`{{execute}} <br>
`docker search apache`{{execute}} <br>