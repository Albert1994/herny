# Observability

**Этап:** [[00 Обзор этапа|3 — Распределённые системы]]  
**Время:** ~2 недели

---

## Цель

Строить системы, которые можно понять в production: logs, metrics, traces — три столпа observability.

---

## Ключевые концепции

### Three Pillars
| Pillar | Что | Tools |
|--------|-----|-------|
| **Logs** | Discrete events | ELK, Loki, CloudWatch |
| **Metrics** | Aggregated numbers | Prometheus, Grafana, Datadog |
| **Traces** | Request journey | Jaeger, Zipkin, OpenTelemetry |

### Structured logging
- JSON format, not plain text
- Correlation ID / Trace ID across services
- Log levels: ERROR needs action, WARN needs attention
- Don't log PII/secrets

### Metrics (RED / USE)
- **RED** (services): Rate, Errors, Duration
- **USE** (resources): Utilization, Saturation, Errors
- Golden signals: latency, traffic, errors, saturation

### Distributed Tracing
- Span, trace, parent-child
- OpenTelemetry — vendor-neutral standard
- Sampling strategies (head vs tail)

### Alerting
- Alert on symptoms, not causes
- Runbooks linked to alerts
- Avoid alert fatigue

---

## Материалы

- *Observability Engineering* — Majors, Fong-Jones, Miranda
- OpenTelemetry documentation
- Google SRE — Monitoring Distributed Systems

---

## Практика

1. OpenTelemetry instrumentation in 2 services
2. Grafana dashboard: RED metrics
3. Alert: error rate > 1% for 5 min → runbook link

---

## Критерии освоения

- [ ] Trace request через 3 services в Jaeger
- [ ] Dashboard с rate, errors, duration
- [ ] Structured logs с correlation ID

---

## Связи

- [[Отказоустойчивость]]
- [[Микросервисы]]
- [[NFR и атрибуты качества]]
