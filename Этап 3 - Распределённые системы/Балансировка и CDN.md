# Балансировка и CDN

**Этап:** [[00 Обзор этапа|3 — Распределённые системы]]  
**Время:** ~1 неделя

---

## Цель

Распределять нагрузку и доставлять контент пользователям с минимальной latency через load balancing и CDN.

---

## Ключевые концепции

### Load Balancer types
- **L4 (Transport)** — TCP/UDP, fast, no content awareness
- **L7 (Application)** — HTTP routing, SSL termination, path-based routing

### Algorithms
- Round Robin, Weighted Round Robin
- Least Connections
- IP Hash (session affinity)
- Consistent Hashing — minimal redistribution on node change

### HA architecture
```
Client → DNS → LB → [App, App, App] → DB
```
- Active-active vs active-passive
- Health checks
- Sticky sessions — when needed, when harmful

### CDN (Content Delivery Network)
- Edge caching static assets
- Dynamic content acceleration
- DDoS protection (Cloudflare, Akamai)
- Cache-Control headers

### Global load balancing
- GeoDNS / Anycast
- Multi-region active-active
- Data residency considerations

---

## Материалы

- NGINX documentation — load balancing
- Cloudflare Learning Center
- AWS — Elastic Load Balancing guide

---

## Практика

1. nginx reverse proxy + 2 backend instances
2. CDN setup for static assets, measure TTFB
3. Diagram: global traffic flow for multi-region app

---

## Критерии освоения

- [ ] Различаю L4 и L7 load balancing
- [ ] Объясняю consistent hashing use case
- [ ] Знаю, когда CDN нужен vs overkill

---

## Связи

- [[Кэширование]]
- [[../Этап 0 - Фундамент/Сети и протоколы|Сети и протоколы]]
- [[Системный design interview]]
