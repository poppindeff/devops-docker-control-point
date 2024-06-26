Практическое задание №4
Описание: Работа с системой Docker
Результатом работы должен быть составлен отчет о выполненной работе в
формате .pdf или пришлите ссылку на репозиторий в Gitlab/Github
Описание задания:
1. Создайте сборку Docker контейнера на базе образа Debian или Ubuntu.
a. Установите в сборку сл. утилиты: wget, curl, nginx
b. Nginx должен запускаться при старте образа
c. Скопируйте из локальной директории в контейнер файлы
произвольного сайта. Сайт должен открываться через браузер
2. Из получившейся сборки соберите контейнер. Контейнер должен быть
доступен по портам 80 и 443
3. Параллельно создайте контейнер произвольной СУБД (PostgreSQL,
MariaDB, MySQL, Oracle и т.д.)
a. СУБД должена быть доступна по базовому порту.
b. Загрузите в контейнер с СУБД тестовую бузу данных.
c. Не забудьте указать пароль для пользователя root(администратора)
Процесс сборки контейнера
Создайте файл с названием – Dockerfile
FROM – указывает образ
RUN – выполнение любой команды в командной строке, терминале
COPY – копирование из локальной папки в контейнер
ENV – указание переменного окружения
ENTRYPOINT – запуск команды при старте контейнера
CMD — описывает команду с аргументами, которую нужно выполнить когда
контейнер будет запущен. Аргументы могут быть переопределены при запуске
контейнера. В файле может присутствовать лишь одна инструкция CMD.
WORKDIR – указание директории, в которой будет выполнятся последующая
работа.
docker build . –tag=название_образа.
Статьи:
https://www.dmosk.ru/miniinstruktions.php?mini=docker-self-image
https://habr.com/ru/companies/ruvds/articles/439980/
