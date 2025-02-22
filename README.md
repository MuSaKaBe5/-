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




