Swagger Petstore - OpenAPI 3.0. Локальная сборка.

## Требования

- Docker-контейнер `swaggerapi/petstore3` с опубликованным портом:  
    `docker run -d -p 8080:8080 --name petstore3 swaggerapi/petstore3`
    
- Переменная окружения `baseUrl` = `http://localhost:8080/api/v3`  
    (без запущенного контейнера прогон упадёт на всех запросах)
    
- База данных in-memory: для воспроизводимого прогона её нужно сбрасывать - `docker restart petstore3`
    

## Структура

1. `user` - создание -> логин -> чтение -> обновление -> удаление -> логаут
    
2. `pet` - добавление -> обновление (файл/форма) -> поиск -> удаление
    
3. `store` - оформление заказа -> чтение -> удаление -> остатки
    
4. `inventory` - состояние заказов
    
5. `negative` - негативные сценарии по ресурсам (`negative/user`, `negative/pet`, `negative/store`)
