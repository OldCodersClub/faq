# Более одной учетной записи ssh на хост #
## Например, более одного аккаунта на GitHub с одной машины ##

_аккаунт №1:_  
`Mr. Putin`  
`mr.putin@yandex.ru`

_аккаунт №2:_  
`Mr. Trump`  
`mr.trump@gmail.com`

---

### генерируем ssh-ключ для Mr. Putin ###

_... не забываем указать имя файла ..._

```
> cd ~/%userprofile%/.ssh/
> ssh-keygen -t rsa -b 4096 -C "mr.putin@yandex.ru"
Generating public/private rsa key pair.
Enter file in which to save the key (~/%userprofile%/.ssh/id_rsa): id_rsa_MrPutin  # указываем имя файла
Enter passphrase (empty for no passphrase):  # можно пропустить
Enter same passphrase again:  # можно пропустить
Your identification has been saved in id_rsa_MrPutin.
Your public key has been saved in id_rsa_MrPutin.pub.
The key fingerprint is:
SHA256:nmdZJF5z1Gry/2Zfmrputin2jZX+2deQwXU33Q25aBI mr.putin@yandex.ru
The key's randomart image is:
+---[RSA 4096]----+
|              o=B|
| ...o+ooo.+..    |
|     ..+.++o     |
|  ..++o=O.       |
|        S .o.+@.o|
|      . . o o.*= |
|      o   +   .oO|
|      o     oB   |
|               o*|
+----[SHA256]-----+
```

Создано два файла:  
`id_rsa_MrPutin` - приватный ключ (_без расширения_)  
и  
`id_rsa_MrPutin.pub` - публичный ключ

---

### генерируем ssh-ключ для Mr. Trump ###

_... не забываем указать имя файла ..._

```
> cd ~/%userprofile%/.ssh/
> ssh-keygen -t rsa -b 4096 -C "mr.trump@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (~/%userprofile%/.ssh/id_rsa): id_rsa_MrTrump  # указываем имя файла
Enter passphrase (empty for no passphrase):  # можно пропустить
Enter same passphrase again:  # можно пропустить
Your identification has been saved in id_rsa_MrTrump.
Your public key has been saved in id_rsa_MrTrump.pub.
The key fingerprint is:
SHA256:EssBed6AYMP/afjmrtrumpgvkvVFRwTjXHm/Q0bAA18 mr.trump@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
| .+..ooo++..E    |
|          E  o..X|
|   . o=+ ..+     |
|    ..o+o   +    |
|     ++oS     o .|
|  . . =.o        |
| o.. *       .   |
|  +oo   .o =     |
|o oo  +o+   ..+o |
+----[SHA256]-----+
```

Создано два файла:  
`id_rsa_MrTrump` - приватный ключ (_без расширения_)  
и  
`id_rsa_MrTrump.pub` - публичный ключ

---

### Конфиг-файл ###

Создаём файл `~/%userprofile%/.ssh/config` :

с таким содержимым

```
# Github for "Mr. Putin"
Host mrputin.github.com  # имя хоста 'github.com' подменяем на 'mrputin.github.com'
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa_MrPutin

# Github for "Mr. Trump"
Host mrtrump.github.com  # имя хоста 'github.com' подменяем на 'mrtrump.github.com'
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa_MrTrump
```

---

### Подключаемся

**Подключаемся как `Mr. Putin`**  
меняем в ссылках имя хоста 'github.com' на 'mrputin.github.com'  
`git@github.com:MrPutin/foreign_policy.git`  
_меняем на:_  
`git@mrputin.github.com:MrPutin/foreign_policy.git`

**Подключаемся как `Mr. Trump`**  
меняем в ссылках имя хоста 'github.com' на 'mrtrump.github.com'  
`git@github.com:MrTrump/domestic_policy.git`  
_меняем на:_  
`git@mrtrump.github.com:MrTrump/domestic_policy.git`
