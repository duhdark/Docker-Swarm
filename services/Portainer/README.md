# Установка и настройка Portainer #

Portainer — это инструмент с открытым исходным кодом для управления контейнерами, который предоставляет удобный графический интерфейс для администрирования Docker, Docker Swarm, Kubernetes и других контейнерных платформ. Portainer значительно упрощает управление контейнеризованными приложениями и кластерами, облегчая взаимодействие с контейнерами и инвентарем для разработчиков и системных администраторов.

### Команды для управления Portainer ###

* Запуск Portainer
```
docker stack deploy -c docker-compose.yml portainer
```
* Перезапуск Portainer
```
docker service update --force portainer_portainer

```
* Просмотр логов Portainer
```
docker service logs -f portainer_portainer
```
* Удаление стека Portainer
```
docker stack rm portainer
```
* Адрес Portainer
```
master ansible_host=x.x.x.x:9000
```