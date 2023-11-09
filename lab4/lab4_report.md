University: [ITMO University](https://itmo.ru/ru/)\
Faculty: [FICT](https://fict.itmo.ru)\
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)\
Year: 2023/2024\
Group: K4110c\
Author: Solovev Pavel Alekseevich\
Lab: Lab4\
Date of create: 08.11.2023\
Date of finished: 09.11.2023

## Выполнение работы

Запускаем minikube с включенным calico и количеством нод равным 2.
![start kuber with calico](pictures/start-kuber-with-calico.png)

Сразу не завелось, поднимаем еще одну ноду вручную.
![one more node](pictures/node.png)

Проверяем, запустились ли поды калико.
![calico pods started](pictures/calico-pods.png)

Назначаем метки нодам. Последней командой можно проверить, присвоились ли метки им.
![added labels](pictures/labels.png)

Устанавливаем calicoctl.
![started calico ctl](pictures/calico-ctl.png)

С помощью вышеупомянутого инструмента удаляем стандартный ippool.
![delete default ippool](pictures/old-ippool.png)

Создаем и проверяем новые ippool.
![create new ippool](pictures/new-ippool.png)

Экспоузим порт, порт-форвардим и попадаем на страничку сервиса. IP и Name меняются в зависимости от того, на какую ноду отправит нас LoadBalancer. Пробуем пингануть один под из-под второго и наоборот. Все успехово!
![ping one pod from another](pictures/ping.png)

## Схема

![scheme](pictures/kuber-lab4.drawio.png)