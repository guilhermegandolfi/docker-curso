# Curso de docker
Este repositorio tem como objetivo armazenar os principais comandos e conceitos que obtive com a utilizacao de docker

## Instalação
Para instalação do docker no ubunto foi utilizado como tutorial a url:(https://docs.docker.com/engine/install/ubuntu/)

## Step-by-Step

```shell
$ sudo apt-get update

$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
    
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

$ sudo apt-get update

$ sudo apt-get install docker-ce docker-ce-cli containerd.io

```
Para testar se foi instalado corretamente execute os comandos abaixo:

```shell
$ docker --help
$ sudo docker run hello-world
```
