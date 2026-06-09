# Слоистая и Clean Architecture

**Этап:** [[00 Обзор этапа|2 — Архитектурные стили]]  
**Время:** ~2 недели

---

## Цель

Организовать код в слои с правилом зависимостей: бизнес-логика не зависит от фреймворков и инфраструктуры.

---

## Ключевые концепции

### Классическая слоистая архитектура
```
Presentation → Business Logic → Data Access → Database
```
Проблема: бизнес-логика часто «просачивается» в UI или SQL.

### Clean Architecture (Uncle Bob)
Кольца (от центра наружу):
1. **Entities** — enterprise business rules
2. **Use Cases** — application business rules
3. **Interface Adapters** — controllers, presenters, gateways
4. **Frameworks & Drivers** — DB, web, UI

**Dependency Rule:** зависимости только внутрь. Внутренние слои не знают о внешних.

### Use Case Driven
- Interactor (use case) orchestrates flow
- Input/Output boundaries (DTOs)
- Тестируемость: use cases без HTTP и DB

---

## Материалы

- Robert Martin — *Clean Architecture*
- Herberto Graca — «DDD, Hexagonal, Onion, Clean, CQRS» (blog)
- Jason Taylor — Clean Architecture template (.NET)

---

## Практика

1. Реструктурировать проект этапа 0 по слоям Clean Architecture
2. Написать use case test без mock HTTP
3. C4 Component diagram для одного bounded context

---

## Критерии освоения

- [ ] Могу нарисовать Clean Architecture и объяснить Dependency Rule
- [ ] Domain layer не импортирует ORM/framework
- [ ] Use case покрыт unit-тестами

---

## Связи

- [[Hexagonal и Onion]]
- [[../Этап 1 - Проектирование ПО/Модульность и связность|Модульность]]
- [[Монолит и модульный монолит]]
