---
## Front matter
lang: ru-RU
title: Лабораторная работа №1
subtitle: Установка и конфигурация ОС на виртуальную машину
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

- Приобретение навыков установки ОС на виртуальную машину и настройки базовых сервисов.


# Выполнение работы

## Установка Rocky Linux

:::::::::::::: {.columns align=center}
::: {.column width="50%"}

![Предварительое скачивание версии](image/9.png)
:::
::::::::::::::


## Базовая настройка

:::::::::::::: {.columns align=center}
::: {.column width="40%"}
![Название, образ диска](image/1.png)
:::
::: {.column width="50%"}
![Жесткий диск](image/2.png)
:::
::::::::::::::

## Установка 
:::::::::::::: {.columns align=center}
::: {.column width="45%"}

![Имя пользователя](image/5.png)
:::
::: {.column width="50%"}

Выбор основного языка, настройка клавиатуры, имя пользователя и пароль для root
:::
::::::::::::::


## Установка

:::::::::::::: {.columns align=center}
::: {.column width="50%"}
![Отключение KDUMP](image/3.png)
:::
::: {.column width="50%"}
![Сеть и имя узла](image/4.png)
:::
::::::::::::::

## Подключение образа диска

:::::::::::::: {.columns align=center}
::: {.column width="50%"}

![Образ диска](image/6.png)
:::
::::::::::::::

## Выполнение задания. Изучение характеристик

:::::::::::::: {.columns align=center}
::: {.column width="50%"}
![Версия ядра, частота процессора](image/7.png)
:::
::: {.column width="50%"}
![Остальные характеристики](image/8.png)
:::
::::::::::::::


# Вывод

## Вывод

- В ходе работы была установлена машина Rocky Linux, проведена ее настройка, изучены различные ее характеристики.


