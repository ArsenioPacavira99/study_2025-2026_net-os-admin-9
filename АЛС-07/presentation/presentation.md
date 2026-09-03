---
lang: ru-RU
title: Администрирование локальных сетей
subtitle: Учёт физических параметров сети
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

Получить навыки работы с физической рабочей областью Cisco Packet Tracer, а также изучить влияние физических параметров сети на работоспособность соединений.

# Физическая рабочая область Packet Tracer

## Город Moscow

![Физическая рабочая область Packet Tracer с городом Moscow](Screenshot_1.png){ width=85% }

## Территории Donskaya и Pavlovskaya

![Размещение зданий Donskaya и Pavlovskaya в физической рабочей области](Screenshot_2.png){ width=80% }

## Серверное помещение Donskaya

![Размещение серверного помещения и оконечных устройств в здании Donskaya](Screenshot_3.png){ width=85% }

## Серверная стойка Donskaya

![Серверная стойка территории Donskaya](Screenshot_4.png){ width=65% }

## Оборудование на территории Pavlovskaya

![Размещение оборудования на территории Pavlovskaya](Screenshot_5.png){ width=80% }

## Серверная стойка Pavlovskaya

![Серверная стойка территории Pavlovskaya](Screenshot_6.png){ width=65% }

# Проверка связи до учёта длины кабеля

## Проверка доступности коммутатора

![Проверка доступности msk-pavlovskaya-arsenio-sw-1 до учёта длины кабеля](Screenshot_7.png){ width=80% }

# Учёт физических параметров сети

## Включение Cable Length Effects

![Включение параметра Enable Cable Length Effects](Screenshot_8.png){ width=85% }

## Длина медного соединения

![Сведения о длине медного соединения между территориями](Screenshot_9.png){ width=85% }

## Потеря связи после увеличения расстояния

![Проверка недоступности удалённого коммутатора после учёта длины кабеля](Screenshot_10.png){ width=80% }

# Восстановление соединения

## Настройка повторителя

![Установка модулей PT-REPEATER-NM-1FFE и PT-REPEATER-NM-1CFE на повторитель](Screenshot_11.png){ width=75% }

## Схема с повторителями

![Логическая схема сети после добавления повторителей](Screenshot_12.png){ width=85% }

## Итоговая проверка связи

![Итоговая проверка доступности после добавления повторителей](Screenshot_13.png){ width=80% }

# Выводы

## Вывод

В ходе лабораторной работы была изучена физическая рабочая область Cisco Packet Tracer.

Использование оптоволоконного участка между территориями позволило восстановить соединение и подтвердить необходимость учёта физических параметров сети при проектировании инфраструктуры.