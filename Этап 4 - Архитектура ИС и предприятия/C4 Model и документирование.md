# C4 Model и документирование

**Этап:** [[00 Обзор этапа|4 — Архитектура ИС и предприятия]]  
**Время:** ~1 неделя

---

## Цель

Документировать архитектуру на разных уровнях абстракции для разных аудиторий — от CTO до разработчика.

---

## Ключевые концепции

### C4 Model (Simon Brown)
1. **Context** — system in the world (users, external systems)
2. **Container** — apps, databases, message brokers
3. **Component** — modules inside container
4. **Code** — classes (optional, auto-generated)

### Diagram rules
- Одна diagram — один level of abstraction
- Названия понятны бизнесу (не «PostgreSQL v15», а «User Database»)
- Легенда, ключ, дата, автор
- Diagrams as code: Structurizr DSL, PlantUML, Mermaid

### Дополнительные views
- **Deployment diagram** — infrastructure mapping
- **Dynamic diagram** — sequence of interactions
- **System Landscape** — all systems in org

### Documentation beyond diagrams
- Architecture README
- Getting started guide
- Decision log (ADR)
- Runbooks

### Anti-patterns
- Single «architecture diagram» со всем сразу
- UML class diagram как единственная документация
- Outdated docs worse than no docs → docs as code in repo

---

## Материалы

- Simon Brown — *Software Architecture for Developers*
- structurizr.com — C4 documentation
- arc42 template — comprehensive architecture documentation

---

## Практика

1. C4 Context + Container для проекта этапа 2
2. Structurizr DSL или Mermaid in repo
3. Dynamic diagram: «User places order» flow

---

## Критерии освоения

- [ ] 4 уровня C4 — что на каждом, для кого
- [ ] C4 diagrams для одной системы (Context + Container minimum)
- [ ] Diagrams in repo, рядом с кодом

---

## Связи

- [[ADR]]
- [[ArchiMate и моделирование]]
- [[Портфолио кейсов]]
