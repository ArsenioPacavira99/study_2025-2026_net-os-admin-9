---
lang: ru-RU
title: Администрирование локальных сетей
subtitle: Динамическая маршрутизация
author:
  - Пакавира Арсениу Висенте Луиш
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 1 июля 2026

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

Настроить динамическую маршрутизацию между территориями организации с использованием протокола OSPF.

# Общая топология сети

## Корпоративная сеть

![Общая топология корпоративной сети](Screenshot_1.png){ width=90% }

# Настройка OSPF

## OSPF на msk-donskaya-gw-1

![Настройка OSPF на маршрутизаторе msk-donskaya-arsenio-gw-1](Screenshot_2.png){ width=85% }

## OSPF на msk-q42-gw-1

![Настройка OSPF на маршрутизаторе msk-q42-arsenio-gw-1](Screenshot_3.png){ width=85% }

## OSPF на msk-hostel-gw-1

![Настройка OSPF на маршрутизаторе msk-hostel-arsenio-gw-1](Screenshot_4.png){ width=85% }

## OSPF на sch-sochi-gw-1

![Настройка OSPF на маршрутизаторе sch-sochi-arsenio-gw-1](Screenshot_5.png){ width=85% }

# Прямая связь q42-sochi

## Создание VLAN 7 у провайдера

![Создание VLAN 7 q42-sochi на коммутаторе provider-arsenio-sw-1](Screenshot_6.png){ width=85% }

## Подинтерфейс на msk-q42-gw-1

![Настройка подинтерфейса f0/1.7 на маршрутизаторе msk-q42-arsenio-gw-1](Screenshot_7.png){ width=85% }

## Создание VLAN 7 в Сочи

![Создание VLAN 7 q42-sochi на коммутаторе sch-sochi-arsenio-sw-1](Screenshot_8.png){ width=85% }

## Подинтерфейс на sch-sochi-gw-1

![Настройка подинтерфейса f0/0.7 на маршрутизаторе sch-sochi-arsenio-gw-1](Screenshot_9.png){ width=85% }

# Проверка связи

## Проверка ping

![Проверка доступности удалённых узлов командой ping](Screenshot_10.png){ width=85% }

## Проверка tracert

![Проверка маршрута до удалённых сетей командой tracert](Screenshot_11.png){ width=85% }

## ICMP в режиме Simulation

![Отслеживание движения ICMP-пакета в режиме Simulation](Screenshot_12.png){ width=90% }

# Проверка отказоустойчивости

## Отключение VLAN 6

![Временное отключение интерфейса Vlan6 на коммутаторе provider-arsenio-sw-1](Screenshot_13.png){ width=85% }

## Маршрут после отключения VLAN 6

![Проверка доступности и трассировка маршрута после отключения VLAN 6](Screenshot_14.png){ width=85% }

## ICMP после отключения VLAN 6

![Изменение маршрута ICMP-пакета в режиме Simulation после отключения VLAN 6](Screenshot_15.png){ width=90% }

## Восстановление VLAN 6

![Восстановление интерфейса Vlan6 на коммутаторе provider-arsenio-sw-1](Screenshot_16.png){ width=85% }

## Маршрут после восстановления VLAN 6

![Проверка доступности и трассировка маршрута после восстановления VLAN 6](Screenshot_17.png){ width=85% }

# Проверка OSPF и маршрутов

## OSPF на msk-donskaya-gw-1

![Проверка состояния OSPF и соседей на msk-donskaya-arsenio-gw-1](Screenshot_18.png){ width=85% }

## Таблица маршрутизации msk-donskaya-gw-1

![Таблица маршрутизации на msk-donskaya-arsenio-gw-1](Screenshot_19.png){ width=85% }

## OSPF на msk-q42-gw-1

![Проверка состояния OSPF и соседей на msk-q42-arsenio-gw-1](Screenshot_20.png){ width=85% }

## Таблица маршрутизации msk-q42-gw-1

![Таблица маршрутизации на msk-q42-arsenio-gw-1](Screenshot_21.png){ width=85% }

## OSPF на msk-hostel-gw-1

![Проверка состояния OSPF и соседей на msk-hostel-arsenio-gw-1](Screenshot_22.png){ width=85% }

## Таблица маршрутизации msk-hostel-gw-1

![Таблица маршрутизации на msk-hostel-arsenio-gw-1](Screenshot_23.png){ width=85% }

## OSPF на sch-sochi-gw-1

![Проверка состояния OSPF и соседей на sch-sochi-arsenio-gw-1](Screenshot_24.png){ width=85% }

## Таблица маршрутизации sch-sochi-gw-1

![Таблица маршрутизации на sch-sochi-arsenio-gw-1](Screenshot_25.png){ width=85% }

# Выводы

## Вывод

В ходе лабораторной работы была настроена динамическая маршрутизация по протоколу OSPF между территориями организации.

Была создана прямая связь между кварталом 42 в Москве и филиалом в г. Сочи через VLAN 7, проверена доступность удалённых сетей, а также исследовано изменение маршрута ICMP-пакета при отключении и восстановлении VLAN 6.