# Awesome-Role-Based-Executive-Dashboards

# Awesome Role-Based Executive Dashboards

> A curated list of top Role-Based Executive Dashboard platforms — both SaaS/Hosted commercial BI solutions and open-source alternatives for delivering tailored KPI views to executives, managers, and operational teams.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Tableau Cloud](#tableau-cloud)
  - [Microsoft Power BI](#microsoft-power-bi)
  - [Looker](#looker)
  - [Domo](#domo)
  - [Klipfolio](#klipfolio)
  - [Sisense](#sisense)
  - [Geckoboard](#geckoboard)
  - [Databox](#databox)
  - [GoodData](#gooddata)
- [Open-Source Software](#-open-source-software)
  - [Apache Superset](#apache-superset)
  - [Metabase](#metabase)
  - [Lightdash](#lightdash)
  - [Redash](#redash)
  - [Helical Insight](#helical-insight)
  - [Orrery](#orrery)
  - [DataRoom](#dataroom)
  - [Blazer](#blazer)
  - [Shaper](#shaper)
  - [Enterprise Automation Platform](#enterprise-automation-platform)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Role-Based Executive Dashboard platforms. These are not open-source but are included as reference points for feature comparison.

### Tableau Cloud
**Type:** Enterprise visual analytics with role-aware content delivery  
Tableau is the long-standing standard for visual data exploration, with dashboards that can be published to specific user groups and filtered by role. Its strength is the depth of visual storytelling and the ability to tailor views for different audiences through user filters and row-level security. Pricing scales per-user, with creator and viewer license tiers.

### Microsoft Power BI
**Type:** Business analytics with row-level security and workspace roles  
Power BI provides strong role-based access through workspace roles (Admin, Member, Contributor, Viewer) and row-level security (RLS) defined in DAX. It is the natural choice for Microsoft-centric organizations, with the easiest adoption curve for existing Excel users. Executive dashboards can be distributed via apps with audience-specific permissions.

### Looker
**Type:** Governed metrics with role-based access and embedded dashboards  
Looker is built around LookML, a proprietary modeling language that gives enterprises one modeled source of truth. Role-based access is enforced through user attributes and access filters, allowing executives to see aggregated metrics while operational teams see granular data. It is the natural choice for Google Cloud shops with mature governance requirements.

### Domo
**Type:** Cloud BI with role-based app distribution  
Domo combines BI with data integration, app development, and collaboration. Dashboards and apps can be distributed to specific roles with granular permissions, making it suitable for organizations wanting an all-in-one platform for executive and operational reporting.

### Klipfolio
**Type:** KPI dashboards with user-level sharing controls  
Klipfolio focuses on real-time KPI dashboards that can be shared with specific users or groups. It is positioned for teams wanting a lightweight, focused dashboard tool rather than a full BI platform, with role-based sharing and embedding capabilities.

### Sisense
**Type:** Embedded analytics with role-based access  
Sisense specializes in embedded analytics, allowing product teams to embed dashboards with role-based access directly into their applications. It is often evaluated by SaaS companies needing white-labeled executive dashboards for their customers.

### Geckoboard
**Type:** Real-time KPI dashboards for team visibility  
Geckoboard provides real-time dashboards designed for office TVs, pulling from various data sources. While not deeply role-based, it is commonly used to keep executive and team KPIs visible across the organization.

### Databox
**Type:** Business dashboard and reporting with user permissions  
Databox connects to hundreds of data sources to build customizable dashboards. It supports user roles and permissions for controlling who can view and edit dashboards, making it suitable for distributing executive reports across teams.

### GoodData
**Type:** Enterprise BI with multi-tenant and role-based analytics  
GoodData provides enterprise BI with strong multi-tenancy and role-based access controls, making it suitable for embedding analytics into SaaS products where different customers and user roles see different data.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Role-Based Executive Dashboard tools. The open-source ecosystem spans **full BI platforms with row-level security**, **code-defined dashboards**, and **enterprise dashboard applications with RBAC**.

### Apache Superset
**Stack:** Python / Flask / React | **License:** Apache-2.0  
Apache Superset is the most widely adopted open-source BI platform, with 40+ visualization types and native connectors to major warehouses [citation:8][citation:14]. Role-based access is enforced through roles and permissions, with the ability to define row-level security rules for datasets, ensuring executives and operational users see appropriate data. The chart-builder UI is no-code, making it accessible to non-technical users once datasets are configured. **Trade-off:** Heavy operational footprint (Flask, metadata DB, Redis, Celery workers) requiring DevOps capacity [citation:14].  
**Best for:** Organizations wanting the broadest open-source BI platform with robust role-based access and a proven track record, accepting significant operational overhead.

### Metabase
**Stack:** Clojure / Java | **License:** AGPL-3.0 (Open Source)  
Metabase is the best first BI tool for most teams, with a question builder that gets a non-analyst to a working dashboard quickly [citation:14]. Role-based access is managed through groups and permissions, with **row-level permissions sandboxing** available in the Pro/Enterprise tier (not the open-source edition). The open-source edition provides basic user groups and collection permissions. Metabase's AI features (Metabot) are included in every version, including open-source [citation:11]. **Trade-off:** Advanced governance features like SSO and row-level sandboxing are commercial, and a disciplined patch schedule is required (CVE history) [citation:14].  
**Best for:** Small to mid-sized teams wanting a lightweight, user-friendly BI tool with fast time-to-value, accepting that advanced role-based data isolation requires the paid tier.

### Lightdash
**Stack:** TypeScript / Node.js | **License:** MIT (core) / Source-available (EE)  
Lightdash is the BI platform built for dbt, with metrics defined in YAML alongside dbt models [citation:4][citation:14]. Role-based access is managed through organization roles and project-level permissions, with **row-level security** available in the Enterprise edition. The point-and-click explorer lets business users combine pre-defined metrics without SQL, and an AI analyst co-pilot answers questions grounded in the semantic layer [citation:4]. **Trade-off:** Requires an existing dbt project; SSO and advanced permissions are gated to Enterprise [citation:4][citation:14].  
**Best for:** dbt shops wanting governed metrics with role-based access and an open-source Looker alternative, accepting the dbt dependency.

### Redash
**Stack:** Python / React | **License:** BSD-2-Clause  
Redash focuses on the query-writing experience and dashboards, with a narrower feature set than Superset or Metabase that makes it simpler and lighter to self-host [citation:4][citation:14]. Role-based access includes user groups and permission controls for queries and dashboards. **Critical caveat:** Redash was acquired by Databricks and shut down in November 2021; community forks exist but the original project is effectively frozen [citation:4].  
**Best for:** Teams already running Redash where migration cost decides, or those wanting a lightweight SQL-first dashboard tool and willing to accept maintenance risk.

### Helical Insight
**Stack:** Java / React | **License:** Open Source (per project)  
Helical Insight is an open-source BI platform with a comprehensive connector library and comparisons against Superset, Metabase, and Redash [citation:6]. It supports row-level security, embedding, SSO, and AI features (Instant BI), positioning itself as a full-stack alternative for organizations wanting reporting and dashboarding in one platform. Deployment via Docker Compose is documented for zero-configuration startup [citation:6].  
**Best for:** Organizations wanting a full-featured open-source BI platform with built-in reporting and row-level security, accepting a heavier Java-based stack.

### Orrery
**Stack:** TypeScript / Node.js | **License:** Open Source (npm)  
Orrery is an open-source, code-defined BI dashboard tool where dashboards are defined in `.board` files rather than clicks [citation:2]. It supports parameters (date ranges, selects, toggles) and connects to PostgreSQL, MySQL, SQLite, and DuckDB. Dashboards can be exported as static HTML. While not explicitly role-based, the code-defined approach allows different dashboard files to be deployed for different audiences, and static exports can be distributed selectively.  
**Best for:** Developers wanting dashboards-as-code with version control and static export capabilities, accepting that role-based access must be handled externally.

### DataRoom
**Stack:** SpringBoot / Vue / ECharts | **License:** Open Source  
DataRoom is an open-source large-screen dashboard designer with 80+ visualization components, supporting MySQL, PostgreSQL, Oracle, ClickHouse, and more [citation:9]. It includes **custom interface permissions and data permissions**, with integration for Shiro/Security authentication frameworks, making it suitable for building role-specific executive command centers. Deploys independently or embedded into existing Java Web projects [citation:9].  
**Best for:** Organizations wanting a visual, drag-and-drop dashboard designer with data-level permissions for executive command centers, particularly in Java-centric environments.

### Blazer
**Stack:** Ruby / PostgreSQL | **License:** MIT  
Blazer is a lightweight, self-hosted SQL business intelligence tool for exploring data, building charts and dashboards, and setting up data checks that alert on unexpected changes [citation:12]. It has **no built-in authentication**, so role-based access must be provided by a fronting proxy (e.g., nginx Basic Auth) or external authentication layer. Best suited for internal reporting where access control is handled at the infrastructure level.  
**Best for:** Small teams wanting a minimal SQL-first dashboard tool with alerting, accepting that authentication and role management must be handled externally.

### Shaper
**Stack:** Go / React / DuckDB | **License:** MPL-2.0  
Shaper is an open-source, SQL-first dashboard and reporting tool powered by DuckDB, with **row-level security via JWT tokens** and white-label embedding . It supports automated PDF/PNG/CSV/Excel reports, scheduled alerts, and password-protected shareable links. The JWT-based RLS allows different users to see different rows based on their token claims, enabling role-specific executive views. Deploys via Docker.  
**Best for:** Teams wanting SQL-driven dashboards with JWT-based row-level security and embedding capabilities, accepting a younger ecosystem than Superset or Metabase.

### Enterprise Automation Platform
**Stack:** Python / Streamlit / FastAPI / PostgreSQL | **License:** Open Source  
A reference implementation of an enterprise automation platform with **role-based dashboards for Admin, User, and Approver roles**, executive KPI dashboards (Orders, Revenue, SLA/SLO), approval workflows with role enforcement, JWT authentication with RBAC, and full audit logging [citation:1]. The architecture uses Streamlit for UI, FastAPI for the backend, and PostgreSQL for storage. Deploys locally with demo credentials for each role [citation:1].  
**Best for:** Developers wanting a working reference implementation of role-based executive dashboards with approval workflows and audit logging, rather than a full BI platform.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Role-Based Access | Row-Level Security | Self-Hosted | Best For |
|----------|---------|-------|-------------------|---------------------|-------------|----------|
| **Tableau** | Proprietary | Cloud | ✅ | ✅ | ❌ | Visual storytelling at scale |
| **Power BI** | Proprietary | Cloud | ✅ Workspace roles | ✅ DAX RLS | ❌ | Microsoft/Excel shops |
| **Looker** | Proprietary | Cloud | ✅ | ✅ Access filters | ❌ | Governed metrics at scale |
| **Apache Superset** | Apache-2.0 | Python/React | ✅ Roles + permissions | ✅ Dataset RLS | ✅ | Broad OSS BI with RLS |
| **Metabase** | AGPL-3.0 | Clojure/Java | ✅ Groups | (Pro/Enterprise) | ✅ | Fast time-to-value |
| **Lightdash** | MIT (core) | TypeScript | ✅ Org/project roles | (Enterprise) | ✅ | dbt-native governed metrics |
| **Helical Insight** | Open Source | Java/React | ✅ | ✅ | ✅ | Full reporting + RLS |
| **DataRoom** | Open Source | SpringBoot/Vue | ✅ Shiro/Security | ✅ Data permissions | ✅ | Visual command centers |
| **Shaper** | MPL-2.0 | Go/React/DuckDB | ✅ JWT claims | ✅ JWT-based | ✅ | SQL + JWT RLS + embedding |
| **Enterprise Automation Platform** | Open Source | Streamlit/FastAPI | ✅ Admin/User/Approver | (Role-scoped) | ✅ | Reference RBAC implementation |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Role-Based Executive Dashboard tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem **splits** between **full BI platforms with row-level security** (Apache Superset, Helical Insight, Shaper), **dbt-native governed metrics** (Lightdash), **visual command center designers** (DataRoom), and **reference RBAC implementations** (Enterprise Automation Platform). **Apache Superset** is the most mature choice for role-based executive dashboards with dataset-level row-level security, though it demands operational capacity [citation:14]. **Metabase** offers the fastest path for smaller teams but gates row-level sandboxing to its paid tier [citation:14]. **Shaper** is notable for JWT-based row-level security, enabling role-specific views without complex permission configuration . For teams wanting a working RBAC reference with Admin/Approver/User dashboards, the Enterprise Automation Platform provides a concrete starting point [citation:1].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
