<!--
README "BIG-TECH" - Tieng Viet khong dau + comment giai thich.
NGUYEN TAC:
- Chi EMAIL co the click. Khong boc <a> cho anh/badge khac.
- Noi dung uu tien ro rang, impact, SLO, observability, security.
- Anh/SVG dong chi hien thi, KHONG la link.
-->

<!-- ======================= HERO / BANNER =======================
Anh mo dau tong trung tinh, chuyen nghiep. Co the doi URL anh cua ban.
-->
<p align="center">
  <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?w=1600&q=80" alt="Hero Banner" width="100%"/>
</p>

<!-- Tieu de + tagline ngan gon theo phong cach enterprise -->
<h1 align="center">Thong Nguyen</h1>
<p align="center"><em>Software Engineer · AI/ML · Systems</em></p>

<!-- ======================= STATUS / BADGES =======================
Chi la anh (khong boc link). Muc dich: mo ta pham vi va nguyen tac lam viec.
-->
<p align="center">
  <img src="https://komarev.com/ghpvc/?username=thongnguyenslife&style=for-the-badge&color=2F80ED" alt="Profile Views"/>
  <img src="https://img.shields.io/badge/Scope-Backend%20%7C%20AI%2FML%20%7C%20Cloud-111111?style=for-the-badge" alt="Scope"/>
  <img src="https://img.shields.io/badge/Principles-Clarity%20-%20Reliability%20-%20Impact-111111?style=for-the-badge" alt="Principles"/>
</p>

---

<!-- Tom luoc dinh vi nghe nghiep: 4-5 cau, trong tam ro rang -->
## Ho so Tong quan

Ky su tap trung xay dung he thong phan mem/ML **reliable, scalable, observable**. Uu tien hop dong ro rang, ket qua do duoc, va trai nghiem dev tot. Hien dang hoc tai **Ton Duc Thang University**; xay dung san pham can bang giua **toc do** va **chat luong**, nhan manh tinh de duy tri va tac dong lau dai.

---

<!-- Ban do nang luc kieu "big-tech": doc luot, hieu sau -->
## Ban do Nang luc

<table>
<tr>
  <td><b>Backend & APIs</b></td>
  <td>FastAPI/Express, domain modeling, idempotency, consistency, rate limiting</td>
</tr>
<tr>
  <td><b>AI / ML</b></td>
  <td>scikit-learn, TensorFlow, PyTorch, feature engineering, danh gia & error analysis</td>
</tr>
<tr>
  <td><b>Data & Pipelines</b></td>
  <td>Airflow DAGs, ETL/ELT, data validation, versioned datasets/artifacts, reproducibility</td>
</tr>
<tr>
  <td><b>MLOps</b></td>
  <td>Packaging/serving, A/B & shadow deploys, monitoring (latency/quality/drift), safe rollbacks</td>
</tr>
<tr>
  <td><b>DevOps</b></td>
  <td>Docker, Linux, CI/CD (GitHub Actions), observability (logs/metrics/traces)</td>
</tr>
<tr>
  <td><b>Frontend</b></td>
  <td>React, Vite, Tailwind, accessibility & SEO co ban</td>
</tr>
</table>

---

<!-- Nguyen tac van hanh: ngan, sac, co the ap dung ngay -->
## Nguyen tac Van hanh

- **Design for clarity** -> module nho, de ket hop; interface ro rang  
- **Prove with tests** -> unit + contract tests cho duong dan quan trong  
- **Measure truoc khi toi uu** -> profile hotspots; theo doi p95/p99; error budgets  
- **Tu dong hoa tac vu lap lai** -> build reproducible; one-click deploy; jobs dinh ky  
- **Ghi nhat ky quyet dinh** -> ADR ngan; lam ro trade-off

---

<!-- Tech Radar dang icon: nhan dien nhanh. Chi anh, khong link -->
## Tech Radar (icon)

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,js,ts,react,nodejs,express,fastapi,tailwind,postgres,mysql,redis,sklearn,tensorflow,pytorch,airflow,docker,linux,git,githubactions,kubernetes" alt="Tech Radar"/>
</p>

---

<!-- Diem nhan tac dong. Dien so thuc te khi co de tang do tin cay -->
## Impact Noi bat

- Giam p95 latency dich vu **[dien: %]** nho caching va rut gon payload  
- Tang task completion NLP **[dien: %]** nho labeling & fallback ro rang  
- Giam thoi gian CI **[dien: %]** nho incremental builds va tai su dung artifacts  
- Tang ti le thanh cong DAG len **[dien: %]** nho schema checks va canh bao

> Thay gia tri trong [dien: ...] bang so lieu that khi co.

---

<!-- Du an tieu bieu: mo ta ro vai tro & ky thuat, khong link ngoai -->
## Du an Tieu bieu

- **AI Chatbot (NLP)** — Transformers + FastAPI; intent classification; confidence thresholds; fallback an toan; iteration dua tren telemetry  
- **Personal Portfolio** — React + Vite + Tailwind; toi uu TTFB/Core Web Vitals; HTML sematic; pattern truy cap tot  
- **Data Science Pipeline** — Airflow ETL -> feature store -> training -> evaluation; du lieu & artifacts co version; bao cao tu dong

<details>
  <summary><b>Case Study - Chatbot Quality</b></summary>
  - Nhieu hon do chinh xac: label & threshold chac hon  
  - Latency p95 thap hon: mo hinh nhe + cache  
  - Ty le hoan thanh cao hon: fallback ro rang
</details>

<details>
  <summary><b>Case Study - Pipeline Reliability</b></summary>
  - Chan schema drift & nulls  
  - Chay reproducible voi pinned dependencies  
  - Bao cao dinh ky kem bieu do xu huong
</details>

---

<!-- Phan "big-tech": SLO & Observability -->
## SLO & Observability

- **Availability SLO:** [dien: 99.9% / 99.95%] uptime  
- **Latency SLO:** [dien: p95 <= XXX ms] cho cac endpoint chinh  
- **Error budget:** [dien: %] moi 30 ngay  
- **Dashboards:** latency, throughput, errors; review hang tuan kem action items

---

<!-- Phan "big-tech": Security & Privacy -->
## Security & Privacy

- Nguyen tac Least Privilege; quan ly secrets; rotation token  
- Valid input; model serving an toan; che PII trong logs  
- Audit dependencies; nhan thuc SBOM; nhip update ban va patch

---

<!-- So lieu hoat dong GitHub: anh SVG dong. KHONG boc link -->
## Activity & Metrics

<p align="center">
  <img height="158" src="https://github-readme-stats.vercel.app/api?username=thongnguyenslife&show_icons=true&theme=graywhite&hide_border=true" alt="GitHub Stats"/>
  <img height="158" src="https://streak-stats.demolab.com?user=thongnguyenslife&theme=default&hide_border=true" alt="Streak"/>
</p>
<p align="center">
  <img height="158" src="https://github-readme-stats.vercel.app/api/top-langs/?username=thongnguyenslife&layout=compact&theme=graywhite&hide_border=true" alt="Top Languages"/>
</p>
<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=thongnguyenslife&theme=flat&no-frame=true&margin-w=8" alt="Trophies"/>
</p>

---

<!-- Lo trinh: the hien ky luat & dinh huong nghe nghiep -->
## Muc tieu 2025

- [ ] Cong khai 2 demo ML kem docs & tests  
- [ ] Xuat ban benchmark latency/throughput  
- [ ] Mo nguon mot thu vien utils nho  
- [ ] Viet 3 ghi chu ky thuat ngan gon

---

<!-- Chi EMAIL co the click; phan khac la placeholder anh, khong link -->
## Lien he

<p align="center">
  <a href="mailto:thongnguyenslife@gmail.com">
    <img src="https://img.shields.io/badge/Email-thongnguyenslife%40gmail.com-2F80ED?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/LinkedIn-Coming%20Soon-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn (placeholder)"/>
  <img src="https://img.shields.io/badge/Portfolio-Coming%20Soon-111111?style=for-the-badge&logo=aboutdotme&logoColor=white" alt="Portfolio (placeholder)"/>
</p>

---

<!-- Chan trang toi gian -->
<p align="center"><sub>Engineered with care - Thong Nguyen</sub></p>
