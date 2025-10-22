## 📊 Этап 3: Мониторинг, CI/CD и облака (Недели 10-14)

### Неделя 10: ELK-Стек для логов

**🎯 Цель:** Настроить централизованный сбор и анализ логов

**📖 Что изучать:**

#### Elasticsearch
- Индексы, документы, шарды, реплики
- API для работы с данными

#### Logstash
- Конфигурационные файлы: input, filter, output
- Плагины: grok, mutate, date

#### Kibana
- Index Patterns, Discover, Visualize, Dashboard
- KQL (Kibana Query Language)

**🛠️ Практика:**
1. ✅ Разверните ELK-стек через Docker Compose
2. ✅ Настройте Filebeat для сбора логов Nginx
3. ✅ Создайте Grop-паттерн для парсинга логов
4. ✅ Постройте дашборд в Kibana с графиками по кодам ответа

**🔗 Полезные ресурсы:**
- [ELK Stack Guide](https://www.elastic.co/guide/index.html)
- [Grok Debugger](https://grokdebug.herokuapp.com/)

---

### Неделя 11: Мониторинг: Prometheus + Grafana

**🎯 Цель:** Настроить сбор метрик и визуализацию

**📖 Что изучать:**

#### Prometheus
- Data model: метрики, labels, time series
- Pull-модель сбора метрик
- Exporters: Node Exporter, cAdvisor

#### Grafana
- Data Sources, Dashboards, Panels
- Query editors: PromQL basics
- Alerting

**🛠️ Практика:**
1. ✅ Разверните стек через Docker Compose: Prometheus + Grafana + Node Exporter
2. ✅ Настройте сбор метрик с вашей VM
3. ✅ Создайте дашборд в Grafana с метриками: CPU, Memory, Disk I/O, Network
4. ✅ Настройте простой алерт на высокую загрузку CPU

**🔗 Полезные ресурсы:**
- [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/)
- [Grafana Tutorials](https://grafana.com/tutorials/)

---

### Неделя 12: CI/CD: GitHub Actions

**🎯 Цель:** Настроить автоматическую сборку и тестирование кода

**📖 Что изучать:**

#### Основы GitHub Actions
- Workflow, jobs, steps
- Events: `push`, `pull_request`
- Runners, `runs-on`

#### Синтаксис YAML
- `name`, `on`, `jobs`, `uses`, `run`
- Работа с секретами (`secrets`)
- Кэширование зависимостей

**🛠️ Практика:**
1. ✅ Создайте workflow-файл в `.github/workflows/ci.yml`
2. ✅ Настройте запуск линтера (`flake8`) при каждом пуше
3. ✅ Добавьте шаг сборки Docker-образа и пуша в GitHub Container Registry
4. ✅ Настройте запуск unit-тестов (если они есть)

**🔗 Полезные ресурсы:**
- [GitHub Actions Docs](https://docs.github.com/en/actions)
- [Awesome Actions](https://github.com/sdras/awesome-actions)

---

### Неделя 13: Облачные платформы (Yandex Cloud)

**🎯 Цель:** Освоить основы работы с облачной инфраструктурой

**📖 Что изучать:**

#### Основные сервисы
- Compute Cloud (ВМ)
- Object Storage (аналог S3)
- Managed Service for PostgreSQL
- VPC, сети, балансировщики

#### Безопасность
- IAM, сервисные аккаунты, ключи
- Группы безопасности

**🛠️ Практика:**
1. ✅ Зарегистрируйтесь в Yandex Cloud, активируйте грант
2. ✅ Создайте ВМ, настройте SSH-доступ
3. ✅ Установите Docker на ВМ и запустите ваше приложение
4. ✅ Создайте бакет в Object Storage, загрузите туда файл через CLI

**🔗 Полезные ресурсы:**
- [Yandex Cloud Documentation](https://cloud.yandex.ru/docs/)
- [YC CLI](https://cloud.yandex.ru/docs/cli/)

---

### Неделя 14: Интеграционный проект

**🎯 Цель:** Связать все изученные технологии в одном проекте

**📖 Что изучать:**

#### Связывание технологий
- Автоматический деплой при коммите
- Мониторинг развернутого приложения
- Резервирование конфигурации

**🛠️ Практика:**
1. ✅ Настройте GitHub Actions для деплоя на Yandex Cloud ВМ:
   - На VM при пуше в main ветку
   - Обновляется код, перезапускаются контейнеры
2. ✅ Настройте сбор логов и метрик с развернутого приложения

**🔗 Полезные ресурсы:**
- [Infrastructure as Code](https://www.terraform.io/docs)
- [DevOps Roadmap](https://roadmap.sh/devops)
