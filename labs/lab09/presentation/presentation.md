---
lang: ru-RU
title: Администрирование локальных сетей
subtitle: Использование протокола STP. Агрегирование каналов
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

Изучить возможности протокола STP и его модификаций по обеспечению отказоустойчивости сети, агрегированию интерфейсов и перераспределению нагрузки между ними.

# Исходная сеть

## Топология сети

![Исходная топология сети после формирования резервных соединений](Screenshot_1.png){ width=85% }

# Проверка ICMP-трафика

## Передача пакета к web-серверу

![Передача ICMP-пакета к серверу web-arsenio через msk-donskaya-arsenio-sw-2](Screenshot_2.png){ width=85% }

## Передача пакета к mail-серверу

![Проверка движения ICMP-пакета к серверу mail-arsenio](Screenshot_3.png){ width=85% }

# Настройка STP

## Состояние STP для VLAN 3

![Состояние STP для VLAN 3 на коммутаторе msk-donskaya-arsenio-sw-2](Screenshot_4.png){ width=80% }

## Назначение корневого коммутатора

Коммутатор msk-donskaya-arsenio-sw-1 был назначен корневым устройством STP для VLAN 3.

![Назначение msk-donskaya-arsenio-sw-1 корневым коммутатором STP](Screenshot_5.png){ width=80% }

# Проверка маршрутов после STP

## Путь к web-серверу

![Передача ICMP-пакета к web-arsenio после настройки корневого коммутатора](Screenshot_6.png){ width=85% }

## Путь к mail-серверу

![Передача ICMP-пакета к mail-arsenio через msk-donskaya-arsenio-sw-3](Screenshot_7.png){ width=85% }

# Настройка PortFast

## PortFast на msk-donskaya-sw-2

![Настройка PortFast на интерфейсах FastEthernet0/1–FastEthernet0/2 коммутатора msk-donskaya-arsenio-sw-2](Screenshot_8.png){ width=80% }

## PortFast на msk-donskaya-sw-3

![Настройка PortFast на интерфейсах FastEthernet0/1–FastEthernet0/2 коммутатора msk-donskaya-arsenio-sw-3](Screenshot_9.png){ width=80% }

# Отказоустойчивость STP

## Проверка восстановления соединения

![Проверка восстановления соединения при отказе канала в режиме STP](Screenshot_10.png){ width=85% }

# Rapid PVST+

## Переключение режима работы

![Переключение коммутатора msk-donskaya-arsenio-sw-1 в режим Rapid PVST+ и сохранение конфигурации](Screenshot_11.png){ width=80% }

## Проверка восстановления в Rapid PVST+

![Проверка восстановления соединения при отказе канала в режиме Rapid PVST+](Screenshot_12.png){ width=85% }

# EtherChannel

## Настройка EtherChannel на sw-1

![Настройка EtherChannel на коммутаторе msk-donskaya-arsenio-sw-1](Screenshot_13.png){ width=80% }

## Настройка EtherChannel на sw-4

![Настройка EtherChannel на коммутаторе msk-donskaya-arsenio-sw-4](Screenshot_14.png){ width=80% }

# Итоговая проверка

## Проверка доступности серверов

![Итоговая проверка доступности серверов после настройки STP, Rapid PVST+ и EtherChannel](Screenshot_15.png){ width=80% }

# Выводы

## Вывод

В ходе лабораторной работы были сформированы резервные соединения между коммутаторами и настроен протокол STP.

Была проверена передача ICMP-пакетов к серверам web и mail.

После перехода на Rapid PVST+ восстановление соединения стало происходить быстрее.

Также было настроено агрегированное соединение EtherChannel между коммутаторами msk-donskaya-arsenio-sw-1 и msk-donskaya-arsenio-sw-4.