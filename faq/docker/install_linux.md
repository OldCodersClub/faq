# Инструкция по установке Docker на Linux

&#9668; [Docker и Docker Compose](docker.md)

В примере рассматривается установка Docker на самый распространенный дистрибутив Linux - `Ubuntu`.

### Ссылки

- [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/) (En)
- [Linux post-installation steps for Docker Engine](https://docs.docker.com/engine/install/linux-postinstall/) (En)
- [Установка и использование Docker в Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-ru) (Ru)
- [Install Docker Compose](https://docs.docker.com/compose/install/) (En)
- [How To Install and Use Docker Compose on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04) (En)

### 1. Добавляем репозиторий Docker

```bash
$ sudo apt-get update
```

```bash
$ sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release -y
```

```bash
$ sudo mkdir -p /etc/apt/keyrings
```

```bash
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```bash
$ echo \
    "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### 2. Устанавливаем Docker

```bash
$ sudo apt-get update
```

```bash
$ sudo apt-get install docker-ce docker-ce-cli containerd.io -y
```

### 3. Устанавливаем docker-compose

```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```bash
$ sudo chmod +x /usr/local/bin/docker-compose
```

### 4. Проверяем

Должны работать следующие команды:

```bash
$ sudo docker -v
Docker version 23.0.1, build a5ee5b1
```

```bash
$ sudo docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

```bash
$ sudo docker images
REPOSITORY       TAG         IMAGE ID       CREATED        SIZE
```

```bash
$ docker-compose -v
docker-compose version 1.29.2, build unknown
```

### 5. Запуск Docker без суперпользователя

```bash
$ sudo groupadd docker
```

```bash
$ sudo usermod -aG docker $USER
```

Выходим из терминала и заходим обратно.

И проверяем:

```bash
$ id -nG
```

```bash
$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

```bash
$ docker images
REPOSITORY       TAG         IMAGE ID       CREATED        SIZE
```
