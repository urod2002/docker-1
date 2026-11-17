# Домашнее задание к занятию "Оркестрация группой Docker контейнеров на примере Docker Compose" - Кобалия Иосиф

### Задание 1

https://hub.docker.com/repository/docker/joeybreat/custom-nginx

### Задание 2

img1.png

### Задание 3

img2

img3

img4

### Задание 4

img5

### Задание 5

1) Был запущен compose.yaml т.к. он является предпочтительным файлом по умолчанию. docker-compose.yamlи docker-compose.yml поддерживаются лишь для обратной совместимости

2) include позволяет интегрировать отдельный compose.yaml файл в свой текущий compose.yaml. compose.yaml:

   `include:`

   `- docker-compose.yaml`

   `services:`
     `portainer:`
       `image: portainer/portainer-ce:lts`
       `ports:`
         `- "127.0.0.1:9443:9443"`
       `volumes:`
         `- /var/run/docker.sock:/var/run/docker.sock`
         `- portainer_data:/data`

   `volumes:`
     `portainer_data:`

   img6

3) img7

4) img8

5) img9-11

6) img12

7) img13

