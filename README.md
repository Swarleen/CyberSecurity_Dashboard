# 🛡️ Cybersecurity Incident Tracker
### An end-to-end Power BI analytics project by [Swarleen Bhamra](https://www.swarleen.com)

[![Live Dashboard](https://img.shields.io/badge/View%20Live%20Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://app.powerbi.com/view?r=eyJrIjoiMDgyNTA5NmYtOGU3OC00ZTMzLTk2ZGItNDVkYTBhNGFlYTk1IiwidCI6IjMyMWIxNDA4LTIxZjAtNDE0My1hMzkwLTNiNjIwMmU2NWUxZiJ9&pageName=0700ccdab041b1267d16)
[![Portfolio](https://img.shields.io/badge/swarleen.com-1B3A6B?style=for-the-badge)](https://www.swarleen.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/swarleenbhamra/)

---

## The Project

This dashboard simulates the kind of analytics capability a Security Operations Centre or Technology team would use to monitor, triage, and report on cybersecurity incidents across an enterprise.

The goal was to take raw, unstructured incident data and turn it into something a non-technical executive could act on — identifying where the organisation is most exposed, where response is falling short, and where control investments should go next.

> 🔗 **[Explore the live interactive dashboard here 🚀](https://app.powerbi.com/view?r=eyJrIjoiMDgyNTA5NmYtOGU3OC00ZTMzLTk2ZGItNDVkYTBhNGFlYTk1IiwidCI6IjMyMWIxNDA4LTIxZjAtNDE0My1hMzkwLTNiNjIwMmU2NWUxZiJ9&pageName=0700ccdab041b1267d16)**

[![Watch the demo](QAGIF.gif)](https://app.powerbi.com/view?r=eyJrIjoiMDgyNTA5NmYtOGU3OC00ZTMzLTk2ZGItNDVkYTBhNGFlYTk1IiwidCI6IjMyMWIxNDA4LTIxZjAtNDE0My1hMzkwLTNiNjIwMmU2NWUxZiJ9&pageName=0700ccdab041b1267d16)
> Click the image above to open the live dashboard!

---

## The Data

**200 cybersecurity incidents · 18 dimensions · January 2024 – April 2025**

The dataset covers every dimension needed for meaningful security analytics:

- **What happened** — incident type, attack vector, root cause
- **How bad** — severity (Critical / High / Medium / Low), financial impact in CAD
- **Who was affected** — department, region
- **How fast did we respond** — time to detect, time to resolve, SLA met or breached
- **Why did it happen** — control gap identified, recurrence flag
- **What are the consequences** — regulatory reportable, resolution team

A dedicated Date Table was built and related to the incident data to enable full time intelligence — month-over-month trends, MTD calculations, and period comparisons.

---

## What Was Built

### Data Modelling
Structured a relational data model connecting the incident dataset to a custom Date Table via a Many-to-One relationship on the reported date field. All columns typed and validated before any measures were written.

### DAX Measures — 20+ custom calculations
Built a dedicated measures table covering four domains:

**Volume & Status** — total incidents, open incidents, critical count, resolved count, recurring incidents, regulatory reportable count

**SLA & Response Performance** — SLA met count, SLA met %, SLA breached %, average time to detect, average time to resolve — all breakable by severity, department, region, and time period

**Financial Impact** — total financial impact, average impact per incident, critical-tier financial exposure

**Time Intelligence** — incidents month-to-date, incidents previous month, month-over-month change % — powered by DAX time intelligence functions against the Date Table

### Dashboard Design
Single-page layout on a dark navy canvas — designed to feel like a real operational tool, not a classroom exercise.

**7 visuals working together:**
- 5 KPI cards — instant read of the organisation's security posture
- Line chart — incident trend over time with Critical overlay
- Donut chart — severity distribution
- Stacked bar — SLA performance by severity tier
- Two clustered bars — incident types and attack vectors ranked by frequency
- Matrix heatmap — department × severity with conditional colour gradient, showing where risk concentrates

All visuals are cross-filtered — every slicer selection (date range, region) updates every visual simultaneously.

---

## Key Insights

**1. MFA gaps are the #1 driver of Critical incidents**
Cross-referencing control gaps against severity reveals that MFA Not Enforced appears disproportionately in Critical-tier incidents. This is the single highest-priority remediation the data supports — a targeted investment with outsized risk reduction.

**2. SLA performance breaks down at Medium severity**
Critical and High incidents generally hit SLA thresholds — escalation workflows kick in. Medium severity incidents show the highest SLA breach rate, suggesting triage deprioritises them until they become something worse.

**3. Phishing remains the dominant attack vector despite being the most well-known threat**
Email is still the #1 entry point. This isn't a technology gap — it's a training and awareness gap. The data points to sustained investment in security culture over additional tooling.

**4. Finance and IT carry concentrated Critical exposure**
The department heatmap shows Finance and IT with the highest density of Critical and High incidents — consistent with real-world targeting patterns where data value and system access make these departments primary targets.

**5. 25% of incidents are recurrences — remediation isn't sticking**
A recurrence rate at this level signals that fixes are treating symptoms not causes. Patch management delays and excessive privilege assignments appear most frequently in recurring incidents — both are process failures, not technical ones.

**6. Critical incidents are ~10% of volume but dominate financial impact**
The financial impact distribution is heavily skewed toward the Critical tier. This validates severity-based resource allocation and makes a clear business case for investing in faster detection at the top of the severity pyramid.

**7. Third-party attack vectors are underweighted in most security programmes**
Third Party appears consistently across incident types but rarely features in control gap discussions. The data suggests vendor risk management deserves more attention than it typically receives.

---

## Tools & Technologies

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-1B3A6B?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

---

## About

**Swarleen Bhamra** — Business Analyst & Data Analyst based in Toronto, ON.

I build analytics solutions that turn complex data into decisions — across cybersecurity, HR, and business operations domains.

- 🌐 [swarleen.com](https://www.swarleen.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/swarleenbhamra/)
- 📊 [Power BI Portfolio](https://github.com/Swarleen/PowerBI-Portfolio)

> Open to Business Analyst, Data Analyst, and Technology Analytics roles in Toronto.

---

*Dataset is fictional and created for portfolio demonstration purposes only.*
