<!--
  Professional Profile README — THONG NGUYEN HOANG
  Focus: Network Engineer · IT Help Desk · Cloud & Java
  Notes:
    - Replace links/IDs marked TODO if needed
    - Keep badges lightweight for fast load
-->

<!-- HERO -->
<h1 align="center">THONG NGUYEN HOANG</h1>
<p align="center"><b>Network Engineer · IT Help Desk · Cloud & Java</b></p>
<p align="center">
  <a href="mailto:thongnguyenslife@gmail.com">
    <img alt="Email" src="https://img.shields.io/badge/Email-thongnguyenslife%40gmail.com-blue?logo=gmail">
  </a>
  <a href="https://github.com/thongnguyenslife">
    <img alt="GitHub" src="https://img.shields.io/badge/GitHub-@thongnguyenslife-black?logo=github">
  </a>
  <!-- TODO: Add LinkedIn
  <a href="https://www.linkedin.com/in/your-id">
    <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-View_Profile-0A66C2?logo=linkedin">
  </a> -->
</p>
<p align="center"><i>Reliable networks. Clear runbooks. Practical automation.</i></p>

<!-- QUICK NAV -->
<p align="center">
  <a href="#about">About</a> ·
  <a href="#projects">Projects</a> ·
  <a href="#skills">Skills</a> ·
  <a href="#principles">Principles</a> ·
  <a href="#roadmap">Roadmap</a> ·
  <a href="#contact">Contact</a>
</p>

---

## <span id="about">About</span>

I build dependable network foundations, resolve end-user issues fast, and write small tools that remove toil. Currently deepening **cloud fundamentals** and using **Java** for ops tooling (diagnostics, checks, reporting).

- Interests: troubleshooting, incident hygiene, low-friction runbooks  
- Learning now: IAM basics, VPC/VNet patterns, secure-by-default  
- Work style: measure → automate → document

> **Operating belief:** Simple, observable systems fail less and recover faster.

---

### Highlights at a glance

`Networking` `Help Desk` `Cloud (Foundations)` `Java CLI` `Git` `Monitoring` `DNS/DHCP` `Routing/Switching` `Firewall Basics`

---

## <span id="projects">Signature Projects</span>

> Replace links with real repositories when ready.

<table>
  <tr>
    <td>
      <b>network-diagnose-cli (Java)</b><br/>
      One-command checks: ping · traceroute · DNS · HTTP; exports txt/md reports.<br/>
      <sub>Status: <b>WIP</b> · <a href="https://github.com/thongnguyenslife">Repo</a></sub>
    </td>
    <td>
      <b>helpdesk-kb-playbook</b><br/>
      Opinionated templates for intake → triage → fix/esc → post-incident notes.<br/>
      <sub>Status: <b>Draft</b> · <a href="https://github.com/thongnguyenslife">Repo</a></sub>
    </td>
  </tr>
  <tr>
    <td>
      <b>cloud-lab-notes</b><br/>
      Vendor-neutral notes: IAM, VPC/VNet, logging/monitoring, cost guardrails.<br/>
      <sub>Status: Updating · <a href="https://github.com/thongnguyenslife">Repo</a></sub>
    </td>
    <td>
      <b>endpoint-ops-scripts</b><br/>
      Small Bash/Java utilities for routine checks and onboarding/offboarding.<br/>
      <sub>Status: Planned · <a href="https://github.com/thongnguyenslife">Repo</a></sub>
    </td>
  </tr>
</table>

<details>
  <summary><b>Why these matter</b></summary>
  These projects turn repetitive troubleshooting into predictable, documented workflows and make incident recovery faster and less error-prone.
</details>

---

## <span id="skills">Skill Matrix</span>

| Area | Scope | Confidence |
|---|---|---|
| **Networking** | TCP/IP, VLANs, routing/switching, DNS/DHCP, basic firewalling, monitoring | ★★★★☆ |
| **IT Help Desk** | ticket lifecycle & SLA, endpoint support, asset onboarding/offboarding, KB | ★★★★☆ |
| **Cloud (Foundations)** | IAM principles, VPC/VNet, logging/monitoring, cost basics | ★★★☆☆ |
| **Java for Ops** | CLI utilities, HTTP/DNS checks, file/report generation | ★★★☆☆ |
| **Workflow** | Git, lightweight CI (lint/test), clear READMEs & runbooks | ★★★★☆ |

<sub>Legend: ★★★★★ expert · ★★★★☆ strong · ★★★☆☆ solid</sub>

---

## <span id="principles">Engineering Principles</span>

- **Standardize** — small checklists and a short rollback for every change.  
- **Observe** — minimal yet meaningful logs/metrics to see health at a glance.  
- **Share** — after tricky tickets, write a short KB (problem → root cause → fix → verify).  
- **Automate** — remove toil; keep scripts simple, auditable, and reversible.

> “If it isn’t documented, it didn’t happen. If it isn’t observable, it doesn’t exist.”

---

## <span id="roadmap">Learning Roadmap</span>

- Advanced network troubleshooting (captures & packet analysis) — **▰▰▰▱▱**  
- Java: testable modules, separate CLI/service, clean packaging — **▰▰▱▱▱**  
- Cloud: least-privilege IAM, network isolation, cost guardrails — **▰▰▰▱▱**

---

## Toolbelt

`Java` · `Bash` · `Git` · `TCP/IP` · `DNS/DHCP` · `Routing/Switching` · `Firewall Basics` · `Monitoring`

<details>
  <summary><b>Ops Snippets</b> (quick copy-paste)</summary>

```bash
# Quick HTTP check (returns status code)
curl -s -o /dev/null -w "%{http_code}\n" https://example.com
