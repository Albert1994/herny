# ArchiMate и моделирование

**Этап:** [[00 Обзор этапа|4 — Архитектура ИС и предприятия]]  
**Время:** ~1 неделя

---

## Цель

Использовать стандартизированную нотацию для моделирования enterprise architecture на всех слоях.

---

## Ключевые концепции

### ArchiMate Layers
- **Business** — processes, actors, services, objects
- **Application** — components, interfaces, data objects
- **Technology** — nodes, devices, system software, networks
- **Motivation** — stakeholders, drivers, goals, requirements
- **Implementation & Migration** — work packages, deliverables, gaps

### Relationship types
- Assignment, Realization, Serving
- Access, Influence, Association
- Specialization, Flow, Triggering

### Viewpoints
- Layered View
- Motivation View
- Implementation View
- Outcome-based views for stakeholders

### Tools
- Archi (open source)
- Sparx Enterprise Architect
- BiZZdesign, LeanIX

### ArchiMate vs C4
- ArchiMate — enterprise, formal, TOGAF-aligned
- C4 — software-focused, developer-friendly
- Используются together: C4 for dev teams, ArchiMate for EA team

---

## Материалы

- The Open Group — ArchiMate Specification (overview)
- Archi tool — getting started
- Gerben Wierda — *Mastering ArchiMate*

---

## Практика

1. Business + Application layer diagram для одного process
2. Motivation view: goal → requirement → component
3. Gap analysis: baseline vs target architecture

---

## Критерии освоения

- [ ] Различаю business, application, technology layers
- [ ] Создал ArchiMate diagram с 3+ layers
- [ ] Знаю, когда ArchiMate vs C4

---

## Связи

- [[TOGAF и enterprise-фреймворки]]
- [[C4 Model и документирование]]
- [[Интеграционные паттерны]]
