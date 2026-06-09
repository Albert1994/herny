# NFR и атрибуты качества

**Этап:** [[00 Обзор этапа|4 — Архитектура ИС и предприятия]]  
**Время:** ~2 недели

---

## Цель

Формулировать, приоритизировать и проектировать под нефункциональные требования — то, что отличает архитектора от senior developer.

---

## Ключевые концепции

### ISO 25010 Quality Attributes
- **Functional suitability**
- **Performance efficiency** — time behavior, resource utilization
- **Compatibility** — interoperability
- **Usability**
- **Reliability** — maturity, availability, fault tolerance
- **Security**
- **Maintainability** — modularity, reusability, testability
- **Portability**

### Архитектурно значимые NFR
| Атрибут | Пример метрики |
|---------|----------------|
| Availability | 99.95% uptime |
| Latency | p99 < 200ms |
| Throughput | 10K RPS |
| Scalability | 10x growth без redesign |
| Security | PCI DSS, GDPR |
| Recoverability | RTO 1h, RPO 15min |

### Quality Attribute Scenarios (SEI)
- **Stimulus** — что происходит
- **Source** — кто/что инициирует
- **Artifact** — что затронуто
- **Environment** — under what conditions
- **Response** — expected behavior
- **Measure** — how to verify

### Trade-offs
- Performance vs Security
- Consistency vs Availability
- Time-to-market vs Maintainability
- **Architectural significance:** решение, которое сложно изменить позже

---

## Материалы

- Len Bass et al. — *Software Architecture in Practice*
- Mark Richards — «Identifying Architectural Characteristics»
- SEI — Quality Attribute Workshops (QAW)

---

## Практика

1. NFR matrix для e-commerce (15+ requirements)
2. 5 quality attribute scenarios в формате SEI
3. Prioritize: MoSCoW или weighted scoring

---

## Критерии освоения

- [ ] Формулирую NFR измеримо (не «быстро» а «p99 < 200ms»)
- [ ] Провожу trade-off analysis для 2 conflicting NFR
- [ ] NFR matrix в проекте этапа 4

---

## Связи

- [[Отказоустойчивость]]
- [[Архитектура безопасности]]
- [[ADR]]
