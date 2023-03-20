###### University: [ITMO University](https://itmo.ru/ru/)
###### Faculty: [FICT](https://fict.itmo.ru)
###### Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)
###### Year: 2023/2024
###### Group: K34212
###### Author: Mikhailov Ivan Yuryevich
###### Lab: Lab2
###### Date of create: 20.03.2023
###### Date of finished: 20.03.2023
***
# Конфигурация voip в среде Сisco packet tracer
### Цель работы:
Изучить построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.

### Ход Работы
##### Часть 1
1. Схема созданной сети.

![image](https://user-images.githubusercontent.com/56927592/226292711-d91b2b5e-c808-4cec-b908-13ad88cb81e5.png)

2. Переименование и добавление паролей для подключения к роутеру.

![image](https://user-images.githubusercontent.com/56927592/226288093-1fdb76e7-f02e-497c-8b8a-a4d4af564703.png)

3. Проверяем в кофиге что присвоилось верно.

![image](https://user-images.githubusercontent.com/56927592/226288692-9b3f29a3-1805-4864-8dd3-90c6011000dd.png)

4. Поднимаем интерфейс на маршрутизаторе, настраиваем DHCP pool для автоматической настройки ip-телефонов.
Для того чтобы IP-телефоны использовали настройки CallManager Express с TFTP сервера необходимо включить опцию 150.

![image](https://user-images.githubusercontent.com/56927592/226289448-d6e193d1-bd4f-4c8d-ad52-ca30d6c8a1ea.png)

5. Настройка CallManager Express, для работы телефонного сервиса в автоматическом режиме.

![image](https://user-images.githubusercontent.com/56927592/226291109-cd54023d-0e5b-4b65-bb3d-8f7fb8227d89.png)

6. На подключенных портах коммутатора поднят дефолтный vlan для передачи VOIP.

![image](https://user-images.githubusercontent.com/56927592/226291539-887e6ad1-9603-4b86-8c06-d218baefe5b7.png)

7. Создание телефонных линий.
![image](https://user-images.githubusercontent.com/56927592/226291915-f8d45b4c-5f8e-456d-862b-ff30a73d4b51.png)

8. Проверка настроек в конфиге роутера. 

![image](https://user-images.githubusercontent.com/56927592/226292364-c0d526a6-75d1-4b9c-b800-aa48f03a27ca.png)

9. Проверка доступности путем отправки пингов.
![image](https://user-images.githubusercontent.com/56927592/226292482-465c5694-dfee-4bbf-a7a9-b87d921f28fd.png)

10. Реализация звонка между трубками 1111 и 2222.

![image](https://user-images.githubusercontent.com/56927592/226296944-f6bdac8c-fa13-49fe-8480-87dc993d68d7.png)

11. В Packet Tracer окончательная схема выглядит следущим образом.

![image](https://user-images.githubusercontent.com/56927592/226297096-a584b618-a2dd-4d8a-bda2-22aa2e732578.png)

##### Часть 2
1. Создание vlan-ов на коммутаторе. Порта подкючённый к маршрутизатору настрроен в качестве агрегирующего порта, а на порты подключённые к телефонам, установлено 2 сети VLAN для резделения VOIP и данных для ПК.
 
![image](https://user-images.githubusercontent.com/56927592/226317942-991c27f6-9d5e-40c9-a117-ca0d8d924b87.png)

2. Проверка настроек в config. 

![image](https://user-images.githubusercontent.com/56927592/226318343-2cfcd94a-bcb8-4d09-85c8-d896ac1a0468.png)
![image](https://user-images.githubusercontent.com/56927592/226318429-f87c7fde-2fc7-4327-b3ff-dee5f13f7eb5.png)

3. Настройка роутера. Созданы логические подинтерфейсы VLAN 10, VLAN 20, VLAN 50.

![image](https://user-images.githubusercontent.com/56927592/226326013-bb3b5fd4-d323-4428-aa89-d7ac9279f066.png)

5. Созданы DHCP пулы для компьютеров и для телефонов, из пулов исключены адреса интерфейса маршрутизатора и DNS-сервера. 
Помимо этого, выполнена настройка телефонного сервиса в автоматическом режиме для 3 телефонов. Им присвоены номера, указан их тип и кнопка вызова.

![image](https://user-images.githubusercontent.com/56927592/226321369-5006c84b-50c7-4b90-8ed2-c7b4434b0c37.png)
![image](https://user-images.githubusercontent.com/56927592/226321442-592dbb20-32bb-4725-a3bf-e73383b60b62.png)

6. Компьютеры успешно получили автоматические ip адреса с DHCP сервера. Выполнена проверка доступности до компьютеров и телефонов командой ping.

![image](https://user-images.githubusercontent.com/56927592/226321725-62bc6ed0-b6b1-4178-83bf-a263a95e3075.png)

7. Выполнен звонок между телефонами 1111 и 2222.

![image](https://user-images.githubusercontent.com/56927592/226322356-78eb681c-4b0a-422f-af89-24ccb76b51a3.png)

8. Вид окончательной схемы сети.

![image](https://user-images.githubusercontent.com/56927592/226327651-202ae849-b493-4f30-94d1-7fd24663368c.png)

### Вывод:
В ходе выполнения лабораторной работы была настроена телефонная сеть с использованием услуги телефонии Cisco CallManager Express, а так же была изучена настройка технологии VOIP поверх передачи данных.
