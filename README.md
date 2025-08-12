<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:1a73e8,100:202124&text=THONG%20NGUYEN&fontAlign=50&fontAlignY=36&fontSize=54&desc=Cloud%20%26%20VPS%20·%20Network%20Engineer%20·%20IT%20Help%20Desk%20·%20Java&descAlignY=58&animation=fadeIn" alt="Header">
</p>

<h1 align="center">Readable. Reliable. Observable.</h1>
<p align="center"><em>I operate cloud/VPS at scale, support users with care, and ship Java services that last.</em></p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=thongnguyenslife&style=for-the-badge&color=1a73e8" alt="Profile Views">
  <img src="https://img.shields.io/badge/Focus-Cloud%20%7C%20VPS%20%7C%20SRE-202124?style=for-the-badge" alt="Focus">
  <img src="https://img.shields.io/badge/Principles-Readability%20%7C%20Reliability%20%7C%20Impact-202124?style=for-the-badge" alt="Principles">
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Inter&weight=700&size=18&pause=1300&center=true&vCenter=true&width=720&duration=3000&color=1a73e8&lines=First+principles.+Design+docs.+Measured+impact." alt="Typing accent">
</p>

---

## Executive Summary

<div align="justify">
I build and operate <b>cloud & VPS</b> infrastructure with first-principles engineering: <b>readability first</b>, strong <b>testing</b>, <b>SRE</b> operations (SLOs, error budgets), and <b>security-by-default</b>. I cover three tracks end-to-end: <b>Network Engineer</b> (IPv4/IPv6, routing, VLANs, ACLs), <b>IT Help Desk</b> (incident/request, SLA, KB), and <b>Java</b> back-end (Spring Boot, CI/CD). I ship fast without compromising long-term quality and user impact.
</div>

---

## Cloud & VPS Operations

- Providers & models: VPS and cloud (AWS, GCP, Azure; also DO/Linode/Vultr)  
- Provisioning: images & sizing, cloud-init, SSH keys, VPC/VNet, subnets, SG/NSG, static IP  
- OS baseline (Ubuntu LTS): non-root sudo user, SSH key-only, UFW, Fail2Ban, time sync, unattended upgrades  
- Reverse proxy & TLS: NGINX, HTTP→HTTPS redirect, HSTS, TLSv1.2+, Let’s Encrypt (certbot) renewals  
- Observability: logs/metrics/traces; Prometheus exporters, Grafana dashboards; p95/p99, saturation, SLO burn  
- Backups & DR: encrypted snapshots, DB dumps, restore drills; RPO/RTO targets  
- Cost & hygiene: tag everything, right-size, lifecycle policies, delete idle IP/volumes, budget alerts

---

## Network Engineering

- L2/L3: VLAN & trunking, STP/RSTP, inter-VLAN routing; OSPF/EIGRP, static routes, NAT; IPv6 (SLAAC/DHCPv6)  
- Security: ACLs, port security, 802.1X; site-to-site & remote-access VPN; basic firewalling  
- Monitoring: syslog, NetFlow/sFlow, SNMP; topology diagrams; backups & versioned configs  
- Targets: CCNA domains (network fundamentals, access, IP connectivity/services, security, automation)

---

## IT Help Desk (ITSM)

- Scope: incident vs request, SLA/priority matrix, escalation paths, clean handoffs  
- Playbooks: triage trees, account/password resets, endpoint hardening, patch cadence, KB curation  
- Experience: first-contact resolution, clear comms, CSAT loops into problem/change management  
- Tooling: Jira Service Management / Freshservice / ServiceDesk Plus; remote assist, inventory, alert routing

---

## Java Services (Spring Boot)

- API design: contracts, idempotency, pagination, validation; OpenAPI spec  
- Quality: JUnit/AssertJ, Testcontainers, integration tests, golden contract tests; CI with GitHub Actions  
- Data: JPA/Hibernate, PostgreSQL/MySQL; Redis caching; migrations with Flyway/Liquibase  
- Ops: Docker images, health/metrics (Micrometer), structured logs; config per env; canary & rollback runbooks

---

## Impact Highlights

- Reduced p95 API latency by **[fill: %]** via caching, connection pooling, lean payloads  
- Improved first-contact resolution by **[fill: %]** with triage playbooks and KB standardization  
- Cut CI build time by **[fill: %]** using incremental builds and artifact reuse  
- Increased change success to **[fill: %]** with pre-change checks and staged rollouts

> Replace bracketed values with real metrics when available.

---

## SRE: SLOs & Operations

- Availability SLO: **[fill: 99.9% / 99.95%]** uptime  
- Latency SLO: **[fill: p95 ≤ XXX ms]** for key endpoints; burn alerts and weekly review  
- Error budget: **[fill: %]** per 30 days; error-budget policies gate risky releases  
- Runbooks: incident triage, degrade modes (read-only, cached), one-command rollback

---

## Security & Privacy

Least-privilege access; secret rotation; input validation & output encoding; secure TLS defaults; PII redaction; CIS-aligned hardening; SBOM/dependency audits; patch cadence.

---

## Selected Work

**Cloud/VPS Baseline** — secure Ubuntu image, SSH keys, UFW + Fail2Ban, NGINX TLS, automated backups, Grafana dashboards  
**Help Desk Excellence** — incident/request templates, SLA & escalation matrix, “solve once, document forever” KB framework  
**Java API Template** — Spring Boot service (auth, DTO validation, pagination), health/metrics, OpenAPI, CI/CD with GitHub Actions

<details>
  <summary><b>Playbook · Provision a VPS</b></summary>
  Choose size/image → add SSH key → create sudo user → harden SSH → firewall → install NGINX + TLS → deploy app → configure backups & monitoring
</details>

<details>
  <summary><b>Runbook · TLS Renewal</b></summary>
  Check expiry → dry-run certbot → renew and reload → verify chain/ciphers → update HSTS if needed
</details>

<details>
  <summary><b>Case Study · Java API Reliability</b></summary>
  Contract tests + idempotency reduce retries; timeouts + circuit breakers shrink blast radius; observability improves MTTR
</details>

---

## Tools & Tech (icons)

<p align="center">
  <img src="https://skillicons.dev/icons?i=aws,gcp,azure,digitalocean,terraform,ansible,docker,kubernetes,nginx,linux,ubuntu,java,spring,gradle,maven,postgres,mysql,redis,grafana,prometheus,git,githubactions,wireguard" alt="Tools & Tech">
</p>

---

## Certifications (in progress / planned)

- **CCNA (200-301)** — network fundamentals, access, IP connectivity/services, security, automation  
- **CompTIA Network+** — implementation, operations, security, troubleshooting  
- **ITIL Foundation** — incident/request, service value system, continual improvement  
- **HashiCorp Terraform Associate** — IaC fundamentals, state/workspaces, modules, policies

---

## 2025 Goals

- Publish a hardened Cloud/VPS baseline with SLOs and dashboards  
- Ship a production-grade Java service with measurable error-budget policies  
- Standardize a help-desk KB and triage playbook; improve FCR% and CSAT  
- Earn one networking and one IaC certification

---

## Contact

<p align="center">
  <a href="mailto:thongnguyenslife@gmail.com">
    <img src="https://img.shields.io/badge/Email-thongnguyenslife%40gmail.com-1a73e8?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=140&color=0:202124,100:1a73e8&section=footer&animation=fadeIn" alt="Footer">
</p>
