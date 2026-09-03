---
lang: ru-RU
title: Администрирование локальных сетей
subtitle: Статическая маршрутизация в Интернете. Настройка
author:
  - Пакавира Арсениу Висенте Луиш
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 30 июня 2026

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

Настроить взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания в 42-м квартале в Москве и сетью филиала в г. Сочи.

# Топология сети

## Общая схема сети

![Общая схема сети в Cisco Packet Tracer](Screenshot_1.png){ width=85% }

# Настройка связи между территориями

## VLAN на коммутаторе провайдера

![Создание VLAN 5 и VLAN 6 на provider-arsenio-sw-1](Screenshot_2.png){ width=75% }

## Маршрутизатор msk-donskaya-arsenio-gw-1

![Настройка сабинтерфейсов, маршрутов и ACL для NAT на msk-donskaya-arsenio-gw-1](Screenshot_3.png){ width=80% }

# Настройка квартала 42

## Сабинтерфейсы маршрутизатора квартала 42

![Настройка интерфейсов и сабинтерфейсов на msk-q42-arsenio-gw-1](Screenshot_4.png){ width=80% }

## Статическая маршрутизация в квартале 42

![Настройка статической маршрутизации на msk-q42-arsenio-gw-1](Screenshot_5.png){ width=80% }

## VLAN 201 на коммутаторе квартала 42

![Настройка VLAN 201 и портов на msk-q42-arsenio-sw-1](Screenshot_6.png){ width=75% }

# Настройка сети общежития

## VLAN 202 и VLAN 301

![Настройка VLAN 202, VLAN 301 и маршрутизации на msk-hostel-arsenio-gw-1](Screenshot_7.png){ width=80% }

## Коммутатор сети общежития

![Настройка VLAN 301 на msk-hostel-arsenio-sw-1](Screenshot_8.png){ width=75% }

# Настройка филиала в Сочи

## Маршрутизатор sch-sochi-arsenio-gw-1

![Настройка сабинтерфейсов и маршрута по умолчанию на sch-sochi-arsenio-gw-1](Screenshot_9.png){ width=80% }

# Настройка оконечных устройств

## Компьютер pc-q42-arsenio

![Настройка IP-адреса на pc-q42-arsenio](Screenshot_10.png){ width=70% }

## Компьютер pc-hostel-arsenio

![Настройка IP-адреса на pc-hostel-arsenio](Screenshot_11.png){ width=70% }

## Компьютер pc-sch-sochi-arsenio

![Настройка IP-адреса на pc-sch-sochi-arsenio](Screenshot_12.png){ width=70% }

# Проверка связности

## Ping с admin-donskaya-arsenio

![Проверка доступности удалённых узлов с admin-donskaya-arsenio](Screenshot_13.png){ width=75% }

## Tracert с admin-donskaya-arsenio

![Трассировка маршрутов с admin-donskaya-arsenio](Screenshot_14.png){ width=75% }

## Ping с pc-q42-arsenio

![Проверка доступности удалённых узлов с pc-q42-arsenio](Screenshot_15.png){ width=75% }

## Tracert с pc-q42-arsenio

![Трассировка маршрутов с pc-q42-arsenio](Screenshot_16.png){ width=75% }

## Ping с pc-hostel-arsenio

![Проверка доступности удалённых узлов с pc-hostel-arsenio](Screenshot_17.png){ width=75% }

## Tracert с pc-hostel-arsenio

![Трассировка маршрутов с pc-hostel-arsenio](Screenshot_18.png){ width=75% }

## Ping с pc-sch-sochi-arsenio

![Проверка доступности удалённых узлов с pc-sch-sochi-arsenio](Screenshot_19.png){ width=75% }

## Tracert с pc-sch-sochi-arsenio

![Трассировка маршрутов с pc-sch-sochi-arsenio](Screenshot_20.png){ width=75% }

# Таблицы маршрутизации

## Таблица маршрутизации msk-donskaya-arsenio-gw-1

![Таблица маршрутизации на msk-donskaya-arsenio-gw-1](Screenshot_21.png){ width=75% }

## Таблица маршрутизации msk-q42-arsenio-gw-1

![Таблица маршрутизации на msk-q42-arsenio-gw-1](Screenshot_22.png){ width=75% }

## Таблица маршрутизации msk-hostel-arsenio-gw-1

![Таблица маршрутизации на msk-hostel-arsenio-gw-1](Screenshot_23.png){ width=75% }

## Таблица маршрутизации sch-sochi-arsenio-gw-1

![Таблица маршрутизации на sch-sochi-arsenio-gw-1](Screenshot_24.png){ width=75% }

# Выводы

## Вывод

В ходе лабораторной работы была настроена связь между несколькими территориями организации в Cisco Packet Tracer.

Были созданы VLAN, настроены сабинтерфейсы маршрутизаторов, добавлены статические маршруты между территориями и подготовлена настройка NAT.

Проверка с помощью команд ping, tracert и show ip route подтвердила корректную работу маршрутизации между кварталом 42, сетью общежития, территорией Донской и филиалом в г. Сочи.