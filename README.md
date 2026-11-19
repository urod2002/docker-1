# Домашнее задание к занятию "Оркестрация группой Docker контейнеров на примере Docker Compose" - Кобалия Иосиф

### Задание 1

https://hub.docker.com/repository/docker/joeybreat/custom-nginx

### Задание 2

![img1.png](https://github.com/urod2002/docker-1/blob/main/img/img1.png?raw=true)

### Задание 3

Ctrl+C отправил сигнал прерывания основному процессу nginx, который завершился, вследствие чего Docker остановил контейнер.

![img2.png](https://github.com/urod2002/docker-1/blob/main/img/img2.png?raw=true)

![img3.png](https://github.com/urod2002/docker-1/blob/main/img/img3.png?raw=true)

Docker продолжал перенаправлять 127.0.0.1:8080 на порт 80 контейнера, хотя nginx уже слушал порт 81.

![img4.png](https://github.com/urod2002/docker-1/blob/main/img/img4.png?raw=true)

### Задание 4

![img5.png](https://github.com/urod2002/docker-1/blob/main/img/img5.png?raw=true)

### Задание 5

1. Был запущен compose.yaml т.к. он является предпочтительным файлом по умолчанию. docker-compose.yaml и docker-compose.yml поддерживаются лишь для обратной совместимости

2. include позволяет интегрировать отдельный compose.yaml файл в свой текущий compose.yaml.

   ![img6.png](https://github.com/urod2002/docker-1/blob/main/img/img6.png?raw=true)

3. ![img7.png](https://github.com/urod2002/docker-1/blob/main/img/img7.png?raw=true)

4. ![img8.png](https://github.com/urod2002/docker-1/blob/main/img/img8.png?raw=true)

5. ![img9.png](https://github.com/urod2002/docker-1/blob/main/img/img9.png?raw=true)
   ![img10.png](https://github.com/urod2002/docker-1/blob/main/img/img10.png?raw=true)
   ![img11.png](https://github.com/urod2002/docker-1/blob/main/img/img11.png?raw=true)

6. ![img12.png](https://github.com/urod2002/docker-1/blob/main/img/img12.png?raw=true)

7. ![img13.png](https://github.com/urod2002/docker-1/blob/main/img/img13.png?raw=true)

   После переименования compose.yaml остался docker-compose.yaml, в котором описан только registry.
   Но контейнер Portainer продолжал существовать. Docker Compose обнаружил контейнер, принадлежащий текущему проекту, но больше не описанный в его конфигурации. Такие контейнеры называются orhpan - осиротевшие.
   Docker Compose предложил удалить orphans контейнеры с помощью добавления флага --remove-orphans.

   ![img14.png](https://github.com/urod2002/docker-1/blob/main/img/img14.png?raw=true)

