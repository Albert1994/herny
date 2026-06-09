# ADR — Architecture Decision Records

**Этап:** [[00 Обзор этапа|4 — Архитектура ИС и предприятия]]  
**Время:** ~1 неделя

---

## Цель

Фиксировать архитектурные решения с контекстом, alternatives и consequences — living documentation для команды.

---

## Ключевые концепции

### Формат ADR (Michael Nygard)
```markdown
# ADR-001: [Title]

## Status
Proposed | Accepted | Deprecated | Superseded by ADR-XXX

## Context
What is the issue that we're seeing that is motivating this decision?

## Decision
What is the change that we're proposing and/or doing?

## Consequences
What becomes easier or harder because of this change?
```

### When to write ADR
- Выбор БД, message broker, cloud provider
- Monolith vs microservices split
- Authentication strategy
- Caching strategy
- Breaking API changes

### Best practices
- One decision per ADR
- Immutable once accepted (supersede, don't edit)
- Store in repo: `/docs/adr/`
- Number sequentially: ADR-001, ADR-002
- Lightweight — 1 page max

### Tools
- adr-tools (CLI)
- Log4brains
- Markdown in git

### Alternatives considered
Always document what you **didn't** choose and why — это самая ценная часть для будущей команды.

---

## Материалы

- Michael Nygard — «Documenting Architecture Decisions»
- Joel Parker Henderson — ADR templates collection
- Thoughtworks Technology Radar — ADR adoption

---

## Практика

1. Написать 5 ADR для проекта этапа 4
2. Setup adr-tools in repo
3. Review: ADR understandable for new team member?

---

## Критерии освоения

- [ ] ADR с context, decision, consequences
- [ ] ≥ 5 ADR в проекте этапа 4
- [ ] Знаю lifecycle: Proposed → Accepted → Superseded

---

## Связи

- [[C4 Model и документирование]]
- [[Оценка и выбор технологий]]
- [[Архитектурный review]]
