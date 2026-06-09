# Архитектурный review

**Этап:** [[00 Обзор этапа|5 — Практика архитектора]]  
**Время:** ~1 неделя

---

## Цель

Проводить и участвовать в architecture reviews — structured process для оценки design decisions до implementation.

---

## Ключевые концепции

### When to review
- New system or major feature
- Significant technology change
- Cross-team integration
- Before production deployment of critical path

### Review checklist
- [ ] Business goals and NFR clear?
- [ ] C4 Context + Container diagrams present?
- [ ] Key decisions documented (ADR)?
- [ ] Security threat model done?
- [ ] Failure modes considered?
- [ ] Scalability path defined?
- [ ] Operational concerns (monitoring, runbooks)?
- [ ] Migration/rollback plan?

### Review formats
- **Design review meeting** — 60 min, presenter + reviewers
- **Async review** — RFC document, comments in PR
- **Architecture Review Board (ARB)** — enterprise governance

### Giving feedback
- Focus on risks and trade-offs, not «I would do differently»
- Ask questions: «What happens if X fails?»
- Severity: Blocker / Concern / Suggestion / Praise

### Receiving feedback
- Don't defend — understand concern
- Document decisions and dissent (disagree and commit)
- Follow up with updated ADR

---

## Материалы

- Google — Design Doc culture
- Thoughtworks — Architecture Decision Guidance
- Own experience — review 3 open-source architecture docs

---

## Практика

1. Review open-source project's architecture README
2. Conduct mock review for peer's project (30 min)
3. Write review report: findings + recommendations

---

## Критерии освоения

- [ ] Провёл mock review с structured feedback
- [ ] Review checklist использую systematically
- [ ] Получил review на свой проект этапа 4 и addressed findings

---

## Связи

- [[ADR]]
- [[C4 Model и документирование]]
- [[Коммуникация со стейкхолдерами]]
