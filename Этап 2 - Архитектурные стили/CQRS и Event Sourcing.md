# CQRS и Event Sourcing

**Этап:** [[00 Обзор этапа|2 — Архитектурные стили]]  
**Время:** ~2 недели

---

## Цель

Понимать разделение read/write моделей и хранение состояния как последовательности событий — когда это оправдано, а когда overkill.

---

## Ключевые концепции

### CQRS (Command Query Responsibility Segregation)
- **Commands** — изменяют состояние, без return data (или minimal)
- **Queries** — read-only, оптимизированы под UI
- Separate models для read и write
- Не обязательно separate databases (но часто)

### Event Sourcing
- Состояние = fold всех events
- Event store — append-only log
- Snapshots для performance
- Temporal queries: «состояние на дату X»

### Когда применять
✅ Audit trail критичен  
✅ Complex domain с many state transitions  
✅ Read/write load сильно асимметричны  
❌ Simple CRUD  
❌ Команда без опыта distributed systems  

### Challenges
- Event schema evolution (upcasting)
- Projections и eventual consistency
- Complexity для developers и ops

---

## Материалы

- Greg Young — CQRS Documents
- Martin Fowler — «CQRS», «Event Sourcing»
- *Versioning in an Event Sourced System* — Greg Young

---

## Практика

1. Event-sourced aggregate (BankAccount: Deposited, Withdrawn)
2. Read model projection (balance view)
3. Replay events для rebuild projection

---

## Критерии освоения

- [ ] Объясняю CQRS без «это просто separate DB»
- [ ] Реализовал mini event store + projection
- [ ] Знаю, когда ES — over-engineering

---

## Связи

- [[Event-Driven Architecture]]
- [[../Этап 0 - Фундамент/Основы DDD|Основы DDD]]
- [[CAP и согласованность]]
