# AI English Tutor Bot

Телеграм бот для обучения английскому с использованием LLM технологий.

## Требования

- Docker и Docker Compose
- Python 3.8+
- Telegram Bot Token
- OpenAI API Key

## Установка и запуск

1. Клонируйте репозиторий:
```bash
git clone <repository-url>
cd llm-course-bot
```

2. Создайте файл `.env` в корневой директории проекта:
```env
BOT_TOKEN=your_bot_token_here
OPENAI_API_KEY=your_openai_api_key_here
MONGODB_URI=mongodb://llm:llm_mongo_pass@mongodb/?retryWrites=true&w=majority
MONGODB_NAME=llm_db
```

3. Создайте файл `.env.docker` в корневой директории:
```env
TG_BOT_NAME=llm_course_bot
MONGO_LOGIN=llm
MONGO_PSWD=llm_mongo_pass
DB_NAME=llm_db
MONGO_EXPRESS_LOGIN=admin
MONGO_EXPRESS_PSWD=admin_pass
```

4. Запустите проект:
```bash
docker-compose up --build
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


