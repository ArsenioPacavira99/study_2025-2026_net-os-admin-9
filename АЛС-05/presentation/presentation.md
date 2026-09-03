---
lang: ru-RU
title: Администрирование локальных сетей
subtitle: Конфигурирование VLAN
author:
  - Пакавира Арсениу Висенте Луиш
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 28 июня 2026

babel-lang: russian
babel-otherlangs: english

toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цели и задачи работы

## Цель лабораторной работы

Получить основные навыки по настройке VLAN на коммутаторах сети.

# Топология сети

## Построенная схема сети

![Построенная топология сети в Packet Tracer](Screenshot_1.png){ width=85% }

# Настройка VTP и VLAN

## VTP Server и создание VLAN

![Настройка VTP-сервера, VLAN и Trunk-портов на msk-donskaya-arsenio-sw-1](Screenshot_2.png){ width=85% }

## VTP Client на msk-donskaya-sw-2

![Настройка VTP-клиента и портов на msk-donskaya-arsenio-sw-2](Screenshot_3.png){ width=85% }

## VTP Client на msk-donskaya-sw-3

![Настройка VTP-клиента и VLAN для серверных портов на msk-donskaya-arsenio-sw-3](Screenshot_4.png){ width=85% }

## Настройка портов доступа на sw-4

![Настройка диапазонов портов доступа на msk-donskaya-arsenio-sw-4](Screenshot_5.png){ width=85% }

## Настройка портов доступа на pavlovskaya-sw-1

![Настройка VTP-клиента и портов доступа на msk-pavlovskaya-arsenio-sw-1](Screenshot_6.png){ width=85% }

# Статическая адресация

## Адресация dk-donskaya

![Настройка IP-адреса на dk-donskaya-arsenio-1](Screenshot_7.png){ width=80% }

## Адресация dk-pavlovskaya

![Настройка IP-адреса на dk-pavlovskaya-arsenio-1](Screenshot_8.png){ width=80% }

## Адресация departments

![Настройка IP-адреса на dep-donskaya-arsenio-1](Screenshot_9.png){ width=80% }

## Адресация adm

![Настройка IP-адреса на adm-donskaya-arsenio-1](Screenshot_10.png){ width=80% }

## Адресация other-donskaya

![Настройка IP-адреса на other-donskaya-arsenio-1](Screenshot_11.png){ width=80% }

## Адресация other-pavlovskaya

![Настройка IP-адреса на other-pavlovskaya-arsenio-1](Screenshot_12.png){ width=80% }

# Адресация серверов

## Web-сервер

![Настройка IP-адреса на сервере web-arsenio](Screenshot_13.png){ width=80% }

## File-сервер

![Настройка IP-адреса на сервере file-arsenio](Screenshot_14.png){ width=80% }

## Mail-сервер

![Настройка IP-адреса на сервере mail-arsenio](Screenshot_15.png){ width=80% }

# Проверка связности

## Проверка VLAN 101

![Проверка доступности устройств из одного и разных VLAN с dk-donskaya-arsenio-1](Screenshot_16.png){ width=80% }

## Проверка VLAN 104

![Проверка доступности устройств из VLAN 104 и недоступности устройства из VLAN 103](Screenshot_17.png){ width=80% }

# Проверка таблиц VLAN

## show vlan на VTP Server

![Проверка VLAN на коммутаторе msk-donskaya-arsenio-sw-1](Screenshot_18.png){ width=85% }

## show vlan на sw-2

![Проверка VLAN и портов на коммутаторе msk-donskaya-arsenio-sw-2](Screenshot_19.png){ width=85% }

## show vlan на sw-3

![Проверка VLAN и серверных портов на коммутаторе msk-donskaya-arsenio-sw-3](Screenshot_20.png){ width=85% }

## show vlan на sw-4

![Проверка распределения портов по VLAN на msk-donskaya-arsenio-sw-4](Screenshot_21.png){ width=85% }

## show vlan на pavlovskaya-sw-1

![Проверка VLAN на коммутаторе msk-pavlovskaya-arsenio-sw-1](Screenshot_22.png){ width=85% }

# Анализ ICMP в режиме Simulation

## Передача ICMP-пакета

![Передача ICMP-пакета в режиме Simulation](Screenshot_23.png){ width=85% }

## ICMP Echo Request

![Структура ICMP Echo Request при передаче от 10.128.3.10 к 10.128.3.15](Screenshot_24.png){ width=85% }

## Обратная передача ICMP-пакета

![Обратная передача ICMP-пакета в режиме Simulation](Screenshot_25.png){ width=85% }

## ICMP Echo Reply

![Структура ICMP Echo Reply при передаче от 10.128.3.15 к 10.128.3.10](Screenshot_26.png){ width=85% }

# Выводы

## Вывод

В ходе лабораторной работы была построена коммутируемая локальная сеть с несколькими VLAN.

Были настроены VTP-домен, Trunk-порты, порты доступа, статические IP-адреса и проверена связность устройств внутри VLAN.

Устройства из одной VLAN успешно обменивались ICMP-пакетами, а устройства из разных VLAN оказались изолированы друг от друга без настройки межсетевой маршрутизации.