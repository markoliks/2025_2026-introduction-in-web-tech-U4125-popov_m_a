# DevOps Lab 2

University: [ITMO University](https://itmo.ru)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io)  
Year: 2025/2026  
Author: Popov Mark  
Lab: Lab2  
Date of create: 17.03.2026  
Date of finished: -  

## Цель работы

Настроить CI/CD pipeline для автоматической сборки и публикации Docker-образа в Docker Hub с использованием GitHub Actions.

## Ход работы

### 1. Создание Docker Hub репозитория

Был создан репозиторий Docker Hub:

markolk/my-flask-app

### 2. Подготовка файлов приложения

В репозиторий были добавлены следующие файлы:

- app.py — Flask-приложение
- requirements.txt — зависимости проекта
- Dockerfile — инструкция для сборки Docker-образа

### 3. Настройка GitHub Actions

Был создан workflow-файл:

.github/workflows/docker-build.yml

Pipeline выполняет следующие действия:

1. Checkout репозитория  
2. Настройку Docker Buildx  
3. Авторизацию в Docker Hub  
4. Сборку Docker-образа  
5. Публикацию образа в Docker Hub  

### 4. Настройка секретов

Для авторизации в Docker Hub был добавлены секреты:
- DOCKER_USERNAME
- DOCKER_PASSWORD

### 5. Результат

После коммита в ветку main GitHub Actions автоматически запустил pipeline.  
Pipeline успешно выполнил сборку Docker-образа и публикацию в Docker Hub.

Docker-образ был успешно загружен в репозиторий:

markolk/my-flask-app:latest

<img width="1265" height="1012" alt="image" src="https://github.com/user-attachments/assets/e222dce9-b38b-4a18-97ef-6e6e1ff6b665" />
<img width="1238" height="794" alt="image" src="https://github.com/user-attachments/assets/2ebee606-fc88-4f40-a867-626e459d8d67" />
<img width="1271" height="881" alt="image" src="https://github.com/user-attachments/assets/fe942e29-792a-4ea6-b40d-45bfe518bf90" />


