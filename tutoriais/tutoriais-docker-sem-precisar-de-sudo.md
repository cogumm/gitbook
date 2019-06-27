# Executar o Docker sem precisar de sudo

## Docker sem `sudo`

Antes de tudo, deve-se criar um grupo chamado `docker`

```bash
$ sudo groupadd docker
```

Agora, basta adicionar o seu usuário ao grupo `docker`:

```bash
$ sudo usermod -aG docker $USER
```

Após utilizar o comando, basta sair da sessão e logar novamente.



