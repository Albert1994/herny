# CAP и согласованность

**Этап:** [[00 Обзор этапа|3 — Распределённые системы]]  
**Время:** ~1 неделя

---

## Цель

Понимать фундаментальные trade-offs распределённых данных и выбирать модель согласованности под бизнес-требования.

---

## Ключевые концепции

### CAP Theorem
При network **P**artition можно выбрать только одно:
- **C**onsistency — все nodes видят одни данные
- **A**vailability — каждый запрос получает ответ

На практике: не binary choice, а spectrum.

### PACELC
If **P**artition → choose **A** or **C**  
**E**lse → choose **L**atency or **C**onsistency

### Модели согласованности
| Модель | Описание |
|--------|----------|
| Strong | Linearizability |
| Sequential | Operations appear in some order |
| Causal | Causally related ops ordered |
| Eventual | Converge over time |
| Read-your-writes | User sees own writes |

### Практические примеры
- PostgreSQL — CP (strong consistency)
- Cassandra — AP (tunable consistency)
- Redis Cluster — eventual under partition

---

## Материалы

- *Designing Data-Intensive Applications* — Kleppmann (ch. 7, 9)
- Daniel Abadi — «PACELC» blog post
- Jepsen.io — consistency testing reports

---

## Практика

1. Для 3 use cases выбрать consistency model и обосновать
2. Read Cassandra QUORUM vs ONE
3. Описать «lost update» problem и решение (optimistic locking)

---

## Критерии освоения

- [ ] Объясняю CAP без oversimplification
- [ ] Выбираю consistency/latency trade-off для кейса
- [ ] Знаю разницу strong vs eventual на примере

---

## Связи

- [[../Этап 0 - Фундамент/Базы данных SQL и NoSQL/Базы данных SQL и NoSQL|Базы данных]]
- [[Масштабирование БД]]
- [[CQRS и Event Sourcing]]
