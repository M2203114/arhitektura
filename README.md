# arhitektura

## Описание проекта
Проект представляет собой микросервисную архитектуру, реализованную с использованием Spring Boot и Axon Framework. Система состоит из нескольких сервисов, каждый из которых отвечает за свою функциональность.

### Сервисы
1. **User Service** - управление пользователями
2. **Balance Service** - управление балансом
3. **Notification Service** - отправка уведомлений
4. **Shared Contract** - общие контракты и модели

### Технологии
- Java 17
- Spring Boot
- Axon Framework
- PostgreSQL
- Docker
- Maven

### Запуск проекта
1. Убедитесь, что у вас установлены:
   - Java 17
   - Maven
   - Docker и Docker Compose

2. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/M2203114/arhitektura.git
   ```

3. Перейдите в директорию проекта:
   ```bash
   cd arhitektura
   ```

4. Запустите все сервисы с помощью Docker Compose:
   ```bash
   docker-compose up
   ```

### API Endpoints

#### User Service
- POST /api/users - создание пользователя
- GET /api/users/{id} - получение информации о пользователе

#### Balance Service
- POST /api/balance - создание баланса
- PUT /api/balance/{id}/credit - пополнение баланса
- PUT /api/balance/{id}/debit - списание с баланса
- GET /api/balance/{id} - получение информации о балансе

#### Notification Service
- POST /api/notifications - отправка уведомления
- GET /api/notifications/{userId} - получение уведомлений пользователя

### Архитектура
Проект построен на принципах Event-Driven Architecture с использованием CQRS (Command Query Responsibility Segregation) и Event Sourcing. Каждый сервис является независимым и может быть развернут отдельно.

### Лицензия
MIT
