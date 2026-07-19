<div align="center">

<img
src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=280&section=header&text=Jaya+Surya&fontSize=70&fontColor=C9A7FF&animation=fadeIn"/>

<p align="center">
  <img
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&pause=1000&color=A78BFA&center=true&vCenter=true&repeat=true&width=900&lines=Data+Engineer+%40+Virtusa;Building+Scalable+Lakehouse+Architectures;PySpark+%7C+Databricks+%7C+AWS+%7C+Delta+Lake;Turning+Raw+Data+Into+Business+Intelligence"
    alt="Typing SVG"
  />
</p>

<br/>

![Databricks Certified](https://img.shields.io/badge/Databricks-Data%20Engineer%20Associate-8A2BE2?style=for-the-badge&logo=databricks&logoColor=white)
![Spark Certified](https://img.shields.io/badge/Databricks-Apache%20Spark%20Developer-7C3AED?style=for-the-badge&logo=apachespark&logoColor=white)
![AWS Certified](https://img.shields.io/badge/AWS-Data%20Engineer%20Associate-6D28D9?style=for-the-badge&logo=amazonaws&logoColor=white)

![Location](https://img.shields.io/badge/📍-Hyderabad,_India-5B21B6?style=flat-square)

<br/>

<a href="https://jayasuryapuralasetti.online">
  <img src="https://img.shields.io/badge/Portfolio-9333EA?style=for-the-badge&logo=vercel&logoColor=white" />
</a>
<a href="https://www.linkedin.com/in/jaya-surya-puralasetti">
  <img src="https://img.shields.io/badge/LinkedIn-7C3AED?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>
<a href="mailto:jayasuryapuralasetti@gmail.com">
  <img src="https://img.shields.io/badge/Email-6D28D9?style=for-the-badge&logo=gmail&logoColor=white" />
</a>
<a href="https://github.com/Jayasurya-2">
  <img src="https://img.shields.io/badge/GitHub-4C1D95?style=for-the-badge&logo=github&logoColor=white" />
</a>

<br/><br/>

![Profile Views](https://komarev.com/ghpvc/?username=Jayasurya-2&style=flat-square&color=8b5cf6&label=Profile+Views)
![Followers](https://img.shields.io/github/followers/Jayasurya-2?style=flat-square&color=a78bfa&label=Followers)
![Stars](https://img.shields.io/github/stars/Jayasurya-2?style=flat-square&color=7c3aed&label=Stars)

</div>

---

## 🟣 About Me

```yaml
Name: Jayasurya
Role: Data Engineer @ Virtusa
Location: Hyderabad, India
Focus: Lakehouse Architecture · Distributed Data Processing · Cloud Data Engineering
```

I'm a **Data Engineer** specializing in building production-grade **Lakehouse architectures** on **Databricks**, with hands-on expertise across the **Medallion Architecture (Bronze → Silver → Gold)**, distributed data processing with **PySpark**, and cloud-native data pipelines on **AWS**. My engineering approach centers on rigorous data quality practices — incremental ingestion, watermarking, and Delta MERGE logic — paired with a focus on delivering clean, analytics-ready data at scale.

I bring an end-to-end pipeline mindset to every project: designing DAG-driven orchestration, automating multi-layer pipeline execution, and writing thorough technical documentation that holds up under real engineering scrutiny.

**🎯 Open To:**

- Data Engineering roles at product-based companies (India & International)
- Cloud & Lakehouse Architecture opportunities
- Collaborative open-source data engineering projects

---

## 🟣 Tech Stack

**Languages**

<img src="https://skillicons.dev/icons?i=python,mysql&theme=dark" />

**Data & Lakehouse**

![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta_Lake-00ADD8?style=flat-square)
![Unity Catalog](https://img.shields.io/badge/Unity_Catalog-8A2BE2?style=flat-square)

**Cloud & Version Control**

<img src="https://skillicons.dev/icons?i=aws,git,github&theme=dark" />

---

## 🟣 Featured Projects

<details>
<summary><b>🛒 E-Commerce Analytics Lakehouse</b></summary>
<br/>

End-to-end **Lakehouse platform** built on **Databricks** under Unity Catalog, processing six interconnected e-commerce datasets — events, orders, order items, products, reviews, and users — through a complete **Bronze → Silver → Gold Medallion Architecture**.

| Attribute | Details |
|---|---|
| **Stack** | PySpark, Databricks, Delta Lake, Unity Catalog, Auto Loader |
| **Scale** | 567,500+ rows across 6 source datasets |
| **Performance** | Incremental Auto Loader ingestion with checkpoint-based recovery |
| **Security** | Unity Catalog governed namespace (`cap_pro_2`) with layer-level access control |
| **Impact** | Executive KPI dashboard, RFM segmentation, cohort retention, customer 360 view |
| **Repository** | [View Repository](https://github.com/Jayasurya-2/E-Commerce-Analytics-Lakehouse) |

**Architecture Highlights:**
- **Bronze Layer:** Incremental ingestion via Auto Loader with dedicated checkpoint directories per source
- **Silver Layer:** Watermark control tables tracking `_ingest_timestamp` per entity; Delta MERGE (`WHEN MATCHED` / `WHEN NOT MATCHED`) logic across all six entities using business keys, with identified data quality bugs (typos, broken fillna logic, subtotal miscalculations) resolved
- **Gold Layer:** Eight analytical notebooks covering RFM segmentation, cohort retention, revenue analytics, customer 360, product performance, and an executive KPI dashboard
- **Orchestration:** Custom four-level DAG (Setup → 6 parallel Bronze jobs → 6 parallel Silver jobs → sequential Gold) built on Databricks Jobs, deliberately avoiding Delta Live Tables to eliminate surcharge overhead
- **Documentation:** 20+ section technical documentation with architecture diagrams and per-layer pipeline breakdowns

</details>

<details>
<summary><b>📡 IoT Sensor Data Pipeline</b></summary>
<br/>

Real-time-style **IoT telemetry pipeline** simulating 10 connected devices over 60 days of sensor data, engineered with a quarantine-based data quality strategy and full Medallion Architecture.

| Attribute | Details |
|---|---|
| **Stack** | PySpark, Databricks, Delta Lake, Auto Loader |
| **Scale** | 10 simulated devices, 60 days of batch data across 3 CSV files |
| **Performance** | `trigger(availableNow=True)` batch-triggered incremental processing |
| **Security** | Silver-layer MERGE with dedicated quarantine routing for invalid records |
| **Impact** | 4 Gold-layer metric tables powering an 11-chart visualization notebook |
| **Repository** | [View Repository](https://github.com/Jayasurya-2/IoT-Sensor-Data-Pipeline) |

**Architecture Highlights:**
- **Bronze Layer:** Auto Loader ingestion into `iot_sensor.bronze`
- **Silver Layer:** MERGE logic with quarantine routing for malformed sensor readings into `iot_sensor.silver`
- **Gold Layer:** Four aggregated metric tables in `iot_sensor.gold` powering downstream analytics
- **Engineering Discipline:** Fixed a broken time-window filter by replacing it with Delta Lake's `VERSION AS OF` pattern for accurate per-run row isolation; entire codebase written functionally without `def` blocks by design
- **Visualization:** Dedicated notebook rendering 11 charts across device and metric dimensions

</details>

---

## 🟣 Experience

**Data Engineer** · **Virtusa**
`Hyderabad, India`

Engineering scalable data pipelines and Lakehouse architectures on Databricks, driving reliable data flows from raw ingestion through to business-ready analytics.

**Scope of Work:**
- Designing and implementing multi-layer (Bronze/Silver/Gold) data pipelines using PySpark and Delta Lake
- Building incremental ingestion frameworks with Auto Loader and checkpoint-based recovery
- Implementing Delta MERGE strategies with watermark tracking for reliable upserts
- Automating pipeline orchestration through Databricks Jobs and DAG design
- Producing comprehensive technical documentation for engineering handoff and audits

`PySpark` `Databricks` `Delta Lake` `Unity Catalog` `AWS` `SQL` `Data Pipeline Design`

---

## 🟣 Achievements

<div align="center">

| Recognition | Details |
|---|---|
| 🏆 Databricks Data Engineer Associate | Certified in end-to-end Lakehouse data engineering on Databricks |
| 🏆 Databricks Apache Spark Developer | Certified in distributed data processing with Apache Spark |
| 🏆 AWS Data Engineer Associate | Certified in cloud-native data engineering on AWS |
| 🏆 Production Lakehouse Delivery | Shipped two complete Medallion Architecture pipelines end-to-end, both live on GitHub |

</div>

---

## 🟣 Certifications

**AWS**

![AWS Data Engineer Associate](https://img.shields.io/badge/AWS-Data%20Engineer%20Associate-FF9900?style=flat-square&logo=amazonaws&logoColor=white)

**Databricks**

![Databricks Data Engineer Associate](https://img.shields.io/badge/Databricks-Data%20Engineer%20Associate-FF3621?style=flat-square&logo=databricks&logoColor=white) <br> <br>
![Databricks Apache Spark Developer](https://img.shields.io/badge/Databricks-Apache%20Spark%20Developer-FF3621?style=flat-square&logo=databricks&logoColor=white)

---

## 🟣 GitHub Analytics

<div align="center">

<!-- <img
src="https://github-readme-stats.vercel.app/api?username=Jayasurya-2&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github&count_private=true&include_all_commits=true"
width="49%"/> -->
<img src="https://streak-stats.demolab.com/?user=Jayasurya-2&theme=tokyonight&hide_border=true&background=0D1117&ring=8B5CF6&fire=A78BFA&currStreakLabel=A78BFA" width="49%" />

<br/>

<p align="center">
  <img height="165" src="https://github-readme-stats-sigma-five.vercel.app/api?username=Jayasurya-2&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" />
  <!-- <img height="165" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=Jayasurya-2&layout=compact&theme=tokyonight&hide_border=true&langs_count=6" /> -->
</p>

</div>

---

## 🟣 Contribution Activity

<div align="center">

<img
src="https://github-readme-activity-graph.vercel.app/graph?username=Jayasurya-2&theme=tokyo-night&hide_border=true"
width="100%"/>

</div>

---

## 🟣 Currently Learning

```yaml
building:
  - Production-grade Lakehouse architectures on Databricks
  - Automated, DAG-orchestrated Medallion pipelines

exploring:
  - AI/ML fundamentals, with a goal of applying them inside Data Engineering pipelines
  - Google Cloud Platform (GCE, GKE, Cloud Run, App Engine) alongside AWS and Databricks

open_to:
  - Data Engineering roles at product-based companies
  - International opportunities
```

---

## 🟣 Connect With Me

<div align="center">

<a href="https://jayasuryapuralasetti.online">
  <img src="https://img.shields.io/badge/Portfolio-9333EA?style=for-the-badge&logo=vercel&logoColor=white" />
</a>
<a href="https://www.linkedin.com/in/jaya-surya-puralasetti">
  <img src="https://img.shields.io/badge/LinkedIn-7C3AED?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>
<a href="mailto:jayasuryapuralasetti@gmail.com">
  <img src="https://img.shields.io/badge/Email-6D28D9?style=for-the-badge&logo=gmail&logoColor=white" />
</a>
<a href="https://github.com/Jayasurya-2">
  <img src="https://img.shields.io/badge/GitHub-4C1D95?style=for-the-badge&logo=github&logoColor=white" />
</a>

</div>

---

<div align="center">

*"Every pipeline tells a story — I make sure it's a clean one."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=150&section=footer" width="100%"/>

</div>
