---
## Front matter
lang: ru-RU
title: Лабораторная работа №4
subtitle: Работа с программными пакетами
author:
  - Жибицкая Е.Д.
institute:
  - Российский университет дружбы народов, Москва, Россия


## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
 
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
---


# Цель работы

## Цель работы

- Продолжение изучения ОС Linux. Приобретение навыков по работе с менеджерами пакетов.

# Выполнение работы

## 4.4.1. Работа с репозиториями

:::::::::::::: {.columns align=center}
::: {.column width="35%"}
![Изучение содержания /etc/yum.repos.d](image/1.jpg)
:::
::: {.column width="50%"}
Откроем терминал под учетной записью root, перейдем в каталог /etc/yum.repos.d и изучим содержание каталога и файлов репозиториев
:::
::::::::::::::

## 4.4.1
:::::::::::::: {.columns align=center}
::: {.column width="45%"}
Выведем на экран список репозиториев командой dnf repolist - она выводит список всех репозиториев системы.
Также выведем список пакетов, в названии или описании которых есть слово user
:::
::: {.column width="41%"}

![dnf repolist, dnf search user](image/3.jpg)
:::

::::::::::::::

## 4.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

![Пакеты nmap](image/4.jpg)
:::
::: {.column width="40%"}
![Установка nmap](image/5.jpg)
:::
::::::::::::::

## 4.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}
![Удаление nmap](image/6.jpg)
:::
::::::::::::::



## 4.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

![dnf groups list](image/7.jpg)
:::
::: {.column width="45%"}
![LANG=C dnf groups list](image/8.jpg)
:::
::::::::::::::


## 4.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

![RPM Development Tools](image/9.jpg)
:::
::::::::::::::

## 4.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

![dnf history](image/10.jpg)
:::
::::::::::::::


## 4.4.2. Использованеи rpm
:::::::::::::: {.columns align=center}
::: {.column width="45%"}
![dnf list lynx, dnf install lynx --downloadonly](image/11.jpg)
:::
::: {.column width="50%"}
![Установка rpm-пакета](image/12.jpg)
:::
::::::::::::::


## 4.4.2

:::::::::::::: {.columns align=center}
::: {.column width="50%"}
Определим расположение файла - which lynx. Командой rpm  и ключами к ней получим дополнительную информацию - принадлежность к пакетам, содержимое, перечень с документацией и тд
:::
::: {.column width="40%"}

![Определение расположения и получение информации](image/13.jpg)
:::
::::::::::::::


## 4.4.2

:::::::::::::: {.columns align=center}
::: {.column width="40%"}
![Просмотр информации](image/14.jpg)
:::
::: {.column width="40%"}
![Проверка работоспособности](image/14.1.jpg)
:::
::::::::::::::




## 4.4.2

:::::::::::::: {.columns align=center}
::: {.column width="60%"}
![Удаление](image/15.jpg)
:::
::::::::::::::

## 4.4.2

:::::::::::::: {.columns align=center}
::: {.column width="40%"}
Продолжим работу с rpm, установим пакет dnsmasq, сразу определим его местоположение
:::
::: {.column width="45%"}
![Установка dnsmasq](image/16.jpg)
:::

::::::::::::::


## 4.4.2
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

![Информация о содержимом](image/17.jpg)
:::
::: {.column width="37%"}

![Список файлов и ведения о месторасположении](image/18.jpg)
:::
::::::::::::::

## 4.4.2
:::::::::::::: {.columns align=center}
::: {.column width="40%"}
Наконец, выведем расположение и содержание скриптов, выполняемых при установке пакета(описывают различные сценарии до/после установки пакетов), а затем удалим все
:::
::: {.column width="35%"}

![Скрипты](image/20.jpg)
:::
::::::::::::::

# Вывод

## Вывод

- В ходе работы произошло знакомство с dnf, были приобретены навыки по работе с менеджерами пакетов.



