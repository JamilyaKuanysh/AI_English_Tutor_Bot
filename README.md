# AI English Tutor Bot

Телеграм бот для обучения английскому с использованием LLM технологий.

Пример запущенного проекта https://t.me/Speakadora_bot

# С использованием Docker (рекомендуется)

# Добавьте нужные ключи и токены в config.yaml 

```
# Клонирование проекта
git clone https://github.com/a-milenkin/LLM_course_project.git
cd LLM_course_project

# Запуск сборки
sudo docker compose up -d --build``

# Запуск после сборки
docker compose start

# Просмотр логов
docker ps -a 
docker logs -f контейнер_id

# Выключение
docker compose stop

# Перезапуск без сборки
docker compose restart
```

# Запуск вне Docker контейнера


```
Клонирование проекта
git clone https://github.com/a-milenkin/LLM_course_project.git
cd LLM_course_project

Установка зависимостей
python3 -m pip install  -U --no-cache-dir -r requirements.txt -c constraints.txt

Запуск проекта
python3 /src/utils/main.py
```

## Структура проекта

```
.
├── src/
│   ├── assets/         # Статические файлы
│   ├── dao/           # Data Access Objects
│   ├── managers/      # Бизнес-логика
│   ├── models/        # Модели данных
│   ├── routes/        # Обработчики маршрутов
│   ├── utils/         # Вспомогательные функции
│   ├── main.py        # Основной файл приложения
│   └── settings.py    # Настройки приложения
├── config.yaml        # Конфигурация приложения
├── docker-compose.yaml # Docker конфигурация
└── requirements.txt   # Зависимости Python
```

## Доступ к сервисам

- Telegram Bot: Доступен через Telegram
- MongoDB: localhost:27017
- Mongo Express: http://localhost:8034

## Разработка

1. Установите зависимости Python:
```bash
pip install -r requirements.txt
```

2. Запустите приложение локально:
```bash
python src/main.py
```

## Функциональность

- Обучение языкам через диалоги
- Генерация текстов на разных языках
- Обработка голосовых сообщений
- Система рейтинга пользователей
- Подсказки и помощь в обучении


