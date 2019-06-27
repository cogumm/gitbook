# Pegando o IP do container

Para conseguir o IP de um container que está rodando, basta rodar o seguinte comando no seu terminal:

```bash
$ docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' nome_do_container
```

Caso você queira o IP de todos os seus container rodando na sua máquina, basta utilizar este comando no terminal:

```bash
$ docker inspect -f '{{.Name}} - {{.NetworkSettings.IPAddress }}' $(docker ps -aq)
```

Se você estiver utilizando o `docker-compose`:

```bash
$ docker inspect -f '{{.Name}} - {{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $(docker ps -aq)
```

Se estiver utilizando o `docker-machine` :

```bash
$ docker-machine nome_do_container
```

