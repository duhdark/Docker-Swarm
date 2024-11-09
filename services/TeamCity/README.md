# Установка и настройка TeamCity #

TeamCity — это мощный сервер непрерывной интеграции и развертывания (CI/CD), разработанный компанией JetBrains. Он позволяет автоматизировать процессы сборки, тестирования и деплоя программного обеспечения, обеспечивая стабильное и быстрое развертывание приложений. TeamCity поддерживает множество платформ и языков программирования и хорошо интегрируется с другими инструментами разработки.

### Команды для управления TeamCity ###

* Запуск TeamCity
```
docker stack deploy -c docker-compose.yml teamcity # После создания контейнера и если планируется использовать MySQL, необходимо внутри контейнера в директорию lib/jdbc положить mysql-connector-j-9.0.0.jar и перезапустить контейнер
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