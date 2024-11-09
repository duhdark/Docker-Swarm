# Установка и настройка Traefik #

Traefik — это мощный и гибкий обратный прокси и балансировщик нагрузки, который легко интегрируется с Docker. Следуйте инструкциям ниже для установки и настройки Traefik в вашем Docker Swarm кластере

### Команды для управления Traefik ###

* Запуск Traefik
```
docker stack deploy -c docker-compose.yml traefik
```
* Перезапуск Traefik
```
docker service update --force traefik_traefik

```
* Просмотр логов Traefik
```
docker service logs -f traefik_traefik
```
* Удаление стека Traefik
```
docker stack rm traefik
```
* Адрес Traefik
```
master ansible_host=x.x.x.x:8080
```