---
## Front matter
lang: ru-RU
title: Лабораторная работа №5
subtitle: Управление системными службами
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

- Продолжение изучения ОС Linux. Знакомство и получение навыков управления системными службами операционной системы посредством systemd.

# Выполнение работы

## 5.4.1. Управление сервисами

:::::::::::::: {.columns align=center}
::: {.column width="35%"}
![Статус и установка службы Very Secure FTP](image/1.jpg)
:::
::: {.column width="50%"}
![Запуск и статус службы Very Secure FTP](image/2.jpg)
:::
::::::::::::::

## 5.4.1
:::::::::::::: {.columns align=center}
::: {.column width="45%"}
![Добавление автозапуска](image/3.jpg)
:::
::: {.column width="50%"}

![Отключение автозапуска](image/4.jpg){#fig:004 width=70%}
:::

::::::::::::::

## 5.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

Выведем на экран символические ссылки, ответственные за запуск различных сервисов. Снова добавим автозапуск и повторим вывод ссылок.
:::
::: {.column width="40%"}
![Символические ссылки](image/5.jpg)
:::
::::::::::::::

## 5.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}
![Статус](image/6.jpg)
:::
::: {.column width="40%"}

Опять проверим статус. Увидим, что для файла юнита состояние изменено.
:::
::::::::::::::



## 5.4.1
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

![Список зависимостей юнита](image/7.jpg)
:::
::: {.column width="50%"}
![Список юнитов, которые зависят от данного юнита](image/8.jpg)
:::
::::::::::::::


## 5.4.2. Конфликты юнитов
:::::::::::::: {.columns align=center}
::: {.column width="45%"}
![Установка iptables](image/9.jpg)
:::
::: {.column width="50%"}
![Статусы firewalld и iptables](image/10.jpg)
:::
::::::::::::::


## 5.4.2

:::::::::::::: {.columns align=center}
::: {.column width="50%"}
Попробуем запустить их. Увидим, что сделать одновременно это невозможно - одна из служб дезактивируется при запуске второй.
:::
::: {.column width="40%"}

![Запуск конфликтующих служб](image/11.jpg)
:::
::::::::::::::


## 5.4.2

:::::::::::::: {.columns align=center}
::: {.column width="40%"}
![cat /usr/lib/systemd/system/firewalld.service ](image/12.jpg)
:::
::: {.column width="50%"}
![cat /usr/lib/systemd/system/iptables.service](image/13.jpg)
:::
::::::::::::::



## 5.4.2

:::::::::::::: {.columns align=center}
::: {.column width="40%"}
![Работа с iptables и  firewalld](image/14.jpg)
:::
::: {.column width="60%"}
Выгрузим службу iptables, запустим firewalld, заблокируем запуск iptables (создана символическая ссылка на /dev/null для /etc/systemd/system/iptables.service) и попробуем запустить. Также попробуем добавить службу в автозапуск
:::
::::::::::::::

## 5.4.3. Изолируемые цели

:::::::::::::: {.columns align=center}
::: {.column width="45%"}
![Списки целей](image/15.jpg)
:::

::::::::::::::


## 5.4.3
:::::::::::::: {.columns align=center}
::: {.column width="40%"}

![Изолируемые цели](image/16.jpg)
:::
::: {.column width="50%"}

![Режим восстановления и перезапуск](image/17.jpg)
:::
::::::::::::::

## 5.4.4. Цель по умолчанию
:::::::::::::: {.columns align=center}
::: {.column width="40%"}
Выведем установленную по умолчанию цель - systemctl get-default. Далее, для запуска по умолчанию текстового режима введем systemctl set-default multi-user.target
:::
::: {.column width="50%"}

![Цель по умолчанию](image/18.jpg)
:::
::::::::::::::

## 5.4.4
:::::::::::::: {.columns align=center}
::: {.column width="40%"}
![Возвращение графического режима](image/19.jpg)
:::
::: {.column width="35%"}

![Проверка](image/20.jpg)
:::
::::::::::::::

# Вывод

## Вывод

- В ходе работы было произведено знакомство с системными службами операционной системы. Были получены навыки управления системными службами посредством systemd.


