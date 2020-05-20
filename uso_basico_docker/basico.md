# Uso basico do docker

## importante estar funcionando o comando docker
docker

## primeiro comando docker
docker container run hello-world

Comando run, principais ações: 
    Baixar imagem
    Criação do container
    Execução do container  
    Caso execute novamente o comando ja possui a imagem com cash das informações
    Sempre cria um novo container

```shell
docker container run debian bash --version
```
Comando para listar os container ativos
```shell
docker container ls
```

Listar todos os container executados
```shell
docker container ls -a
```

Execução modo i interativo e t terminal
```shell
docker container run -it debian bash
```

Nomeando o container docker
```shell
docker container run --name mydebian -it debian bash 
```
Reutilizando de container criados 
    (i) Interativo 
    (a) Apache que anexa no terminal

```shell
docker container ls -a
docker container start -ai mydebian
```
Mapeando uma porta no docker e expondo a porta para acesso
```shell
docker container run -p 8080:80 nginx
```
Rodar em um container em background:
    d mode daemon para executar em background
```shell
docker container run -d --name ex-daemon-basic -p 8080:80 -v $(pwd)/html:/usr/share/nginx/html nginx
```
Parar o container
```shell
docker container stop ex-daemon-basic
```
# Gerenciando container

iniciar
```shell
docker container start ex-daemon-basic
```
reiniciar
```shell
docker container restart ex-daemon-basic
```
stopando o container
```shell
docker container stop ex-daemon-basic
```
listando 
```shell
docker container ps
docker container list
docker container ls
```
inclusao do -a para listar todos os container existente
```shell
docker container ls -a
```

verificar log
```shell
docker container logs ex-daemon-basic
```

inspect
```shell
docker container inspect ex-daemon-basic
```
