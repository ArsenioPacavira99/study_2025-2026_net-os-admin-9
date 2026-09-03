---
lang: ru-RU
title: Администрирование локальных сетей
subtitle: Знакомство с Cisco Packet Tracer
author:
  - Пакавира Арсениу Висенте Луиш
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 27 июня 2026

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

Изучить интерфейс Cisco Packet Tracer и получить практические навыки построения локальной сети с использованием концентратора, коммутатора и маршрутизатора.

# Сеть на базе концентратора

## Топология с Hub-PT

![Модель простой сети с концентратором](Screenshot_1.png){ width=70% }

## Настройка IP-адресов

![Настройка статического IP-адреса на PC0-Arsenio](Screenshot_2.png){ width=80% }

## Создание Simple PDU

![Создание тестового PDU в режиме Simulation](Screenshot_6.png){ width=85% }

## Передача ARP через концентратор

![Передача ARP-пакетов через концентратор](Screenshot_7.png){ width=85% }

## OSI Model для ARP

![Информация о PDU на вкладке OSI Model](Screenshot_8.png){ width=80% }

## Структура ARP-пакета

![Структура ARP-пакета в PDU Details](Screenshot_9.png){ width=85% }

## Структура ICMP-пакета

![Структура ICMP-пакета в PDU Details](Screenshot_11.png){ width=85% }

## Коллизия в сети с концентратором

![Возникновение коллизии при одновременной передаче](Screenshot_12.png){ width=85% }

# Сеть на базе коммутатора

## Топология с Cisco 2950-24

![Модель сети с концентратором и отдельной сети с коммутатором](Screenshot_14.png){ width=85% }

## Настройка PC4

![Настройка IP-адреса на PC4-Arsenio](Screenshot_15.png){ width=80% }

## Передача ARP и ICMP через коммутатор

![Передача ARP и ICMP в сети с коммутатором](Screenshot_19.png){ width=85% }

## ARP Reply через коммутатор

![Структура ARP-пакета в сети с коммутатором](Screenshot_20.png){ width=85% }

## ICMP Echo Reply

![Структура ICMP-пакета в сети с коммутатором](Screenshot_22.png){ width=85% }

## Передача без коллизий

![Одновременная передача ICMP-пакетов через коммутатор](Screenshot_23.png){ width=85% }

# Объединение концентратора и коммутатора

## Соединение hub и switch

![Соединение концентратора и коммутатора кроссовым кабелем](Screenshot_24.png){ width=85% }

## Коллизия между сегментами

![Возникновение коллизии при обмене между сегментами hub и switch](Screenshot_25.png){ width=85% }

## Распространение ARP-пакетов

![Распространение ARP-пакетов между hub и switch](Screenshot_26.png){ width=85% }

## Успешная доставка после повторной передачи

![Успешная передача ICMP-пакетов после коллизии](Screenshot_27.png){ width=85% }

# Служебные протоколы

## STP BPDU

![Структура STP BPDU на коммутаторе](Screenshot_28.png){ width=85% }

## STP в списке событий

![Отображение STP-пакетов в списке событий](Screenshot_29.png){ width=85% }

# Подключение маршрутизатора

## Добавление Cisco 2811

![Добавление маршрутизатора Cisco 2811 в общую схему сети](Screenshot_30.png){ width=85% }

## Настройка интерфейса маршрутизатора

![Настройка интерфейса FastEthernet0/0 маршрутизатора](Screenshot_31.png){ width=85% }

## ARP-запрос к маршрутизатору

![ARP-запрос от PC3-Arsenio к маршрутизатору](Screenshot_32.png){ width=85% }

## ICMP-обмен с маршрутизатором

![Передача ICMP-пакетов между PC3-Arsenio и Router0-Arsenio](Screenshot_33.png){ width=85% }

## Структура CDP-кадра

![Структура CDP-пакета в PDU Information](Screenshot_34.png){ width=85% }

# Выводы

## Вывод

В ходе лабораторной работы была построена локальная сеть в Cisco Packet Tracer с использованием концентратора, коммутатора и маршрутизатора.

Были настроены статические IP-адреса, выполнена проверка связи между узлами и исследована передача пакетов ARP, ICMP, STP и CDP.
