# Machinery Factory Compose Project

### Краткая ифнормация

Копируем конфиг из .env.dist в .env файл

#### Сборка
```bash
docker-compose build
```

#### Поднятие контейнеров
```bash
docker-compose up -d
```

#### Зайти в контейнер
```bash
docker-compose exec machinery-factory sh
```

#### Приглушить контейнеры
```bash
docker-compose down
```

## Настройка окружения для удобной разработки

#### Настройка DOCKER
Чтобы docker не запускать через sudo надо добавить пользователя в группу docker 
```
sudo gpasswd -a $USER docker && sudo usermod -aG docker $USER
```
После перезагружаем машину

#### Настройка PHP-STORM
1. Настраиваем, чтобы IDE читала PHP из docker-compose контейнера
2. Настравам маппинг xdebug