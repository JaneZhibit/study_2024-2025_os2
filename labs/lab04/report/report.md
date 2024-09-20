---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Дисциплина: Оcновы администрирования операционных систем"
author: "Жибицкая Евгения Дмитриевна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Продолжение изучения ОС Linux. Приобретение навыков по работе с менеджерами пакетов.


# Выполнение лабораторной работы

Откроем терминал под учетной записью root, перейдем в каталог /etc/yum.repos.d и изучим содержание каталога и файлов репозиториев(рис. [-@fig:001]).

![Изучение содержания /etc/yum.repos.d](image/1.jpg){#fig:001 width=70%}


Выведем на экран список репозиториев командой dnf repolist - она выводит список всех репозиториев системы.
Также выведем список пакетов, в названии или описании которых есть слово user:
dnf search user(рис. [-@fig:002]).


![dnf repolist, dnf search user](image/3.jpg){#fig:002 width=70%}


Изучим информацию по имеющимся пакетам nmap(рис. [-@fig:003]).

![Пакеты nmap](image/4.jpg){#fig:003 width=70%}


Установим nmap:
dnf install nmap
dnf install nmap\*
Различие команд заключается в том, что в первом случае установится пакет с точным названием, а во втором все пакеты, начинающиеся с этих букв(рис. [-@fig:004]).

![Установка nmap](image/5.jpg){#fig:004 width=70%}


Далее сразу удалим только что скачанные пакеты(рис. [-@fig:005]).

![Удаление nmap](image/6.jpg){#fig:005 width=70%}



Затем получим список имеющихся групп пакетов(рис. [-@fig:006]) и (рис. [-@fig:007]).

![dnf groups list](image/7.jpg){#fig:006 width=70%}


![LANG=C dnf groups list](image/8.jpg){#fig:007 width=70%}



Установим и удалим пакеты RPM(рис. [-@fig:008]).

![RPM Development Tools](image/9.jpg){#fig:008 width=70%}


Также ознакомимся с историей использования команды и отменим какое-то действие,например, пятое(рис. [-@fig:009]).

![dnf history](image/10.jpg){#fig:009 width=70%}




Перейдем к работе с rpm. Скачаем rpm пакет lynx.
dnf list lynx
dnf install lynx --downloadonly(рис. [-@fig:010]).

![dnf list lynx, dnf install lynx --downloadonly](image/11.jpg){#fig:010 width=70%}


Перейдем в каталог, в который установился пакет и установим rpm туда(рис. [-@fig:011]).

![Установка rpm-пакета](image/12.jpg){#fig:011 width=70%}


Определим расположение файла - which lynx. Командой rpm  и ключами к ней получим дополнительную информацию - принадлежность к пакетам, содержимое, перечень с документацией и тд(рис. [-@fig:012]) и (рис. [-@fig:013]).

![Определение расположения и получение информации](image/13.jpg){#fig:012 width=70%}


![Просмотр информации](image/14.jpg){#fig:013 width=70%}


В отдельном терминале под своей учётной записью запустм текстовый браузер lynx, чтобы проверить корректность установки пакета(рис. [-@fig:014]).

![Проверка работоспособности](image/14.1.jpg){#fig:014 width=70%}



Удалим этот пакет, вернувшись к root(рис. [-@fig:015]).

![Удаление](image/15.jpg){#fig:015 width=70%}


Продолжим работу с rpm, установим пакет dnsmasq, сразу определим его местоположение(рис. [-@fig:016]).

![Установка dnsmasq](image/16.jpg){#fig:016 width=70%}


Опять получим различную необходимую информацию
(рис. [-@fig:017]), (рис. [-@fig:018]).

![Информация о содержимом](image/17.jpg){#fig:017 width=70%}


![Список файлов и сведения о месторасположении](image/18.jpg){#fig:018 width=70%}


Наконец, выведем расположение и содержание скриптов, выполняемых при установке пакета(описывают различные сценарии до/после установки пакетов), а затем удалим все(рис. [-@fig:019]).

![Скрипты](image/20.jpg){#fig:019 width=70%}


# Ответы на контрольные вопросы

1. Для поиска пакета RPM, содержащего файл useradd, можно использовать команду:
      rpm -qf $(which useradd)
      рис. [-@fig:020]) 

![Пример](image/13.jpg){#fig:020 width=70%}
      
   

2. Для показа имени группы DNF, которая содержит инструменты безопасности, можно использовать команду:
      dnf group list
       (рис. [-@fig:021]).

![dnf groups list](image/7.jpg){#fig:021 width=70%}
   
   
3. Для установки RPM-файла, который не находится в репозиториях, нужна команда:
      sudo rpm -ivh имя_пакета.rpm
   

4. Чтобы проверить, что пакет RPM, не содержит опасного кода сценария, можно использовать команду:
      rpm --checksig имя_пакета.rpm
   
   Это проверит подпись RPM-пакета.

5. Для отображения всей документации, связанной с RPM, можно использовать команду:
      rpm -qd имя_пакета
    (рис. [-@fig:022]).

![Список файлов и сведения о месторасположении](image/18.jpg){#fig:022 width=70%}

6. Чтобы определить, какому пакету RPM принадлежит файл, используйте команду:
      rpm -qf /путь/к/файлу
  


# Выводы

В ходе работы произошло знакомство с dnf, были приобретеныы навки по работе с менеджерами пакетов.

# Список литературы{.unnumbered}

 [ТУИС](https://esystem.rudn.ru/pluginfile.php/2400691/mod_resource/content/4/005-dnf.pdf)

