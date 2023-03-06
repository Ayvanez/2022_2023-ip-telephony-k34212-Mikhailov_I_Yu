###### University: [ITMO University](https://itmo.ru/ru/)
###### Faculty: [FICT](https://fict.itmo.ru)
###### Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)
###### Year: 2023/2024
###### Group: K34212
###### Author: Mikhailov Ivan Yuryevich
###### Lab: Lab1
###### Date of create: 06.03.2023
###### Date of finished: 
***
# Базовая настройка ip-телефонов в среде Сisco packet tracer
### Задачи работы:
1. Изучить рабочую среду Cisco Packet Tracer;
2. Ознакомиться с интерфейсами основных устройств, типами кабелей, научиться собирать топологию;
3. Изучить построение сети IP-телефонии с помощью маршрутизатора, коммутатора и IP телефонов Cisco 7960 в среде Packet tracer;

### Ход Работы
##### Часть 1
1. Собрана схема сети

![image](https://user-images.githubusercontent.com/56927592/223090472-a2471b3d-6ffb-4655-b078-b7961419d73f.png)

2. Произведены настройки на DHCP сервере для автоматической настройки адресов на устройствах

![image](https://user-images.githubusercontent.com/56927592/223089900-5fbc009d-91a3-4f62-a7fe-4ccf0e2034bc.png)

3. Проверено получение динамического IP

![image](https://user-images.githubusercontent.com/56927592/223089657-6556bbb8-60e0-4f69-9e8a-ddc9300a2257.png)
![image](https://user-images.githubusercontent.com/56927592/223089764-e0b54caf-06da-4ee2-b160-cb951223e675.png)

4. Выполнено несколько тестовых пингов для проверки настроенных адресов

![image](https://user-images.githubusercontent.com/56927592/223090424-1267a663-d73e-4de6-99f4-d1dbe3641fb6.png)


##### Часть 2

1. Постороена схема сети

![image](https://user-images.githubusercontent.com/56927592/223113594-9b1c0e66-e7b7-4202-a6d7-af48873f17a8.png)

2. Осуществлено подключение IP телефонов к питанию.

![image](https://user-images.githubusercontent.com/56927592/223091972-6f12645c-2937-46d7-9f76-bece3ad8356a.png)

3. Настроен интерфейс fa0/1 а также DHCP сервер на маршрутизаторе CMERouter.

![image](https://user-images.githubusercontent.com/56927592/223109932-d073d1b9-e07e-43ce-a003-4f010339a62e.png)

4. Настроены услуги телефонии Cisco CallManager Express и носера для тедефонов.

![image](https://user-images.githubusercontent.com/56927592/223111072-83b59cd7-c2f3-4d7a-b7e6-fb0a88ccfc6b.png)

5. Настроен voice vlan для работы VoIP.

![image](https://user-images.githubusercontent.com/56927592/223100312-e65f675d-c6c2-4601-99c4-561e4f6c7b18.png)

6. На роутере проверена настройки конфигурации телефонов

![image](https://user-images.githubusercontent.com/56927592/223111760-edb4014b-8582-4fb6-b090-bf5163eed157.png)

7. Осуществлён звонок 

![image](https://user-images.githubusercontent.com/56927592/223112891-5ea1d385-9ba7-4618-94c0-3a0830780b68.png)

### Вывод
В ходе выполнения лабораторной работы были реализованы две схемы сети - с множеством коммутаторов и устройств и и с реализацией IP телефониии стредствами Cisco Packet Tracer.
