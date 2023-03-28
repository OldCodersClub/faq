# Инструкция по установке Docker на Windows

&#9668; [Docker и Docker Compose](docker.md)

### Ссылки

- [Install Linux on Windows with WSL](https://learn.microsoft.com/en-us/windows/wsl/install) (En)
- [Install Docker Desktop on Windows](https://docs.docker.com/desktop/install/windows-install/) (En)
- [How to access linux/Ubuntu files from Windows 10 WSL?](https://superuser.com/questions/1110974/how-to-access-linux-ubuntu-files-from-windows-10-wsl) (En)

> **`Ctrl + C` и `Ctrl + V` в терминале на `Windows`**
>
> Используйте правую кнопку мыши для копирования значений из терминала, или для вставки в него. Выделите необходимый текст, нажмите ПКМ - текст скопирован. Если так не срабатывает, используйте `Ctrl + Shift + C` для копирования и `Ctrl + Shift + V` для вставки.

В примере рассматривается установка `Docker` и `docker-compose` на `Windows 10` через `WSL2` и `Docker Desktop`.

### 1. Устанавливаем WSL

Открываем терминал от имени администратора и вводим команду:

```bash
$ wsl --install
```

После этого перезагружаемся.

### 2. Устанавливаем Ubuntu

Открываем терминал от имени администратора и вводим команду:

```bash
$ wsl --install -d Ubuntu
```

После установки управление в терминале перехватывает свежая Ubuntu, где нужно будет создать нового пользователя с паролем. После чего выйти из консоли Ubuntu.

Проверяем в консоли Windows установку Ubuntu:

```bash
$ wsl -l -v
  NAME        STATE        VERSION
* Ubuntu      Running      2
```

Чтобы войти в консоль Ubuntu нужно в терминале набрать команду:

```bash
$ wsl
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.
```

Это понадобится для работы с докером через консоль.

### 3. Устанавливаем Docker Desktop

Скачиваем дистрибутив [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/) (файл .exe). При установке ставим галочку на `Use WSL 2 instead of Hyper-V`.
После установки можно будет запустить `Docker Desktop` через ярлык.

### 4. Проверяем

В консоли Windows выполняем команду:

```bash
$ wsl -l -v
  NAME                STATE        VERSION
* Ubuntu              Running      2
* docker-desktop      Running      2
* docker-desktop-data Running      2
```

Входим в консоль Ubuntu:

```bash
$ wsl
```

И уже там проверяем установку:

```bash
$ docker -v
Docker version 23.0.1, build a5ee5b1
```

```bash
$ docker-compose -v
docker-compose version 1.29.2, build unknown
```

```bash
$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

```bash
$ docker images
REPOSITORY       TAG         IMAGE ID       CREATED        SIZE
```
