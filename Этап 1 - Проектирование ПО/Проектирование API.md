# Проектирование API

**Этап:** [[00 Обзор этапа|1 — Проектирование ПО]]  
**Время:** ~2 недели

---

## Цель

Проектировать контракты между системами — REST, GraphQL, gRPC, события — с учётом версионирования и обратной совместимости.

---

## Ключевые концепции

### REST API Design
- Resources, HTTP verbs, status codes
- HATEOAS (когда нужен, когда overkill)
- Pagination: offset vs cursor
- Filtering, sorting, field selection
- Idempotency: PUT, DELETE, POST with key
- Error format (RFC 7807 Problem Details)

### GraphQL
- Schema, queries, mutations, subscriptions
- N+1 problem и DataLoader
- Когда GraphQL vs REST

### gRPC / Protocol Buffers
- Strongly typed contracts
- Streaming (unary, server, client, bidirectional)
- Когда gRPC: internal service-to-service

### Общие практики
- **Versioning**: URL (/v1/) vs header vs content negotiation
- **Backward compatibility** — additive changes only
- **Rate limiting**, **API keys**, **OAuth 2.0 / OIDC**
- OpenAPI / AsyncAPI specification
- Contract-first vs code-first

---

## Материалы

- *RESTful Web APIs* — Richardson & Amundsen
- Google API Design Guide
- graphql.org — best practices
- gRPC documentation

---

## Практика

1. OpenAPI spec для CRUD API из этапа 0
2. Реализовать cursor-based pagination
3. Сравнить один use case в REST vs gRPC (latency, DX)

---

## Критерии освоения

- [ ] Проектирую REST API без «RPC через POST»
- [ ] Знаю правила backward-compatible изменений
- [ ] Выбираю REST/GraphQL/gRPC с обоснованием

---

## Связи

- [[../Этап 0 - Фундамент/Сети и протоколы|Сети и протоколы]]
- [[Микросервисы]]
- [[Интеграционные паттерны]]
