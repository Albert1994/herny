# Hexagonal и Onion

**Этап:** [[00 Обзор этапа|2 — Архитектурные стили]]  
**Время:** ~1 неделя

---

## Цель

Понимать Ports & Adapters — архитектуру, где домен в центре, а все внешние системы подключаются через порты.

---

## Ключевые концепции

### Hexagonal Architecture (Alistair Cockburn)
- **Ports** — интерфейсы (inbound: API, CLI; outbound: DB, messaging)
- **Adapters** — реализации портов (REST controller, PostgreSQL repo)
- Домен не знает, REST это или gRPC, PostgreSQL или MongoDB

### Onion Architecture (Jeffrey Palermo)
Слои как кольца лука:
- Domain Model (center)
- Domain Services
- Application Services
- Infrastructure

Похоже на Clean Architecture — разные авторы, общая идея.

### Primary vs Secondary Adapters
| Тип | Примеры |
|-----|---------|
| Primary (driving) | REST API, GraphQL, CLI, message consumer |
| Secondary (driven) | Repository, email sender, payment gateway |

### Testing benefit
- In-memory adapters для integration tests
- Mock secondary ports для unit tests

---

## Материалы

- Alistair Cockburn — «Hexagonal Architecture» (original article)
- Tom Hombergs — *Get Your Hands Dirty on Clean Architecture*

---

## Практика

1. Выделить ports для persistence и notifications
2. Swap PostgreSQL adapter на in-memory для tests
3. Diagram: hexagon с 4+ adapters

---

## Критерии освоения

- [ ] Различаю port и adapter
- [ ] Могу добавить новый adapter (e.g. CLI) без изменения domain
- [ ] Объясняю связь Hexagonal ↔ Clean ↔ DDD

---

## Связи

- [[Слоистая и Clean Architecture]]
- [[../Этап 0 - Фундамент/Основы DDD|Основы DDD]]
- [[Enterprise-паттерны]]
