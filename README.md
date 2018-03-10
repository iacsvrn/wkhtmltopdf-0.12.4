# wkhtmltopdf-0.12.4

### Вернее Ubuntu 16.04 LTS desktop + wkhtmltopdf 0.12.4 (with patched qt).

+ Репозитории берём отсюда: https://repogen.simplylinux.ch/index.php
+ Правим репозитории: nano /etc/apt/sources.list:

###### Ubuntu Main Repos
+ deb http://ru.archive.ubuntu.com/ubuntu/ xenial main restricted universe multiverse 
+ deb-src http://ru.archive.ubuntu.com/ubuntu/ xenial main restricted universe multiverse 
###### Ubuntu Update Repos
+ deb http://ru.archive.ubuntu.com/ubuntu/ xenial-security main restricted universe multiverse 
+ deb http://ru.archive.ubuntu.com/ubuntu/ xenial-updates main restricted universe multiverse 
+ deb http://ru.archive.ubuntu.com/ubuntu/ xenial-proposed main restricted universe multiverse 
+ deb http://ru.archive.ubuntu.com/ubuntu/ xenial-backports main restricted universe multiverse 
+ deb-src http://ru.archive.ubuntu.com/ubuntu/ xenial-security main restricted universe multiverse 
+ deb-src http://ru.archive.ubuntu.com/ubuntu/ xenial-updates main restricted universe multiverse 
+ deb-src http://ru.archive.ubuntu.com/ubuntu/ xenial-proposed main restricted universe multiverse 
+ deb-src http://ru.archive.ubuntu.com/ubuntu/ xenial-backports main restricted universe multiverse 
###### Ubuntu Partner Repo
+ deb http://archive.canonical.com/ubuntu xenial partner
+ deb-src http://archive.canonical.com/ubuntu xenial partner

Обвновляемся:
+ aptitude clean && aptitude update && aptitude upgrade -y

Так как обновилось ядро, требуется ребут:

+ reboot

После перезагрузки, берём файл отсюда: ( https://github.com/wkhtmltopdf/wkhtmltopdf/releases/tag/0.12.4 ). Меня интересует в данном случае: wkhtmltox-0.12.4_linux-generic-amd64.tar.xz. Качаем, ставим, делаем симлинк.

+ cd /tmp
+ wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.4/wkhtmltox-0.12.4_linux-generic-amd64.tar.xz
+ cd /opt
+ tar xf /tmp/wkhtmltox-0.12.4_linux-generic-amd64.tar.xz
+ ln -s /opt/wkhtmltox/bin/wkhtmltopdf /usr/local/bin/wkhtmltopdf

-------
Всё. На данном этапе установка завершена
