# Установка и настройка TeamCity #

TeamCity — это мощный сервер непрерывной интеграции и развертывания (CI/CD), разработанный компанией JetBrains. Он позволяет автоматизировать процессы сборки, тестирования и деплоя программного обеспечения, обеспечивая стабильное и быстрое развертывание приложений. TeamCity поддерживает множество платформ и языков программирования и хорошо интегрируется с другими инструментами разработки.

### Команды для управления TeamCity ###

* Запуск TeamCity
```
docker stack deploy -c docker-compose.yml teamcity
```
* Копирование mysql connector
```
docker cp mysql-connector-j-9.0.0.jar $(docker ps -q -f name=teamcity_teamcity-server):/data/teamcity_server/datadir/lib/jdbc
```
* Копирование бекапа
```
docker cp TeamCity_Backup_20240818_173946.zip $(docker ps -q -f name=teamcity_teamcity-server):/data/teamcity_server/datadir
```
* Перезапуск TeamCity
```
docker service update --force teamcity_teamcity

```
* Просмотр логов TeamCity
```
docker service logs -f teamcity_teamcity
```
* Удаление стека TeamCity
```
docker stack rm teamcity
```
* Адрес TeamCity
```
master ansible_host=x.x.x.x:8111
```