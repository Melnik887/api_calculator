
# API Калькулятор

Простой API-калькулятор, разработанный с использованием **FastAPI** и **Docker**. Позволяет выполнять базовые арифметические операции: сложение, вычитание, умножение и деление.

## Запуск с помощью Docker

### Шаг 1: Сборка Docker-образа

Перейдите в корневую папку проекта и выполните команду:

```bash
docker build -t api_calculator .
```

### Шаг 2: Запуск Docker-контейнера

После успешной сборки образа запустите контейнер:

```bash
docker run -d -p 8000:8000 api_calculator
```

## Использование API

Откройте браузер и перейдите по адресу [http://localhost:8000/docs](http://localhost:8000/docs) для доступа к интерактивной документации API, созданной с помощью Swagger UI.

### Пример запроса

**POST /calculate**

```json
{
  "operation": "add",
  "operands": [1, 2, 3]
}
```

**Ответ:**

```json
{
  "result": 6
}
```

## Требования

- [Docker](https://www.docker.com/get-started) установлен на вашем компьютере.

## Структура Проекта

```
api_calculator/
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── app/
│   ├── main.py
│   └── requirements.txt
├── .dockerignore
├── Dockerfile
└── README.md
```

