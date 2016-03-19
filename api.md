# API

## Зоны

Список всех зон пользователя

`curl http://api.cloudns.ru/api/zones/ -u <user@email.ru>:<apisecretkey>`

Создание новой зоны

`curl http://api.cloudns.ru/api/zones/ -u <user@email.ru>:<apisecretkey> -X POST -d "&zone=<newdomain.com>"`

Удаление существующей зоны

`curl http://api.cloudns.ru/api/zones/ -u <user@email.ru>:<apisecretkey> -X DELETE -d '&zone_id=<domain_id>'`

## Записи

Список всех записей в зоне

`curl http://api.cloudns.ru/api/zones/<zone_id>/records/?layer=default -u <user@email.ru>:<apisecretkey>`

Создание новой саписи

`curl http://api.cloudns.ru/api/zones/<zone_id>/records/?layer=default -u <user@email.ru>:<apisecretkey> -X POST -d '&layer=default&name=test&ttl=7200&type=MX&data=1.2.3.4&priority=0'`

Удаление существующей записи

`curl http://api.cloudns.ru/api/zones/<zone_id>/records/?layer=default -u <user@email.ru>:<apisecretkey> -X DELETE -d '&layer=default&record_id=4'`

Изменение существующей записи

`curl http://api.cloudns.ru/api/zones/<zone_id>/records/?layer=default -u <user@email.ru>:<apisecretkey> -X PUT -d '&layer=default&record_id=8&ttl=7200type=MX&data=1.2.3.4&priority=1'`
