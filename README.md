<center>
   <h1>UML - Диаграмма</h1>
</center>

   ![image](https://github.com/user-attachments/assets/d1188c08-2930-427a-b9da-d2c3508c8dd6)

# -Начинаем работу с установки утилиты wget

sudo yum install wget


![Ибрагейн](https://github.com/user-attachments/assets/a4b8d23f-bb36-45c0-bfea-cdfe297b588b)

Полученную ошибку "is not a sudoers file" решаем исправлением конфигурационного файла

![Ибрагейн](https://github.com/user-attachments/assets/5fab7563-f9b7-4dac-87e9-9bfcf5af549b)


Установка гостевых дополнений 

![Ибрагейн](https://github.com/user-attachments/assets/9596fc5f-52bd-4764-b390-cfa75080c7a6)

1.Установка sudo yum install wget

![Ибрагейн](https://github.com/user-attachments/assets/ac6e1134-f69a-49c2-84a8-0aae1b64ba5a)

2. Установка sudo yum install curl

   ![image](https://github.com/user-attachments/assets/f1906bf4-901e-48bf-be05-b8f2ccb4e6b5)

3. Установка sudo yum instal git
   установка утилиты

![image](https://github.com/user-attachments/assets/aab9cad5-eca4-410d-879f-bdee25080b6d)
![image](https://github.com/user-attachments/assets/5ac4f47a-bc92-4b1f-a37b-86bc04ace82e)


4. sudo wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo
   Скачиваем файл репозитория.

![image](https://github.com/user-attachments/assets/314937e1-7b3f-4c7e-aaa4-39b4af7b86c9)

5. sudo yum install docker-ce docker-ce-cli containerd.io
   Устанавливаем docker (Установил)
![image](https://github.com/user-attachments/assets/d982628f-8b01-49a0-bdd8-5f85dc385293)
![image](https://github.com/user-attachments/assets/f70f79b6-c321-47fc-a5e7-76bd2750ee47)

6. sudo systemctl enable docker --now
   Запускаем его и разрешаем автозапуск.
7. sudo yum install curl
Для этого сначала убедимся в наличие пакета curl

8. COMVER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep 'tag_name' | cut -d\" -f4)

• Объявление переменной COMVER, полученной в результате curl запроса, хранящей в себе номер последней версии Docker Compose
![image](https://github.com/user-attachments/assets/14344e8c-2442-4df8-96ca-b03f3a9ed3bd)

9. sudo curl -L "https://github.com/docker/compose/releases/download/$COMVER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose

• Теперь скачиваем скрипт docker-compose последней версии, используя объявленную ранее переменную и помещаем его в каталог /usr/bin

![image](https://github.com/user-attachments/assets/07185c16-bfb1-49da-91de-702e21c879e3)

10. sudo chmod +x /usr/bin/docker-compose

10.1 ![image](https://github.com/user-attachments/assets/8424a52c-3475-4bce-82e4-d436c41eee9d)
Делаем проверку на правильность работы команды (Работает Нормально)


• Предоставление прав на выполнение файла docker-compose.

11. docker-compose --version

• Проверка установленной версии Docker Compose.

![image](https://github.com/user-attachments/assets/8d95fff2-85b7-4574-85cc-fc75e8aa225e)

• Можно скачать git прямо из командной строки прописав Y

12. git clone https://github.com/skl256/grafana_stack_for_docker.git

![image](https://github.com/user-attachments/assets/47eabedc-7e93-43ff-ab93-d3b8d73ea4ac)

13. cd grafana_stack_for_docker

• переход в папку

14. sudo mkdir -p /mnt/common_volume/swarm/grafana/config

• команда создаёт полный путь /mnt/common_volume/swarm/grafana/config, включая все необходимые промежуточные каталоги, если они ещё не существуют.

15. sudo mkdir -p /mnt/common_volume/grafana/{grafana-config,grafana-data,prometheus-data}

• команда создаёт структуру каталогов для Grafana и связанных с ней компонентов, если они ещё не существуют.

16. sudo chown -R $(id -u):$(id -g) {/mnt/common_volume/swarm/grafana/config,/mnt/common_volume/grafana}

• все файлы и каталоги в указанных директориях будут переданы в собственность текущему пользователю и его группе

17. touch /mnt/common_volume/grafana/grafana-config/grafana.ini

• файл grafana.ini уже существует, команда обновит его временные метки (время последнего доступа и изменения). Если файл не существует, команда создаст новый пустой файл с указанным именем по указанному пути.

18. cp config/* /mnt/common_volume/swarm/grafana/config/

• команда копирует все файлы и подкаталоги из директории config в директорию /mnt/common_volume/swarm/grafana/config/

19. mv grafana.yaml docker-compose.yaml 

• команда переименовывает файл grafana.yaml в docker-compose.yaml. Ничего не покажет, но можно проверить при помощи команды ls

20. sudo docker compose up -d

• команда создает и запускает контейнеры в фоновом режиме, используя конфигурацию из файла docker-compose.yml, с правами суперпользователя.

![image](https://github.com/user-attachments/assets/b4520813-766a-4f79-ae15-b37eabf4fe0e)

![image](https://github.com/user-attachments/assets/e0f68f60-bf63-4c33-bfe5-ce5d8321ff5f)

21. sudo vi docker-compose.yaml

• команда открывает файл prometheus.yaml в текстовом редакторе vi с правами суперпользователя.

• Нас перекинет в текстовый редактор

• Что-бы что-то изменить в тесковом редакторе нажмите insert на клавиатуре

• Что бы сохранить что-то в этом документе нажимаем Esc пишем :wq! В этом текставом редакторе мы должны поставить node-exporter после services

![image](https://github.com/user-attachments/assets/8f08dfd6-c010-469e-b2f1-98af5d11bea4)

![image](https://github.com/user-attachments/assets/155da492-d436-4d8c-a162-215d4167883b)

22. sudo vi prometheus.yaml 

• команда открывает файл prometheus.yaml в текстовом редакторе vi с правами суперпользователя.

• /mnt/common_volume/swarm/grafana/config/prometheus.yaml - исправить targets: на exporter:9100,

![image](https://github.com/user-attachments/assets/5479e6be-1f53-465b-b542-dd5c1a2a21b2)


<h1>Grafana</h1>

переходим на сайт localhost:3000

![image](https://github.com/user-attachments/assets/968cd72b-4c7e-4370-b2de-1ba3cfeb0637)

Выбираем dashboard 

![image](https://github.com/user-attachments/assets/610949f6-40fb-4877-b2dc-73ddd6a0433b)

Создаем визуализацию

![image](https://github.com/user-attachments/assets/f13c69ab-29ef-4dca-9e5b-c47ee72d5933)

Выбираем прометеус 

![image](https://github.com/user-attachments/assets/f5205698-a5b2-4a84-8530-bac2e41f50a2)

Код прометеуса: http://prometheus:9090

![image](https://github.com/user-attachments/assets/c54794c8-4cbb-4c1c-a13f-41ffede59005)

Проверка:

![image](https://github.com/user-attachments/assets/fc404e8c-ab97-41f5-80cf-1a7b379b48e4)

Создаю dashboard и ввожу шаблон 1860:

![image](https://github.com/user-attachments/assets/a49cf0fd-5102-481a-87f6-23e217c233aa)

Import dashboard:

![image](https://github.com/user-attachments/assets/0f6b4b7f-ff3b-483d-bddd-fa7446e6ce71)

Нажимаем import:

![image](https://github.com/user-attachments/assets/5fc5786b-e9da-490f-b25b-1e2466d47b04)

<h1>Все готово!</h1>




















