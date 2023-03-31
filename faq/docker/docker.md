# Docker и Docker Compose

## Дорожная карта (roadmap) изучения [Docker](https://docs.docker.com/desktop/) и [Docker Compose](https://docs.docker.com/compose/)

[<img src="../../res/docker/docker.svg" alt="docker" width="300">](https://docs.docker.com/)

### С чего начать ###

- [Официальный сайт](https://www.docker.com/)
- [Официальная документация](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)

<!-- -->

- [Установка на Linux](install_linux.md)
- [Установка на Mac](install_mac.md)
- [Установка на Windows](install_win.md)
 ---

### Что это и зачем?

> &#8211; Лариска, объясни простыми словами для совсем новичков, что такое Docker?
>
> &#8211; Docker - это технология, позволяющая упаковывать приложения и их зависимости в изолированные контейнеры, которые можно запускать на любой операционной системе. Таким образом, приложения могут работать одинаково на любых серверах, не требуя дополнительной настройки, или установки зависимостей на каждом из них.

Docker - это платформа, позволяющая универсальным способом упаковать в контейнер приложение вместе с нужными ему окружением и зависимостями, а затем доставить и запустить его на целевой системе. Запустить на любой целевой системе, с любой ОС, независимо от того, какое окружение присутствует, или отсутствует в этой системе, так как всё необходимое для запуска и работы приложения уже упаковано внутри контейнера.

Единственное необходимое условие - **на целевой системе должна быть установлена платформа Docker**.

Таким образом получается, что на целевой системе с установленной платформой Docker можно внутри этой платформы располагать разнообразные контейнеры. В каждом контейнере содержится нужная ОС с установленным в неё приложением и необходимыми ему зависимостями. И любой из этих контейнеров в неизменном виде можно перенести на любую другую систему с Докером, и тот гарантированно будет работать на ней. Точно так же, как любой картридж с игрой внутри будет работать на любой игровой приставке для таких картриджей. По этой аналогии получается, что Docker - это игровая приставка, контейнер - картридж, игра внутри картриджа - ваше приложение и всё, что ему необходимо для работы, включая ОС, интерпретаторы и библиотеки.

Приложения, упакованные в контейнеры, изолируются от целевой операционной системы и от других подобных контейнеров. Поэтому можно не задумываться, в каком окружении они будут работать и единообразно запускать и останавливать их простыми универсальными консольными командами, не заботясь о системных зависимостях.

### Статьи для новичков

- [Изучаем Docker, часть 1: основы](https://habr.com/ru/company/ruvds/blog/438796/) (Ru)
- [Изучаем Docker, часть 2: термины и концепции](https://habr.com/ru/company/ruvds/blog/439978/) (Ru)
- [Изучаем Docker, часть 3: файлы Dockerfile](https://habr.com/ru/company/ruvds/blog/439980/) (Ru)
- [Изучаем Docker, часть 4: уменьшение размеров образов и ускорение их сборки](https://habr.com/ru/company/ruvds/blog/440658/) (Ru)
- [Изучаем Docker, часть 5: команды](https://habr.com/ru/company/ruvds/blog/440660/) (Ru)
- [Изучаем Docker, часть 6: работа с данными](https://habr.com/ru/company/ruvds/blog/441574/) (Ru)
- [Руководство по Docker Compose для начинающих](https://habr.com/ru/company/ruvds/blog/450312/) (Ru)
- [Руководство по Kubernetes, часть 1: приложения, микросервисы и контейнеры](https://habr.com/ru/company/ruvds/blog/438982/) (Ru)

<!-- -->

- [Начала Docker для юнги](https://habr.com/ru/post/651813/) (Ru)
- [Docker (Докер) для чайников](https://wiki.dieg.info/docker) (Ru)
- [Использование Docker для чайников](https://losst.pro/ispolzovanie-docker-dlya-chajnikov) (Ru)
- [Освоение контейнера Docker для чайников: теоретическое и практическое руководство](https://codernet.ru/articles/drugoe/osvoenie_kontejnera_docker_dlya_chajnikov_teoreticheskoe_i_prakticheskoe_rukovodstvo/) (Ru)
- [Что такое Docker простыми словами](https://blog.vverh.digital/2021/chto-takoe-docker-what-is-it/) (Ru)
- [Простыми словами про Docker](https://goodbit.dev/blog/prostymi-slovami-pro-docker) (Ru)
- [Docker. Начало](https://habr.com/ru/post/353238/) (Ru)

---

### Шпаргалки и шаблоны

- [Awesome Docker](https://github.com/veggiemonk/awesome-docker) (En)
- [Awesome Compose](https://github.com/docker/awesome-compose) (En)
- [Docker Cheat Sheet](https://gist.github.com/Aleksey-Voko/50f3631386514e340fca7c416f21ab9f)
- [Docker Cheat Sheet (Will Sargent)](https://github.com/wsargent/docker-cheat-sheet/tree/master/ru)
- [Docker-compose Cheat Sheet](https://www.programonaut.com/wp-content/uploads/2021/07/docker-compose-cheat-sheet.pdf)
- [MySQL на базе docker-compose](https://github.com/LessonDump/DockerMySQL)
- [Postgresql на базе docker-compose](https://github.com/LessonDump/DockerPostgres)
- [Postgresql + PgAdmin на базе docker-compose](https://github.com/LessonDump/DockerPostgresPgAdmin)
- [MySQL + Adminer на базе docker-compose](https://github.com/LessonDump/DockerMySqlAdminer)
- [Простой шаблон Telegram-бота на основе docker-compose](https://github.com/LessonDump/TelegramBotDockerTmpl)

<!-- -->

- [Play with Docker](https://labs.play-with-docker.com/) (En)

---

### Курсы

- [Docker для начинающих + практический опыт](https://stepik.org/course/123300/info) (Ru)
- [DOCKER С НУЛЯ. БЕСПЛАТНЫЙ КУРС](https://karpov.courses/docker) (Ru)
- [Docker для начинающих](https://stepik.org/course/74010/info) (Ru)

---

### Учебники

[<img src="https://dmkpress.com/images/cms/thumbs/a5b0aeaa3fa7d6e58d75710c18673bd7ec6d5f6d/978-5-97060-426-7_270_369_jpg__100.jpg" alt="dmkpress" height="200">](https://dmkpress.com/catalog/computer/os/978-5-97060-426-7/)
&nbsp;
[<img src="https://dmkpress.com/images/cms/thumbs/a5b0aeaa3fa7d6e58d75710c18673bd7ec6d5f6d/978-5-97060-772-5_270_369_jpg__100.jpg" alt="dmkpress" height="200">](https://dmkpress.com/catalog/computer/os/978-5-97060-772-5/)
&nbsp;
[<img src="https://img3.labirint.ru/rc/94e41f1785903d9c2d3eb3d27a610631/363x561q80/books70/691503/cover.jpg?1555594011" alt="labirint" height="200">](https://www.labirint.ru/books/691503/)
&nbsp;
[<img src="https://learning.oreilly.com/library/cover/9781800565135/250w/" alt="oreilly" height="200">](https://www.oreilly.com/library/view/docker-deep-dive/9781800565135/)
&nbsp;
[<img src="https://media.springernature.com/w600/springer-static/cover-hires/book/978-1-4842-7815-4" alt="springernature" height="200">](https://link.springer.com/book/10.1007/978-1-4842-7815-4)

[<img src="https://learning.oreilly.com/library/cover/9780988820203/250w/" alt="oreilly" height="200">](https://www.oreilly.com/library/view/the-docker-book/9780988820203/)
&nbsp;
[<img src="https://content.packt.com/B11211/cover_image_small.png" alt="packt" height="200">](https://www.packtpub.com/product/docker-quick-start-guide/9781789347326)
&nbsp;
[<img src="https://media.springernature.com/w600/springer-static/cover-hires/book/978-1-4842-8117-8" alt="springernature" height="200">](https://link.springer.com/book/10.1007/978-1-4842-8117-8)
&nbsp;
[<img src="https://content.packt.com/B18778/cover_image_small.jpg" alt="packt" height="200">](https://www.packtpub.com/product/a-developers-essential-guide-to-docker-compose/9781803234366)
&nbsp;
[<img src="https://d2sofvawe08yqg.cloudfront.net/understanding-docker-visual-way/s_hero?1675200003" alt="leanpub" height="200">](https://leanpub.com/understanding-docker-visual-way)

[<img src="https://content.packt.com/B14865/cover_image_small.png" alt="packt" height="200">](https://www.packtpub.com/product/learn-docker-fundamentals-of-docker-19x-second-edition/9781838827472)
&nbsp;
[<img src="https://drek4537l1klr.cloudfront.net/stoneman/Figures/cover.jpg" alt="manning" height="200">](https://www.manning.com/books/learn-docker-in-a-month-of-lunches)

---

### Руководства

- [Docker Getting Started Tutorial](https://github.com/docker/getting-started) (En)
- [Why Do I Need Docker, and How Do I Use It?](https://guides.hexlet.io/docker/) (En)
- [Введение в Docker: образы, контейнеры и докер-файлы](https://1cloud.ru/blog/docker_start) (Ru)
- [Полное практическое руководство по Docker: с нуля до кластера на AWS](https://habr.com/ru/post/310460/) (Ru)
- [Докер Учебник](https://coderlessons.com/tutorials/noveishie-tekhnologii/uchitsia-doker/doker-uchebnik) (Ru)
- [Продвинутая работа с Docker — Docker-compose](https://1cloud.ru/blog/docker-compose) (Ru)
- [Гайд по Docker: что это такое, зачем его использовать и как с ним работать](https://ru.hexlet.io/blog/posts/gid-docker) (Ru)
- [Развертывание нескольких контейнеров с помощью Docker Compose](https://learn.microsoft.com/ru-ru/azure/cognitive-services/containers/docker-compose-recipe) (Ru)
- [Как оркестровать микросервисы с помощью Docker Compose](https://vk.com/@nuancesprog-kak-orkestrovat-mikroservisy-s-pomoschu-docker-compose?t2fs=79a4e28b10177b8413_3) (Ru)
- [Что такое Docker](https://doka.guide/tools/docker/) (Ru)
- [Мультиконтейнерное приложение и Docker Compose](https://doka.guide/tools/docker-compose/) (Ru)
- [Что такое Docker: краткий экскурс в историю и основные абстракции](https://habr.com/ru/company/southbridge/blog/515508/) (Ru)
- [Лабораторная работа: введение в Docker с нуля. Ваш первый микросервис](https://habr.com/ru/post/346634/) (Ru)
- [Docker: практическое руководство для начинающих](https://techrocks.ru/2019/04/19/docker-guide-for-beginners/) (Ru)
- [Docker: что это и как используется в разработке](https://tproger.ru/articles/chto-takoje-docker/) (Ru)
- [Основы контейнеризации (обзор Docker и Podman)](https://habr.com/ru/post/659049/) (Ru)

---

### Видео уроки ###

[![Основы Docker. Большой практический выпуск](http://img.youtube.com/vi/QF4ZF857m44/0.jpg)](https://www.youtube.com/watch?v=QF4ZF857m44)  
[Основы Docker. Большой практический выпуск](https://www.youtube.com/watch?v=QjT4HuF9gJs) от **Артема Матяшова**

[![Что такое docker за 200 секунд](http://img.youtube.com/vi/HqhgsmThmwA/0.jpg)](https://www.youtube.com/watch?v=HqhgsmThmwA)  
[Что такое docker за 200 секунд](https://www.youtube.com/watch?v=HqhgsmThmwA) от **The Art of Development**

[![Docker для Начинающих - Полный Курс](http://img.youtube.com/vi/n9uCgUzfeRQ/0.jpg)](https://www.youtube.com/watch?v=n9uCgUzfeRQ)  
[Docker для Начинающих - Полный Курс](https://www.youtube.com/watch?v=n9uCgUzfeRQ) от **Владилена Минина**

[![Плейлист Docker уроки от А до Я](http://img.youtube.com/vi/EbEZgdTOHzE/0.jpg)](https://www.youtube.com/playlist?list=PLD5U-C5KK50XMCBkY0U-NLzglcRHzOwAg)  
[Плейлист Docker уроки от А до Я](https://www.youtube.com/playlist?list=PLD5U-C5KK50XMCBkY0U-NLzglcRHzOwAg) от **DKA-DEVELOP**

[![Плейлист Docker](http://img.youtube.com/vi/Sa7uOGczoHc/0.jpg)](https://www.youtube.com/playlist?list=PLU2ftbIeotGoGFC_2lj-OplT_cItXfu48)  
[Плейлист Docker](https://www.youtube.com/playlist?list=PLU2ftbIeotGoGFC_2lj-OplT_cItXfu48) от **letsCode**

---

### Полезности ###

- [DockStation](https://dockstation.io/)
- [Portainer](https://www.portainer.io/)
- [Dockly](https://www.npmjs.com/package/dockly)

<!-- -->

- [A Beginner-Friendly Introduction to Containers, VMs and Docker](https://www.freecodecamp.org/news/a-beginner-friendly-introduction-to-containers-vms-and-docker-79a9e3e119b) (En)
- [Docker Best Practices for Python Developers](https://testdriven.io/blog/docker-best-practices/#dockerfiles) (En)
- [The best Docker base image for your Python application](https://pythonspeed.com/articles/base-image-python-docker-images/) (En)
- [Using Alpine can make Python Docker builds 50× slower](https://pythonspeed.com/articles/alpine-docker-python/) (En)
- [Как устроен Docker и почему он популярен](https://cloud.yandex.ru/blog/posts/2022/03/docker-containers) (Ru)
- [ENTRYPOINT vs CMD: назад к основам](https://habr.com/ru/company/southbridge/blog/329138/) (Ru)
- [50 вопросов по Docker, которые задают на собеседованиях, и ответы на них](https://habr.com/ru/company/southbridge/blog/528206/) (Ru)
- [Первый опыт работы с Docker](https://habr.com/ru/post/663026/) (Ru)
- [Docker на AWS](https://aws.amazon.com/ru/docker/) (Ru)
- [What is Docker networking?](https://www.oreilly.com/content/what-is-docker-networking/) (En)
- [Лучшие альтернативы для Docker](https://habr.com/ru/company/first/blog/598337/) (Ru)
- [Альтернативы Docker](https://techrocks.ru/2021/12/04/docker-alternatives/) (Ru)
