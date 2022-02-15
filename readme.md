# DOCKER

## Configurações iniciais do Docker

### Docker Help

```bash
docker --help

# New sintaxe
docker container --help
```

### Executar Imagem

```bash
docker run -d -p 80:80 --name [nameContainer] docker/getting-started
```

- <code>-d</code> executar o contêiner no modo desanexado (em segundo plano)

- <code>-p 80:80</code>  mapear a porta 80 do host para a porta 80 no contêiner

- <code>--name</code> renomear contêiner a ser usada

- <code>-docker/getting-started</code> a imagem a ser usada

### Executar um comando em um novo contêiner com <code>bash</code> interativo

```bash
docker run -it [containerId||nameContainer]
```

### Executar um comando dentro do contêiner em execução com <code>bash</code> interativo

```bash
docker exec -it [containerId||nameContainer] /bin/bash
```

```bash
docker exec -it [containerId||nameContainer] bash
```

```bash
# Executa comandos dentro do contêiner sem acessar o bash
docker exec [containerId||nameContainer] [command]
```

### Baixar imagem do Hub Docker

```bash
docker pull [name-image]
```

### Listar Imagens

```bash
docker images
```

### Excluir Imagens

```bash
docker rmi [containerId||nameContainer]
```

### Listar contêiner em execução

```bash
docker ps
# OR
docker container ls
```

- <code>-a</code> lista todos contêiner executados anteriormente

### Parar contêiner em execução

```bash
docker stop [containerId||nameContainer]
```

### Excluir contêiner

```bash
docker rm [containerId||nameContainer]
```

### Copiando arquivos da maquina local para contêiner

```bash
docker cp [diretório/origem/meuArquivoLocal.txt] [containerId||nameContainer]:[/diretório/destino]
```

### Copiando arquivos do contêiner para maquina local

```bash
docker cp [containerId||nameContainer]:[/diretório/origem] [diretório/destino/meuArquivoLocal.txt]
```

# LARADOCK

### Subir contêiner

```bash
docker-compose up -d [nameImage1] [nameImage2] [nameImage3]
docker-compose up -d nginx mysql phpmyadmin redis
```

### Acessar contêiner

```bash
docker exec -it [containerId||nameContainer] /bin/sh
# OR
docker exec -it [containerId||nameContainer] /bin/bash
```

### Executar comandos com Bash interativo

```bash
docker-compose exec --user=laradock [containerId||nameContainer] bash
```

### Listar contêiner em execução

```bash
docker-composer ps
```

# Referências

- Pesquisa

    - [Docker com VS Code](https://docs.microsoft.com/pt-br/visualstudio/docker/tutorials/docker-tutorial?WT.mc_id=vscode_docker_aka_getstartedwithdocker) neste tutorial, você aprenderá a criar e implantar aplicativos do docker em Windows ou Mac usando Visual Studio Code.

    - [Laravel + Docker = Laradock](https://youtu.be/GienvDWdBmo) Crie um ambiente com Laravel e Docker de maneira rápida, simples e fácil.

### Autor

> Made with 💙 by JUNIOR LIMA 👋 [See my LinkedIn](https://www.linkedin.com/in/junior-lima-495108208/) • GitHub [@JuniorLima22](https://github.com/JuniorLima22)