# Event-Driven Architecture

**Этап:** [[00 Обзор этапа|2 — Архитектурные стили]]  
**Время:** ~2 недели

---

## Цель

Проектировать системы на основе событий для loose coupling, масштабируемости и реактивности.

---

## Ключевые концепции

### Event types
- **Domain Event** — факт в бизнесе (OrderPlaced)
- **Integration Event** — для межсервисной коммуникации
- **Event Notification** vs **Event-Carried State Transfer**

### Patterns
- **Event Notification** — минимум данных, consumer запрашивает детали
- **Event-Carried State Transfer** — полное состояние в событии
- **Event Collaboration** — сервисы через chain of events

### Topology
- **Broker** (Kafka, RabbitMQ) — central broker
- **Mediated** vs **Brokerless**

### Guarantees
- At-most-once, at-least-once, exactly-once (и почему exactly-once сложно)
- Ordering guarantees (partition key)
- Idempotent consumers

### EDA + Microservices
- Choreography vs Orchestration
- Event storming для проектирования flows

---

## Материалы

- Ben Stopford — *Designing Event-Driven Systems*
- Confluent — Kafka documentation
- Martin Fowler — «What do you mean by Event-Driven?»

---

## Практика

1. Event flow: OrderPlaced → PaymentProcessed → ShipmentCreated
2. Idempotent consumer с dedup table
3. AsyncAPI spec для event contracts

---

## Критерии освоения

- [ ] Различаю event notification и event-carried state transfer
- [ ] Проектирую idempotent event handler
- [ ] Объясняю choreography vs orchestration trade-offs

---

## Связи

- [[CQRS и Event Sourcing]]
- [[Очереди и брокеры сообщений]]
- [[Enterprise-паттерны]] — Outbox
