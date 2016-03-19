# API

## Зоны

Список всех зон пользователя

`curl http://api.cloudns.ru/api/zones/ -u <user@email.ru>:<apisecretkey>`

Создание новой зоны

`curl http://api.cloudns.ru/api/zones/ -u <user@email.ru>:<apisecretkey> -X POST -d "&zone=<newdomain.com>"`

Удаление существующей зоны

`curl http://api.cloudns.ru/api/zones/ -u <user@email.ru>:<apisecretkey> -X DELETE -d '&zone_id=<domain_id>'`

