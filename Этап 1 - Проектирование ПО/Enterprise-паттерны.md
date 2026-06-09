# Enterprise-паттерны

**Этап:** [[00 Обзор этапа|1 — Проектирование ПО]]  
**Время:** ~2 недели

---

## Цель

Понимать паттерны уровня приложения и интеграции — мост между OOP-паттернами и архитектурой.

---

## Ключевые концепции

### Martin Fowler — Patterns of Enterprise Application Architecture
- **Repository** — абстракция persistence
- **Unit of Work** — атомарность изменений
- **Identity Map** — кэш объектов в рамках сессии
- **Data Mapper** vs **Active Record**
- **Domain Model** vs **Transaction Script**
- **Service Layer** — координация use cases
- **Table Data Gateway** / **Row Data Gateway**

### Интеграционные
- **Gateway** — изоляция внешнего API
- **Anti-Corruption Layer (ACL)** — защита домена от legacy
- **Outbox Pattern** — надёжная публикация событий
- **Saga** — распределённые транзакции (орchestration vs choreography)
- **Idempotency Key** — безопасные повторы

### CQRS (введение)
Разделение моделей чтения и записи — подробнее в [[../Этап 2 - Архитектурные стили/CQRS и Event Sourcing|CQRS и Event Sourcing]].

---

## Материалы

- Martin Fowler — *Patterns of Enterprise Application Architecture*
- microservices.io — Outbox, Saga patterns
- Chris Richardson — *Microservices Patterns*

---

## Практика

1. Реализовать Repository + Unit of Work для своего агрегата
2. Gateway для внешнего payment API с ACL
3. Outbox table + background publisher

---

## Критерии освоения

- [ ] Объясняю Data Mapper vs Active Record trade-offs
- [ ] Могу спроектировать Saga для заказа с 3 сервисами
- [ ] Реализовал Outbox или Idempotency Key

---

## Связи

- [[../Этап 0 - Фундамент/Основы DDD|Основы DDD]]
- [[Интеграционные паттерны]]
- [[Микросервисы]]
