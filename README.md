<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:1a73e8,100:6c63ff&text=THONG NGUYEN&fontAlign=50&fontAlignY=36&fontSize=52&desc=Software%20Engineer%20%C2%B7%20AI%2FML%20%C2%B7%20Systems&descAlignY=58&animation=fadeIn" alt="Header">
</p>

<h1 align="center">Design simply. Measure honestly. Scale responsibly.</h1>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=thongnguyenslife&style=for-the-badge&color=1a73e8" alt="Views">
  <img src="https://img.shields.io/badge/Focus-AI%2FML%20%7C%20Backend%20%7C%20Cloud-0b1021?style=for-the-badge" alt="Focus">
  <img src="https://img.shields.io/badge/Principles-Clarity%20%7C%20Reliability%20%7C%20Impact-0b1021?style=for-the-badge" alt="Principles">
</p>

---

## Executive Summary

I design reliable, scalable, and observable software and ML systems. I value clear interfaces, measurable outcomes, and an excellent developer experience.
I focus on shipping fast without compromising long-term maintainability and user impact.

---

## Core Competencies

**Backend & APIs** — FastAPI/Express; domain modeling; idempotency; consistency; rate limiting  
**AI/ML** — scikit-learn, TensorFlow, PyTorch; feature engineering; evaluation and error analysis  
**Data & Pipelines** — Airflow DAGs; ETL/ELT; data validation; versioned datasets and artifacts; reproducibility  
**MLOps & DevOps** — packaging and serving; A/B and shadow deploys; latency, quality, and drift monitoring; Docker; Linux; CI/CD with GitHub Actions; observability (logs, metrics, traces)  
**Frontend** — React, Vite, Tailwind; accessibility; basic SEO

---

## Operating Tenets

- Design for clarity and explicit interfaces
- Prove with tests for critical paths
- Measure before tuning (p95, p99, error budget, cost)
- Automate repeatable workflows and releases
- Document technical decisions with concise ADRs

---

## Architectural Decisions (ADRs)

### ADR 01: Service Boundaries

**Context**  
Multiple teams contribute to a monolith that slows delivery.

**Decision**  
Extract user-facing features into a FastAPI service with clear contracts.

**Consequences**  
Faster iteration; more explicit SLAs; extra infra overhead.

### ADR 02: Authentication Strategy

**Context**  
Several endpoints handle auth ad-hoc.

**Decision**  
Introduce a single middleware with token validation and scopes.

**Consequences**  
Reduced duplication; simpler audits; centralized failure mode.

### ADR 03: Model Serving Pattern

**Context**  
Batch job used for online predictions.

**Decision**  
Adopt online serving with caching and feature store sync.

**Consequences**  
Lower latency; need strong cache invalidation rules.

### ADR 04: CI Speed

**Context**  
Builds take 20+ minutes.

**Decision**  
Use incremental builds and artifact reuse.

**Consequences**  
CI minutes drop; cache needs pruning policy.

### ADR 05: Data Contracts

**Context**  
Schema changes break downstream jobs.

**Decision**  
Define JSON-schema contracts and validate at boundaries.

**Consequences**  
Earlier failures; clearer ownership; some ceremony added.

### ADR 06: Rollout Safety

**Context**  
Deploys cause occasional regressions.

**Decision**  
Use canary with automatic rollback on SLO burn.

**Consequences**  
Lower blast radius; extra metrics and alerts to maintain.

### ADR 07: Logging Policy

**Context**  
Verbose logs cause cost spikes.

**Decision**  
Introduce log budgets and sampling per endpoint.

**Consequences**  
Lower cost; require tuning for rare failures.

### ADR 08: Feature Flags

**Context**  
Hard-coded toggles across codebase.

**Decision**  
Centralize flags with kill switches.

**Consequences**  
Safer experiments; risk of flag sprawl.

### ADR 09: Secrets Management

**Context**  
Secrets in env files checked in by mistake.

**Decision**  
Use a vault and short-lived tokens.

**Consequences**  
Fewer leaks; rotation discipline required.

### ADR 10: Schema Migrations

**Context**  
Downtime during migrations.

**Decision**  
Use online, backward-compatible migrations.

**Consequences**  
Zero-downtime; more phased releases.

### ADR 11: Queue Backpressure

**Context**  
Spikes overwhelm consumers.

**Decision**  
Apply rate limits and circuit breakers.

**Consequences**  
Protects downstream; may throttle good traffic.

### ADR 12: Observability

**Context**  
Hard to trace cross-service issues.

**Decision**  
Add tracing and consistent correlation IDs.

**Consequences**  
Better MTTR; overhead in propagation.

---

## Production Checklists

### Backend Review

- [ ] Endpoints have explicit contracts
- [ ] Idempotency ensured for unsafe methods
- [ ] Pagination and filtering are consistent
- [ ] Input validation and error types standardized
- [ ] Rate limits documented and tested
- [ ] Timeouts and retries defined at clients
- [ ] Circuit breakers enabled for dependencies
- [ ] Graceful degradation paths documented
- [ ] Versioning policy followed
- [ ] Security headers applied
- [ ] OpenAPI spec updated
- [ ] Cache keys and TTLs documented
- [ ] Heavy endpoints profiled and optimized
- [ ] Ownership and on-call rotation listed

### ML Evaluation

- [ ] Datasets versioned and labeled
- [ ] Train, validation, test splits fixed and logged
- [ ] Metrics clear: accuracy, F1, AUC, calibration
- [ ] Ablations recorded and reproducible
- [ ] Bias and fairness checks documented
- [ ] Drift detection thresholds set
- [ ] Shadow or A/B plan prepared
- [ ] Safety filters and guardrails in place
- [ ] Latency budgets respected
- [ ] Rollback plan defined
- [ ] Model cards updated
- [ ] Feature store sync checks

### Data Quality

- [ ] Schema contracts enforced
- [ ] Null and range checks in place
- [ ] Deduplication strategy documented
- [ ] Backfills tested and idempotent
- [ ] Late-arriving data policy defined
- [ ] PII handling and redaction reviewed
- [ ] Lineage visible in catalog
- [ ] SLAs on freshness documented
- [ ] Sampling plans for validation
- [ ] Alert routing and owners set

### Security

- [ ] Least-privilege access applied
- [ ] Secrets stored in a vault
- [ ] Token rotation schedule in place
- [ ] Third-party dependencies audited
- [ ] SBOM generated and tracked
- [ ] Input validation standardized
- [ ] Output encoding where needed
- [ ] HTTPS everywhere
- [ ] CSP and security headers set
- [ ] PII redaction in logs
- [ ] Access review cadence defined

### SRE Operations

- [ ] SLOs and SLIs defined
- [ ] Error budget policy agreed
- [ ] Dashboards have RED/USE views
- [ ] Alerts actionable and rate-limited
- [ ] Runbooks up to date
- [ ] Canary and progressive rollout paths
- [ ] On-call handover template
- [ ] Postmortem template and owners
- [ ] Capacity plan and autoscaling policy
- [ ] DR and backup strategy validated

---

## Impact Highlights

- Reduced service p95 latency by [fill: %] via caching and lean payloads
- Improved NLP task completion by [fill: %] with better labeling and fallbacks
- Cut CI minutes by [fill: %] using incremental builds and artifact reuse
- Raised pipeline success rate to [fill: %] with schema checks and proactive alerts

> Replace bracketed values with real metrics when available.

---

## Selected Work

**AI Chatbot (NLP)**  
Transformers with FastAPI; intent classification; confidence thresholds; safe fallbacks; telemetry-driven iteration

**Personal Portfolio**  
React with Vite and Tailwind; optimized TTFB and Core Web Vitals; semantic HTML and accessible patterns

**Data Science Pipeline**  
Airflow ETL -> feature store -> training -> evaluation; versioned datasets and automated reports

<details>
  <summary><b>Case Study · Chatbot Quality</b></summary>
  Tighter labels and thresholds reduce false positives  
  Lightweight model and caching lower p95 latency  
  Clear fallback paths increase successful outcomes
</details>

<details>
  <summary><b>Case Study · Pipeline Reliability</b></summary>
  Schema-drift guards and null checks  
  Pinned dependencies and reproducible runs  
  Scheduled summaries with trend snapshots
</details>

---

## SLO & Operations

- Availability SLO: [fill: 99.9% / 99.95%] uptime
- Latency SLO: [fill: p95 <= XXX ms] for key endpoints
- Error budget: [fill: %] per 30-day window; review on burn
- Releases: canary/progressive rollout; safe rollbacks; runbooks for incidents

---

## Security & Privacy

Least privilege; secret management and token rotation; input validation; safe model serving; PII redaction; dependency audits and regular patch cadence.

---

## Tech Radar

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,js,ts,react,nodejs,express,fastapi,tailwind,postgres,mysql,redis,sklearn,tensorflow,pytorch,airflow,docker,linux,git,githubactions,kubernetes" alt="Tech Icons">
</p>

---

## Activity & Metrics

<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=thongnguyenslife&show_icons=true&theme=transparent&hide_border=true" alt="Stats">
  <img height="160" src="https://streak-stats.demolab.com?user=thongnguyenslife&theme=transparent&hide_border=true" alt="Streak">
</p>
<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=thongnguyenslife&layout=compact&theme=transparent&hide_border=true" alt="Top Languages">
</p>

---

## 2025 Objectives (OKR style)

- O1: Demonstrate production-grade ML craft  
  - KR1: Ship 2 ML demos with docs/tests  
  - KR2: Publish latency and throughput benchmarks
- O2: Improve developer effectiveness  
  - KR1: Reduce CI time by [fill: %]  
  - KR2: Open-source a small utilities library
- O3: Share knowledge  
  - KR1: Write 3 concise engineering notes

---

## FAQ

**Q1.** How do you approach problem 1?
**A1.** Start with first principles, define constraints, prototype, measure, iterate.
**Q2.** How do you approach problem 2?
**A2.** Start with first principles, define constraints, prototype, measure, iterate.
**Q3.** How do you approach problem 3?
**A3.** Start with first principles, define constraints, prototype, measure, iterate.
**Q4.** How do you approach problem 4?
**A4.** Start with first principles, define constraints, prototype, measure, iterate.
**Q5.** How do you approach problem 5?
**A5.** Start with first principles, define constraints, prototype, measure, iterate.
**Q6.** How do you approach problem 6?
**A6.** Start with first principles, define constraints, prototype, measure, iterate.
**Q7.** How do you approach problem 7?
**A7.** Start with first principles, define constraints, prototype, measure, iterate.
**Q8.** How do you approach problem 8?
**A8.** Start with first principles, define constraints, prototype, measure, iterate.
**Q9.** How do you approach problem 9?
**A9.** Start with first principles, define constraints, prototype, measure, iterate.
**Q10.** How do you approach problem 10?
**A10.** Start with first principles, define constraints, prototype, measure, iterate.
**Q11.** How do you approach problem 11?
**A11.** Start with first principles, define constraints, prototype, measure, iterate.
**Q12.** How do you approach problem 12?
**A12.** Start with first principles, define constraints, prototype, measure, iterate.
**Q13.** How do you approach problem 13?
**A13.** Start with first principles, define constraints, prototype, measure, iterate.
**Q14.** How do you approach problem 14?
**A14.** Start with first principles, define constraints, prototype, measure, iterate.
**Q15.** How do you approach problem 15?
**A15.** Start with first principles, define constraints, prototype, measure, iterate.
**Q16.** How do you approach problem 16?
**A16.** Start with first principles, define constraints, prototype, measure, iterate.
**Q17.** How do you approach problem 17?
**A17.** Start with first principles, define constraints, prototype, measure, iterate.
**Q18.** How do you approach problem 18?
**A18.** Start with first principles, define constraints, prototype, measure, iterate.
**Q19.** How do you approach problem 19?
**A19.** Start with first principles, define constraints, prototype, measure, iterate.
**Q20.** How do you approach problem 20?
**A20.** Start with first principles, define constraints, prototype, measure, iterate.
**Q21.** How do you approach problem 21?
**A21.** Start with first principles, define constraints, prototype, measure, iterate.
**Q22.** How do you approach problem 22?
**A22.** Start with first principles, define constraints, prototype, measure, iterate.
**Q23.** How do you approach problem 23?
**A23.** Start with first principles, define constraints, prototype, measure, iterate.
**Q24.** How do you approach problem 24?
**A24.** Start with first principles, define constraints, prototype, measure, iterate.
**Q25.** How do you approach problem 25?
**A25.** Start with first principles, define constraints, prototype, measure, iterate.
**Q26.** How do you approach problem 26?
**A26.** Start with first principles, define constraints, prototype, measure, iterate.
**Q27.** How do you approach problem 27?
**A27.** Start with first principles, define constraints, prototype, measure, iterate.
**Q28.** How do you approach problem 28?
**A28.** Start with first principles, define constraints, prototype, measure, iterate.
**Q29.** How do you approach problem 29?
**A29.** Start with first principles, define constraints, prototype, measure, iterate.
**Q30.** How do you approach problem 30?
**A30.** Start with first principles, define constraints, prototype, measure, iterate.
**Q31.** How do you approach problem 31?
**A31.** Start with first principles, define constraints, prototype, measure, iterate.
**Q32.** How do you approach problem 32?
**A32.** Start with first principles, define constraints, prototype, measure, iterate.
**Q33.** How do you approach problem 33?
**A33.** Start with first principles, define constraints, prototype, measure, iterate.
**Q34.** How do you approach problem 34?
**A34.** Start with first principles, define constraints, prototype, measure, iterate.
**Q35.** How do you approach problem 35?
**A35.** Start with first principles, define constraints, prototype, measure, iterate.
**Q36.** How do you approach problem 36?
**A36.** Start with first principles, define constraints, prototype, measure, iterate.
**Q37.** How do you approach problem 37?
**A37.** Start with first principles, define constraints, prototype, measure, iterate.
**Q38.** How do you approach problem 38?
**A38.** Start with first principles, define constraints, prototype, measure, iterate.
**Q39.** How do you approach problem 39?
**A39.** Start with first principles, define constraints, prototype, measure, iterate.
**Q40.** How do you approach problem 40?
**A40.** Start with first principles, define constraints, prototype, measure, iterate.
**Q41.** How do you approach problem 41?
**A41.** Start with first principles, define constraints, prototype, measure, iterate.
**Q42.** How do you approach problem 42?
**A42.** Start with first principles, define constraints, prototype, measure, iterate.
**Q43.** How do you approach problem 43?
**A43.** Start with first principles, define constraints, prototype, measure, iterate.
**Q44.** How do you approach problem 44?
**A44.** Start with first principles, define constraints, prototype, measure, iterate.
**Q45.** How do you approach problem 45?
**A45.** Start with first principles, define constraints, prototype, measure, iterate.
**Q46.** How do you approach problem 46?
**A46.** Start with first principles, define constraints, prototype, measure, iterate.
**Q47.** How do you approach problem 47?
**A47.** Start with first principles, define constraints, prototype, measure, iterate.
**Q48.** How do you approach problem 48?
**A48.** Start with first principles, define constraints, prototype, measure, iterate.
**Q49.** How do you approach problem 49?
**A49.** Start with first principles, define constraints, prototype, measure, iterate.
**Q50.** How do you approach problem 50?
**A50.** Start with first principles, define constraints, prototype, measure, iterate.
**Q51.** How do you approach problem 51?
**A51.** Start with first principles, define constraints, prototype, measure, iterate.
**Q52.** How do you approach problem 52?
**A52.** Start with first principles, define constraints, prototype, measure, iterate.
**Q53.** How do you approach problem 53?
**A53.** Start with first principles, define constraints, prototype, measure, iterate.
**Q54.** How do you approach problem 54?
**A54.** Start with first principles, define constraints, prototype, measure, iterate.
**Q55.** How do you approach problem 55?
**A55.** Start with first principles, define constraints, prototype, measure, iterate.
**Q56.** How do you approach problem 56?
**A56.** Start with first principles, define constraints, prototype, measure, iterate.
**Q57.** How do you approach problem 57?
**A57.** Start with first principles, define constraints, prototype, measure, iterate.
**Q58.** How do you approach problem 58?
**A58.** Start with first principles, define constraints, prototype, measure, iterate.
**Q59.** How do you approach problem 59?
**A59.** Start with first principles, define constraints, prototype, measure, iterate.
**Q60.** How do you approach problem 60?
**A60.** Start with first principles, define constraints, prototype, measure, iterate.

---

## Glossary

**A** — term: definition, context, and why it matters.
**B** — term: definition, context, and why it matters.
**C** — term: definition, context, and why it matters.
**D** — term: definition, context, and why it matters.
**E** — term: definition, context, and why it matters.
**F** — term: definition, context, and why it matters.
**G** — term: definition, context, and why it matters.
**H** — term: definition, context, and why it matters.
**I** — term: definition, context, and why it matters.
**J** — term: definition, context, and why it matters.
**K** — term: definition, context, and why it matters.
**L** — term: definition, context, and why it matters.
**M** — term: definition, context, and why it matters.
**N** — term: definition, context, and why it matters.
**O** — term: definition, context, and why it matters.
**P** — term: definition, context, and why it matters.
**Q** — term: definition, context, and why it matters.
**R** — term: definition, context, and why it matters.
**S** — term: definition, context, and why it matters.
**T** — term: definition, context, and why it matters.
**U** — term: definition, context, and why it matters.
**V** — term: definition, context, and why it matters.
**W** — term: definition, context, and why it matters.
**X** — term: definition, context, and why it matters.
**Y** — term: definition, context, and why it matters.
**Z** — term: definition, context, and why it matters.

---

## Changelog

- 2025-Q2: milestone 1 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 2 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 3 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 4 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 5 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 6 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 7 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 8 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 9 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 10 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 11 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 12 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 13 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 14 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 15 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 16 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 17 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 18 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 19 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 20 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 21 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 22 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 23 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 24 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 25 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 26 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 27 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 28 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 29 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 30 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 31 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 32 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 33 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 34 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 35 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 36 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 37 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 38 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 39 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 40 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 41 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 42 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 43 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 44 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 45 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 46 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 47 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 48 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 49 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 50 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 51 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 52 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 53 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 54 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 55 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 56 delivered; notes, owners, metrics recorded.
- 2025-Q2: milestone 57 delivered; notes, owners, metrics recorded.
- 2025-Q3: milestone 58 delivered; notes, owners, metrics recorded.
- 2025-Q4: milestone 59 delivered; notes, owners, metrics recorded.
- 2025-Q1: milestone 60 delivered; notes, owners, metrics recorded.

---

## Engineering Library

### Code Review

- Guideline 1: keep it simple, explicit, and measurable.
- Guideline 2: keep it simple, explicit, and measurable.
- Guideline 3: keep it simple, explicit, and measurable.
- Guideline 4: keep it simple, explicit, and measurable.
- Guideline 5: keep it simple, explicit, and measurable.
- Guideline 6: keep it simple, explicit, and measurable.
- Guideline 7: keep it simple, explicit, and measurable.
- Guideline 8: keep it simple, explicit, and measurable.
- Guideline 9: keep it simple, explicit, and measurable.
- Guideline 10: keep it simple, explicit, and measurable.
- Guideline 11: keep it simple, explicit, and measurable.
- Guideline 12: keep it simple, explicit, and measurable.
- Guideline 13: keep it simple, explicit, and measurable.
- Guideline 14: keep it simple, explicit, and measurable.
- Guideline 15: keep it simple, explicit, and measurable.
- Guideline 16: keep it simple, explicit, and measurable.
- Guideline 17: keep it simple, explicit, and measurable.
- Guideline 18: keep it simple, explicit, and measurable.
- Guideline 19: keep it simple, explicit, and measurable.
- Guideline 20: keep it simple, explicit, and measurable.
- Guideline 21: keep it simple, explicit, and measurable.
- Guideline 22: keep it simple, explicit, and measurable.
- Guideline 23: keep it simple, explicit, and measurable.
- Guideline 24: keep it simple, explicit, and measurable.
- Guideline 25: keep it simple, explicit, and measurable.

### Testing

- Guideline 1: keep it simple, explicit, and measurable.
- Guideline 2: keep it simple, explicit, and measurable.
- Guideline 3: keep it simple, explicit, and measurable.
- Guideline 4: keep it simple, explicit, and measurable.
- Guideline 5: keep it simple, explicit, and measurable.
- Guideline 6: keep it simple, explicit, and measurable.
- Guideline 7: keep it simple, explicit, and measurable.
- Guideline 8: keep it simple, explicit, and measurable.
- Guideline 9: keep it simple, explicit, and measurable.
- Guideline 10: keep it simple, explicit, and measurable.
- Guideline 11: keep it simple, explicit, and measurable.
- Guideline 12: keep it simple, explicit, and measurable.
- Guideline 13: keep it simple, explicit, and measurable.
- Guideline 14: keep it simple, explicit, and measurable.
- Guideline 15: keep it simple, explicit, and measurable.
- Guideline 16: keep it simple, explicit, and measurable.
- Guideline 17: keep it simple, explicit, and measurable.
- Guideline 18: keep it simple, explicit, and measurable.
- Guideline 19: keep it simple, explicit, and measurable.
- Guideline 20: keep it simple, explicit, and measurable.
- Guideline 21: keep it simple, explicit, and measurable.
- Guideline 22: keep it simple, explicit, and measurable.
- Guideline 23: keep it simple, explicit, and measurable.
- Guideline 24: keep it simple, explicit, and measurable.
- Guideline 25: keep it simple, explicit, and measurable.

### Performance

- Guideline 1: keep it simple, explicit, and measurable.
- Guideline 2: keep it simple, explicit, and measurable.
- Guideline 3: keep it simple, explicit, and measurable.
- Guideline 4: keep it simple, explicit, and measurable.
- Guideline 5: keep it simple, explicit, and measurable.
- Guideline 6: keep it simple, explicit, and measurable.
- Guideline 7: keep it simple, explicit, and measurable.
- Guideline 8: keep it simple, explicit, and measurable.
- Guideline 9: keep it simple, explicit, and measurable.
- Guideline 10: keep it simple, explicit, and measurable.
- Guideline 11: keep it simple, explicit, and measurable.
- Guideline 12: keep it simple, explicit, and measurable.
- Guideline 13: keep it simple, explicit, and measurable.
- Guideline 14: keep it simple, explicit, and measurable.
- Guideline 15: keep it simple, explicit, and measurable.
- Guideline 16: keep it simple, explicit, and measurable.
- Guideline 17: keep it simple, explicit, and measurable.
- Guideline 18: keep it simple, explicit, and measurable.
- Guideline 19: keep it simple, explicit, and measurable.
- Guideline 20: keep it simple, explicit, and measurable.
- Guideline 21: keep it simple, explicit, and measurable.
- Guideline 22: keep it simple, explicit, and measurable.
- Guideline 23: keep it simple, explicit, and measurable.
- Guideline 24: keep it simple, explicit, and measurable.
- Guideline 25: keep it simple, explicit, and measurable.

### Data Quality

- Guideline 1: keep it simple, explicit, and measurable.
- Guideline 2: keep it simple, explicit, and measurable.
- Guideline 3: keep it simple, explicit, and measurable.
- Guideline 4: keep it simple, explicit, and measurable.
- Guideline 5: keep it simple, explicit, and measurable.
- Guideline 6: keep it simple, explicit, and measurable.
- Guideline 7: keep it simple, explicit, and measurable.
- Guideline 8: keep it simple, explicit, and measurable.
- Guideline 9: keep it simple, explicit, and measurable.
- Guideline 10: keep it simple, explicit, and measurable.
- Guideline 11: keep it simple, explicit, and measurable.
- Guideline 12: keep it simple, explicit, and measurable.
- Guideline 13: keep it simple, explicit, and measurable.
- Guideline 14: keep it simple, explicit, and measurable.
- Guideline 15: keep it simple, explicit, and measurable.
- Guideline 16: keep it simple, explicit, and measurable.
- Guideline 17: keep it simple, explicit, and measurable.
- Guideline 18: keep it simple, explicit, and measurable.
- Guideline 19: keep it simple, explicit, and measurable.
- Guideline 20: keep it simple, explicit, and measurable.
- Guideline 21: keep it simple, explicit, and measurable.
- Guideline 22: keep it simple, explicit, and measurable.
- Guideline 23: keep it simple, explicit, and measurable.
- Guideline 24: keep it simple, explicit, and measurable.
- Guideline 25: keep it simple, explicit, and measurable.

### Deployment

- Guideline 1: keep it simple, explicit, and measurable.
- Guideline 2: keep it simple, explicit, and measurable.
- Guideline 3: keep it simple, explicit, and measurable.
- Guideline 4: keep it simple, explicit, and measurable.
- Guideline 5: keep it simple, explicit, and measurable.
- Guideline 6: keep it simple, explicit, and measurable.
- Guideline 7: keep it simple, explicit, and measurable.
- Guideline 8: keep it simple, explicit, and measurable.
- Guideline 9: keep it simple, explicit, and measurable.
- Guideline 10: keep it simple, explicit, and measurable.
- Guideline 11: keep it simple, explicit, and measurable.
- Guideline 12: keep it simple, explicit, and measurable.
- Guideline 13: keep it simple, explicit, and measurable.
- Guideline 14: keep it simple, explicit, and measurable.
- Guideline 15: keep it simple, explicit, and measurable.
- Guideline 16: keep it simple, explicit, and measurable.
- Guideline 17: keep it simple, explicit, and measurable.
- Guideline 18: keep it simple, explicit, and measurable.
- Guideline 19: keep it simple, explicit, and measurable.
- Guideline 20: keep it simple, explicit, and measurable.
- Guideline 21: keep it simple, explicit, and measurable.
- Guideline 22: keep it simple, explicit, and measurable.
- Guideline 23: keep it simple, explicit, and measurable.
- Guideline 24: keep it simple, explicit, and measurable.
- Guideline 25: keep it simple, explicit, and measurable.

### Incident Response

- Guideline 1: keep it simple, explicit, and measurable.
- Guideline 2: keep it simple, explicit, and measurable.
- Guideline 3: keep it simple, explicit, and measurable.
- Guideline 4: keep it simple, explicit, and measurable.
- Guideline 5: keep it simple, explicit, and measurable.
- Guideline 6: keep it simple, explicit, and measurable.
- Guideline 7: keep it simple, explicit, and measurable.
- Guideline 8: keep it simple, explicit, and measurable.
- Guideline 9: keep it simple, explicit, and measurable.
- Guideline 10: keep it simple, explicit, and measurable.
- Guideline 11: keep it simple, explicit, and measurable.
- Guideline 12: keep it simple, explicit, and measurable.
- Guideline 13: keep it simple, explicit, and measurable.
- Guideline 14: keep it simple, explicit, and measurable.
- Guideline 15: keep it simple, explicit, and measurable.
- Guideline 16: keep it simple, explicit, and measurable.
- Guideline 17: keep it simple, explicit, and measurable.
- Guideline 18: keep it simple, explicit, and measurable.
- Guideline 19: keep it simple, explicit, and measurable.
- Guideline 20: keep it simple, explicit, and measurable.
- Guideline 21: keep it simple, explicit, and measurable.
- Guideline 22: keep it simple, explicit, and measurable.
- Guideline 23: keep it simple, explicit, and measurable.
- Guideline 24: keep it simple, explicit, and measurable.
- Guideline 25: keep it simple, explicit, and measurable.

---

## Contact

<p align="center">
  <a href="mailto:thongnguyenslife@gmail.com">
    <img src="https://img.shields.io/badge/Email-thongnguyenslife%40gmail.com-1a73e8?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/LinkedIn-Coming%20Soon-0b1021?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn placeholder">
  <img src="https://img.shields.io/badge/Portfolio-Coming%20Soon-0b1021?style=for-the-badge&logo=aboutdotme&logoColor=white" alt="Portfolio placeholder">
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=140&color=0:6c63ff,100:1a73e8&section=footer&animation=fadeIn" alt="Footer">
</p>
