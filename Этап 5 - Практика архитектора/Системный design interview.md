# Системный design interview

**Этап:** [[00 Обзор этапа|5 — Практика архитектора]]  
**Время:** ~3 недели (ongoing practice)

---

## Цель

Уверенно проходить system design interviews и использовать тот же framework для real-world architecture discussions.

---

## Ключевые концепции

### Interview framework (45–60 min)
1. **Requirements** (5 min) — functional + non-functional
2. **Estimation** (5 min) — users, QPS, storage (back-of-envelope)
3. **High-level design** (10 min) — boxes and arrows
4. **Deep dive** (20 min) — data model, API, scaling bottlenecks
5. **Wrap up** (5 min) — trade-offs, what you'd do with more time

### Common questions
- URL shortener (TinyURL)
- Twitter / News feed
- Chat system (WhatsApp)
- Rate limiter
- Web crawler
- Video streaming (YouTube)
- Ride sharing (Uber)
- E-commerce platform

### Back-of-envelope math
- 1 day ≈ 100K seconds (for QPS estimation)
- 1 million ≈ 2^20
- Storage: average object size × count
- Bandwidth: requests × payload size

### What interviewers evaluate
- Structured thinking
- Trade-off articulation
- Depth in 1–2 areas
- Communication
- Handling feedback and iteration

### Resources for practice
- «Designing Data-Intensive Applications» — deep knowledge
- ByteByteGo, System Design Interview (Alex Xu)
- HelloInterview, Exponent
- Pramp — peer mock interviews

---

## Материалы

- Alex Xu — *System Design Interview* (vol 1 & 2)
- educative.io — Grokking Modern System Design
- High Scalability blog — real architecture postmortems

---

## Практика

1. 10 system design problems с таймером 45 min
2. 3 mock interviews with peers or Pramp
3. Write post-mortem: what went well, what to improve

---

## Критерии освоения

- [ ] 10+ completed system design exercises
- [ ] 3 mock interviews with feedback
- [ ] Могу estimate QPS and storage за 5 min

---

## Связи

- [[Балансировка и CDN]]
- [[Масштабирование БД]]
- [[Кэширование]]
- [[Портфолио кейсов]]
