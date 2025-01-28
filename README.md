# GitHub Repository Scraper

Проект предназначен для сбора данных о репозиториях с GitHub и их сохранения в базу данных ClickHouse. Система использует API GitHub для получения информации о популярных репозиториях и коммитах, а также ClickHouse для хранения и обработки данных.

## 🚀 Возможности

- Сбор информации о популярных репозиториях с GitHub.
- Сохранение данных о репозиториях и статистике коммитов в ClickHouse.
- Логирование всех операций.
- Архитектура построена с использованием принципов слоистой архитектуры, что обеспечивает простоту масштабирования и тестирования.

## 🛠️ Технологии

- **Python 3.12+** для разработки.
- **FastAPI** для создания REST API.
- **GitHub API** для получения информации о репозиториях.
- **ClickHouse** для хранения и анализа данных.
- **aiohttp** для асинхронных HTTP-запросов.
- **punq** для внедрения зависимостей.
- **docker-compose** для контейнеризации.
- **Makefile** для управления сборкой и запуском.

## ⚙️ Установка

Для установки и запуска проекта выполните следующие шаги:

1. Клонируйте репозиторий:
    ```bash
    git clone https://github.com/yourusername/github-api-client.git
    cd github-api-client
    ```

2. Создайте и активируйте виртуальное окружение:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # Для Linux/MacOS
    venv\Scripts\activate  # Для Windows
    ```

3. Установите зависимости:
    ```bash
    pip install -r requirements.txt
    ```

4. Настройте файл конфигурации `.env`:
    ```bash
    cp .env.example .env
    ```

    В файле `.env` укажите:
    - Ваш GitHub токен (для доступа к GitHub API).
    - Данные для подключения к ClickHouse базе данных.

5. **Сборка и запуск через Docker**:
    Проект использует `Makefile` для автоматизации сборки и запуска через Docker.

    Для сборки и запуска используйте следующие команды:

    - Для сборки Docker-образа:
      ```bash
      make
      ```

    - Для запуска контейнеров:
      ```bash
      make drop
      ```

    - Для очистка контейнеров:
      ```bash
      make clean
      ```

## 🧪 Тестирование

Проект включает в себя юнит-тесты и интеграционные тесты. Для их выполнения используйте команду:

```bash
pytest
```