# KnowledgeNexus

KnowledgeNexus — цифровой ассистент для работы с базами знаний, объединяющий различные источники информации в единую, модульную платформу.

Проект разработан за 48 часов

## Основной функционал

- **Создание баз знаний:** Лёгкое создание и управление информационными ресурсами.
- **Кастомизация интерфейса чата:** Гибкая настройка внешнего вида и функционала для комфортного взаимодействия.
- **Генерация ответов:** Алгоритмы для формирования релевантных ответов на основе загруженных данных.
- **Поддержка мультимедиа и СУБД:** Интеграция документов, аудио, изображений и баз данных.
- **Распознавание текста (OCR):** Автоматическое извлечение текста из изображений.
- **Текстовое описание аудио (CLAP):** Преобразование аудиофайлов в текстовые описания.
- **Текстовое описание изображения (CLIP):** Генерация текстовых описаний по содержимому изображений.

# Интерфейс

## Управление базами знаний

![1](https://github.com/user-attachments/assets/c197c28f-cb2f-40a9-b332-94232a9a9460)


## Кастомизация чата

![2](https://github.com/user-attachments/assets/9b2990e8-e78c-40a8-905e-9d209a5111e4)


## Создание базы знаний

![3](https://github.com/user-attachments/assets/e85040d5-e52a-4ff8-9ed3-1905f4df9463)


### Архитектура проекта 

<img width="440" height="420" alt="image" src="https://github.com/user-attachments/assets/c4a5d851-dc2e-4eca-9a24-ba479f82fe7d" />



# Сборка фронта
```
cd orvim-frontend
yarn install && yarn build
mkdir ../nginx/public
mv dist/* chat-widget/ ../nginx/public
```

# Развертывание
```
cp .env.example .env
docker network create orvim
docker compose up -d --build
```

## Модели
Для развертывания моделей:
```
cd orvim-models
```
### CPU версия
```
docker compose -f docker-compose.cpu.yaml up -d --build
```
### GPU версия
```
docker compose -f docker-compose.gpu.yaml up -d --build
```
