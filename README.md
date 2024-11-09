# Docker-Swarm
**Развертывание Docker Swarm с помощью Ansible**

Этот репозиторий содержит Ansible playbook'и для настройки кластера Docker Swarm. Настройка включает установку Docker на всех узлах, инициализацию Swarm на мастер-узле и подключение рабочих узлов к Swarm.

---

## Структура репозитория

- **swarm-bootstrap.yml** - основной playbook для развертывания кластера Docker Swarm.
- **install_docker.yml** - playbook для установки Docker и Docker Compose на всех узлах.
- **docker-swarm_init_master.yml** - playbook для инициализации Docker Swarm на мастер-узле.
- **docker-swarm_init_worcker.yml** - playbook для получения команды присоединения от мастер-узла и подключения рабочих узлов к Swarm.
- **hosts** - инвентори-файл, содержащий мастер- и рабочие узлы.

---

## Инвентори-файл

**hosts**
```
[masters]
master ansible_host=x.x.x.x

[workers]
node-1 ansible_host=x.x.x.x
node-2 ansible_host=x.x.x.x

[all:vars]
ansible_python_interpreter=/usr/bin/python3
```

---

## Запуск

Для запуска playbook'ов используйте следующую команду:
```
ansible-playbook -i hosts swarm-bootstrap.yml
```
Этот репозиторий автоматически установит Docker, инициализирует кластер Docker Swarm на мастер-узле и присоединит рабочие узлы к кластеру.
---