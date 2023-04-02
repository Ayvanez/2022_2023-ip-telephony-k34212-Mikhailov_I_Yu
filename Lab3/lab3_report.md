###### University: [ITMO University](https://itmo.ru/ru/)
###### Faculty: [FICT](https://fict.itmo.ru)
###### Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)
###### Year: 2022/2023
###### Group: K34212
###### Author: Mikhailov Ivan Yuryevich
###### Lab: Lab3
###### Date of create: 02.04.2023
###### Date of finished: .2023
***
# Построение сети ip-телефонии между удаленными маршрутизаторами
### Цель работы: 
Изучить построение сети IP-телефонии между удаленными филиалами с помощью маршрутизаторов Cisco 2811 и коммутаторов Cisco 2950Т.

### Ход Работы
##### Часть 1
1. Конфигурация интерфейса fa0/0 на маршрутизаторе RouterA:

![image](https://user-images.githubusercontent.com/56927592/229346837-36de6b90-0a82-4ecc-8884-210d5c7bd0ab.png)

2. Чтобы добавить serial интерфейс к коммутатору, был добавлен физический компонент WIC-2T:

![image](https://user-images.githubusercontent.com/56927592/229346879-6afdeee2-163f-4406-9b03-cf6269efbb33.png)

3. После этого можно перейти к конфигурации интерфейса s0/3/0:

![image](https://user-images.githubusercontent.com/56927592/229348133-5d812985-95ac-41c2-81b9-458b8f595a00.png)

4. На router1 произведены аналогичные настройки на интерфейсах fa0/0 и s0/3/0:

![image](https://user-images.githubusercontent.com/56927592/229347327-ed226c34-487b-40ba-9094-3577549e0148.png)

5. После включения всех интерфейсов схема сети выглядит следующим образом:

![image](https://user-images.githubusercontent.com/56927592/229347384-328f6452-6930-4824-923b-604739577087.png)

6. На обоих роутерах настроены dhcp пулы для автоматической настройки компьютеров и IP-телефонов в сети. Для этого заданы сети, в которых будут работать DHCP сервера, указаны ip адреса VLAN, для передач данных и включена опция 150 для того чтобы IPтелефоны использовали настройки CallManager Express с TFTP сервера:

![image](https://user-images.githubusercontent.com/56927592/229348056-8aeb9692-d590-4634-accf-6792387f1ed1.png)

7. Настройка динамической маршрутизации на основе протокола RIP второй версии для передачи информации между маршрутизаторами в сети: 

![image](https://user-images.githubusercontent.com/56927592/229348262-94c00bdc-8757-4add-b63d-e909bf354f15.png)

8. Проведена настройка CallManager Express, то есть телефонного сервиса в автоматическом режиме. Задано максимальное количество номеров, присваиваемых IPтелефоном, максимальное количество IP-телефонов, IP адрес голосового шлюза и настроео автоматическое назначение внешних номеров: 

![image](https://user-images.githubusercontent.com/56927592/229348425-0e149fa3-e616-4c3b-811a-1a175c2a676d.png)

9. Произведена настройка vlan портов на обоих switch:

![image](https://user-images.githubusercontent.com/56927592/229348584-cdadb462-67e6-4e46-8440-ea6975db7825.png)

10. Рc переведены на динамическое получение IP адресов.

![image](https://user-images.githubusercontent.com/56927592/229348796-f77b78d1-a72d-4129-a5ce-6c0bee55dc03.png)

11. Выполнено присвоение номеров для всех телефонов, а так же выполнена настройка перенаправления адресации вызовов в соседние сети:

![image](https://user-images.githubusercontent.com/56927592/229349270-13de0ac7-5fda-4a23-b242-92f67d31fced.png)

12. Проведена проверка звонка из одной сети в другую:

![image](https://user-images.githubusercontent.com/56927592/229349316-71ab3765-a561-406c-9522-7d0b0d1d6fc0.png)

13. Проведена проверка доступности пк в разных сетях:

![image](https://user-images.githubusercontent.com/56927592/229349381-cdc447d5-bc13-495b-a183-3ab517f4626d.png)

### Вывод
В ходе выполнения лабораторной работы были реализована телефонная IP свзяь между устройствами в разных сетях с помощью протокала RIP.
