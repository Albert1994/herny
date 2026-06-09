# Serverless и FaaS

**Этап:** [[00 Обзор этапа|2 — Архитектурные стили]]  
**Время:** ~1 неделя

---

## Цель

Понимать serverless как архитектурный стиль: функции как compute, managed services, event-driven triggers.

---

## Ключевые концепции

### FaaS (Function as a Service)
- AWS Lambda, Azure Functions, Google Cloud Functions
- Pay per invocation
- Cold start problem
- Stateless functions, limited execution time

### Serverless ecosystem
- **Compute:** Lambda, Cloud Run
- **Storage:** S3, DynamoDB
- **Messaging:** SNS/SQS, EventBridge
- **API:** API Gateway

### Patterns
- **Function pipeline** — S3 upload → Lambda → DynamoDB
- **Strangler on serverless** — proxy через API Gateway
- **Backend for Frontend (BFF)** на Lambda

### Trade-offs
| Плюсы | Минусы |
|-------|--------|
| No server management | Vendor lock-in |
| Auto-scaling | Cold starts |
| Cost at low traffic | Debugging complexity |
| Event-native | Stateless limits |

### When to use
- Spiky/unpredictable traffic
- Event processing pipelines
- Prototypes and MVPs
- Не для: long-running, stateful, low-latency critical paths

---

## Материалы

- AWS Well-Architected Serverless Lens
- *Serverless Architectures on AWS* — J. Sbarski
- Serverless Framework / SAM documentation

---

## Практика

1. Lambda function triggered by SQS message
2. Measure cold start vs warm latency
3. Cost estimate: 1M invocations/month

---

## Критерии освоения

- [ ] Объясняю cold start и mitigation strategies
- [ ] Знаю serverless vs containers trade-offs
- [ ] Спроектировал event-driven pipeline на serverless

---

## Связи

- [[Event-Driven Architecture]]
- [[Serverless и FaaS]] → [[Оценка и выбор технологий]]
- [[Микросервисы]] — complementary, not replacement
