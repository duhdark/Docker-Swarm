# Установка и настройка Selenium  #

Selenium — это популярный инструмент для автоматизации веб-браузеров, широко используемый для тестирования веб-приложений. С его помощью можно создавать скрипты, имитирующие действия пользователя на веб-сайтах, такие как клики, ввод текста, навигация по страницам и обработка динамического контента. Selenium поддерживает множество языков программирования, включая Python, Java, JavaScript, C#, и может работать с разными браузерами, такими как Chrome, Firefox, Safari и Edge.

### Команды для управления Selenium  ###

* Запуск Selenium 
```
docker stack deploy -c docker-compose.yml selenium-hub
```
* Перезапуск Selenium 
```
docker service update --force selenium-hub_selenium-hub

```
* Просмотр логов Selenium 
```
docker service logs -f selenium-hub_selenium-hub
```
* Удаление стека Selenium 
```
docker stack rm selenium-hub
```
* Адрес Selenium 
```
master ansible_host=x.x.x.x:4444
```