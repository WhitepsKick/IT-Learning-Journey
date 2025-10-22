## 🏗️ Этап 2: Инфраструктура и виртуализация (Недели 5-9)

### Неделя 5: Сети: DNS, DHCP, NAT

**🎯 Цель:** Понять основы сетевых технологий и их настройку

**📖 Что изучать:**

#### DNS
- Иерархия доменов, типы записей (A, AAAA, CNAME, MX)
- Рекурсивные и авторитативные серверы
- Утилиты: `nslookup`, `dig`, `host`

#### DHCP
- Процесс DORA (Discover, Offer, Request, Acknowledge)
- Аренда адресов, резервирования

#### NAT
- PAT (NAT overload), SNAT, DNAT
- Проброс портов

**🛠️ Практика:**
1. ✅ Настройте статический IP на вашей VM
2. ✅ Установите и настройте `dnsmasq` как кэширующий DNS и DHCP-сервер для внутренней сети VirtualBox
3. ✅ Разберите таблицу маршрутизации (`route -n`)

**🔗 Полезные ресурсы:**
- [DNS for Rocket Scientists](http://www.zytrax.com/books/dns/)
- [DHCP Protocol](https://tools.ietf.org/html/rfc2131)

---

### Неделя 6: Active Directory

**🎯 Цель:** Освоить основы доменной инфраструктуры Windows

**📖 Что изучать:**

#### Основы
- Что такое домен, лес, дерево
- Роли: Domain Controller, Member Server
- Объекты: пользователи, группы, компьютеры, OU

#### Практическое администрирование
- Создание пользователей и групп
- Групповые политики (GPO): порядок применения
- Делегирование прав

**🛠️ Практика:**
1. ✅ Установите Windows Server в VirtualBox
2. ✅ Поднимите домен `lab.local`
3. ✅ Добавьте Windows 10 в домен
4. ✅ Создайте OU "Отдел IT", пользователей, примените GPO с ограничениями

**🔗 Полезные ресурсы:**
- [Microsoft AD Documentation](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview)
- [GPO Guide](https://adsecurity.org/?p=2716)

---

### Неделя 7: Docker - Основы

**🎯 Цель:** Освоить контейнеризацию приложений с Docker

**📖 Что изучать:**

#### Концепции
- Образы vs контейнеры
- Docker Hub, Dockerfile
- Тома (volumes), сети

#### Команды
- `docker run`, `ps`, `stop`, `rm`, `images`, `rmi`
- `docker exec`, `logs`, `inspect`
- Сборка образа: `docker build -t <name> .`

**🛠️ Практика:**
1. ✅ Установите Docker Engine
2. ✅ Запустите контейнеры: `nginx`, `redis`, `postgres`
3. ✅ Напишите Dockerfile для вашего Python-API приложения
4. ✅ Соберите образ и запустите контейнер

**🔗 Полезные ресурсы:**
- [Docker Get Started](https://docs.docker.com/get-started/)
- [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)

---

### Неделя 8: Docker - Compose & Практика

**🎯 Цель:** Научиться управлять многоконтейнерными приложениями

**📖 Что изучать:**

#### Docker Compose
- Структура `docker-compose.yml`
- Секции: `services`, `networks`, `volumes`
- Переменные окружения, зависимости

#### Сети в Docker
- Bridge, host, none сети
- Связывание контейнеров

**🛠️ Практика:**
1. ✅ Создайте `docker-compose.yml` для вашего приложения + PostgreSQL
2. ✅ Настройте том для persistence данных БД
3. ✅ Настройте сеть и переменные окружения для подключения приложения к БД
4. ✅ Запустите стек командой `docker-compose up -d`

**🔗 Полезные ресурсы:**
- [Docker Compose Guide](https://docs.docker.com/compose/gettingstarted/)
- [Docker Networking](https://docs.docker.com/network/)

---

### Неделя 9: Введение в Kubernetes

**🎯 Цель:** Понять основы оркестрации контейнеров

**📖 Что изучать:**

#### Основные понятия
- Pod, Deployment, Service, Namespace
- Architecture: Control Plane (API Server, etcd, Scheduler), Worker Nodes (kubelet, kube-proxy)
- `kubectl`: основной CLI-инструмент

#### Манифесты
- Структура YAML-файлов
- `spec`, `selector`, `template`, `ports`

**🛠️ Практика:**
1. ✅ Установите Minikube или используйте Play with Kubernetes
2. ✅ Пройдите официальный интерактивный туториал
3. ✅ Напишите YAML-манифест для деплоя вашего приложения
4. ✅ Разверните его командой `kubectl apply -f deployment.yaml`

**🔗 Полезные ресурсы:**
- [Kubernetes Basics Tutorial](https://kubernetes.io/ru/docs/tutorials/kubernetes-basics/)
- [kubectl Cheat Sheet](https://kubernetes.io/ru/docs/reference/kubectl/cheatsheet/)
