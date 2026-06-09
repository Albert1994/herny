# Основы DDD

**Этап:** [[00 Обзор этапа|0 — Фундамент]]  
**Время:** ~2 недели

---

## Цель

Моделировать программную систему в терминах предметной области, а не только таблиц и REST endpoints.

---

## Ключевые концепции

### Стратегический DDD
- **Ubiquitous Language** — единый язык команды и кода
- **Bounded Context** — граница модели и команды
- **Context Map** — отношения между контекстами (Shared Kernel, ACL, Customer-Supplier)
- **Subdomain** — core, supporting, generic

### Тактический DDD
- **Entity** vs **Value Object**
- **Aggregate** и **Aggregate Root** — граница транзакционной согласованности
- **Domain Event** — факт, произошедший в домене
- **Repository** — коллекция агрегатов
- **Domain Service** — логика, не принадлежащая одной entity

### Анemic Domain Model — антипаттерн
Логика в сервисах, entity — только getters/setters. Признак и способ исправления.

---

## Материалы

- Eric Evans — *Domain-Driven Design* (Part I–III для старта)
- Vlad Khil — «Domain-Driven Design Distilled»
- Martin Fowler — bliki: BoundedContext, UbiquitousLanguage

---

## Практика

1. Event Storming для процесса «оформление заказа» (sticky notes)
2. Выделить 2–3 bounded context из своего проекта
3. Оформить aggregate с инвариантами (например, Order нельзя оплатить дважды)

---

## Критерии освоения

- [ ] Различаю entity, value object, aggregate
- [ ] Могу нарисовать context map для знакомой системы
- [ ] В проекте этапа доменная логика живёт в domain layer, не в controllers

---

## Связи

- [[ООП и SOLID]]
- [[CQRS и Event Sourcing]]
- [[Микросервисы]] — один сервис ≈ один bounded context (часто)
