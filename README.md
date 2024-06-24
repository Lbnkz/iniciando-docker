# Aprendendo Docker

Bem-vindo ao repositório onde estou aprendendo Docker! Este README fornece uma visão geral dos comandos mais usados do Docker com breves explicações sobre cada um deles.

## Índice

- [O que é Docker?](#o-que-é-docker)
- [Instalação](#instalação)
- [Comandos Docker](#comandos-docker)
  - [Imagens](#imagens)
  - [Contêineres](#contêineres)
  - [Volumes](#volumes)
  - [Redes](#redes)
  - [Docker Compose](#docker-compose)
- [Recursos](#recursos)

## O que é Docker?

Docker é uma plataforma de contêinerização que permite criar, testar e implantar aplicativos rapidamente. Os contêineres são leves e incluem tudo o que é necessário para executar uma aplicação, desde o código até as bibliotecas e dependências.

## Instalação

Para instalar o Docker, siga as instruções oficiais no site [Docker Install](https://docs.docker.com/get-docker/).

## Comandos Docker

### Imagens

- `docker pull <imagem>`  
  Baixa uma imagem do Docker Hub para o seu ambiente local.
  ```sh
  docker pull ubuntu
  ```

- `docker build -t <nome:tag> <caminho>`  
  Cria uma imagem a partir de um Dockerfile.
  ```sh
  docker build -t meuapp:1.0 .
  ```

- `docker images`  
  Lista todas as imagens disponíveis localmente.
  ```sh
  docker images
  ```

- `docker rmi <imagem>`  
  Remove uma imagem local.
  ```sh
  docker rmi ubuntu
  ```

### Contêineres

- `docker run -it <imagem>`  
  Cria e inicia um novo contêiner em modo interativo.
  ```sh
  docker run -it ubuntu
  ```

- `docker ps`  
  Lista todos os contêineres em execução.
  ```sh
  docker ps
  ```

- `docker ps -a`  
  Lista todos os contêineres, incluindo os que não estão em execução.
  ```sh
  docker ps -a
  ```

- `docker stop <id>`  
  Para um contêiner em execução.
  ```sh
  docker stop <id>
  ```

- `docker start <id>`  
  Inicia um contêiner parado.
  ```sh
  docker start <id>
  ```

- `docker rm <id>`  
  Remove um contêiner parado.
  ```sh
  docker rm <id>
  ```

### Volumes

- `docker volume create <nome>`  
  Cria um volume.
  ```sh
  docker volume create meuvolume
  ```

- `docker volume ls`  
  Lista todos os volumes.
  ```sh
  docker volume ls
  ```

- `docker volume rm <nome>`  
  Remove um volume.
  ```sh
  docker volume rm meuvolume
  ```

### Redes

- `docker network create <nome>`  
  Cria uma nova rede.
  ```sh
  docker network create minharede
  ```

- `docker network ls`  
  Lista todas as redes.
  ```sh
  docker network ls
  ```

- `docker network rm <nome>`  
  Remove uma rede.
  ```sh
  docker network rm minharede
  ```

### Docker Compose

- `docker-compose up`  
  Inicia os serviços definidos em um arquivo `docker-compose.yml`.
  ```sh
  docker-compose up
  ```

- `docker-compose down`  
  Para e remove os contêineres, redes e volumes criados pelo `docker-compose up`.
  ```sh
  docker-compose down
  ```

## Recursos

- [Documentação Oficial do Docker](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)

---

Espero que este README seja útil para o seu aprendizado de Docker. Se tiver dúvidas ou sugestões, sinta-se à vontade para abrir uma issue ou um pull request!