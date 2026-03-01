# MNCH+N Facility Readiness Informatics Dashboard

## Overview
This project represents a full end-to-end health informatics pipeline, spanning digital field data collection to interactive analytic dashboard development. It was designed to assess, visualize, and interpret facility readiness for maternal, newborn, child health, and nutrition (MNCH+N) service delivery across **106 health facilities in 16 Local Government Areas (LGAs)** of Bauchi State, Nigeria. Implemented under the **EpiC (Meeting Targets and Maintaining Epidemic Control)** programme, funded by the U.S. Department of State in partnership with the Bauchi State Ministry of Health/Primary Health Care Board, the initiative demonstrates a rare example of applied health informatics in a resource-limited setting.  

The pipeline covered the complete data lifecycle: **instrument design → digital field collection → data cleaning and aggregation → interactive visualization**. This integrated approach replaced fragmented paper-based assessments with a structured, digital system that improved data quality, turnaround time, and usability.

---

## What Went Into the Work

### i. ODK Tool Design and Field Data Collection
- **XLSForm authoring** with skip logic, relevance conditions, and constraint validations to ensure data quality.  
- **Separate modules** for PHCs and Secondary Hospitals to reflect different service expectations.  
- **Binary and multi-select questions** structured around BEmONC/CEmONC signal functions, WHO nutrition commodity checklists, HRH adequacy standards, and infrastructure indicators.  
- Deployment via **ODK Central**, enabling real-time submissions from Android devices across 16 LGAs.  
- Built-in **IMSS (Integrated Maternal and Newborn Services Score)** logic to auto-compute composite readiness scores.  

Field teams assessed **90 PHCs and 16 secondary hospitals**, covering staffing, service availability, drugs, equipment, nutrition commodities, power infrastructure, and referral pathways. This digital approach reduced transcription errors, cut turnaround from weeks to days, and enabled real-time quality checks.

---

### ii. Data Processing and Aggregation
- Raw ODK submissions exported as structured files.  
- **Python-based pipeline** standardized facility names against the Bauchi State master list.  
- Binary indicators aggregated into domain-level percentages per facility and LGA.  
- IMSS composite scores computed and validated (mean: 71.7%, range: 46.0–90.4%).  
- Nutrition commodity availability, drug stockouts, equipment functionality, and HRH adequacy calculated at both PHC and secondary tiers.  
- Cleaned data embedded directly into the dashboard as JavaScript objects, enabling a **self-contained, offline-capable deployment**.

---

### iii. Dashboard Development
- Built in **vanilla HTML, CSS, and JavaScript** (no backend infrastructure required).  
- **Chart.js with DataLabels plugin** powers all visualizations: bar charts, grouped comparisons, doughnuts, pies, and radar charts.  
- **10 thematic tabs**: Overview, Staff & HRH, MNCH Services, Nutrition, Drugs & Supply, Equipment, Referral, Mortality & QI, Power & Infrastructure, Facility Tables.  
- **30+ interactive charts**, each with facility-level and LGA-level filters populated with real facility names.  
- **Global Filter Bar** enables cross-tab filtering by facility type, LGA, or individual facility.  
- **Nutrition Commodity Comparison Chart** provides PHC vs. Secondary analysis across six commodities.  
- Branding integrates U.S. Department of State, Bauchi State Government, and EpiC identity.  
- Fully self-contained at ~210KB, deployed via **GitHub Pages** with a single clickable link.

---

## What It Achieved
- Delivered a complete MNCH+N readiness intelligence system from ODK instrument to interactive dashboard.  
- Improved data completeness, consistency, and turnaround time across 106 facilities.  
- Enabled LGA-level gap identification across six readiness domains.  
- Provided facility-level drill-downs on BEmONC signal functions.  
- Surfaced nutrition commodity stockout patterns, enabling supply chain corrections.  
- Supported state-level MNCH performance reviews with referral linkage, power reliability, and maternal mortality audit data.  
- Produced a portable, offline-capable dashboard operable in low-bandwidth environments.

---

## Importance in MNCH+N and Global Health Security
Nigeria bears a disproportionate share of global maternal and newborn deaths, with northern states recording among the highest ratios. Facility readiness, the availability of skilled personnel, medicines, equipment, and infrastructure is the most modifiable determinant of survival at the point of care.  

This project addresses key priorities:
- **Health System Strengthening (HSS):** Replicable model for generating actionable facility readiness intelligence.  
- **EmONC Standards Compliance:** Tracks BEmONC/CEmONC signal functions, aligning with SDG 3.1 and WHO benchmarks.  
- **Nutrition Security:** Maps commodity availability against WHO/UNICEF frameworks, linking supply gaps to child survival outcomes.  
- **Digital Health:** Demonstrates transition from paper-based systems to interoperable digital platforms.  
- **Programme Accountability:** Aligns readiness indicators with EpiC targets and U.S. Government reporting requirements.  
- **Equity and Reach:** Captures readiness at PHCs, the first point of contact for most of Bauchi’s rural population.

---

## Technology Stack
- **Field Data Collection:** ODK (XLSForm), ODK Central, Android devices  
- **Data Processing:** Python, pandas, Excel/XLSX  
- **Dashboard Frontend:** HTML5, CSS3, JavaScript (ES6)  
- **Visualization:** Chart.js, ChartDataLabels plugin  
- **Deployment:** GitHub Pages  
- **Design:** Custom CSS, U.S. Dept. of State, Bauchi State, EpiC branding  

---

## Author
**Moses Luke, PhD(c), MPH**
- Senior Technical Advisor | Digital Health & Health Informatics Analyst
  AI Automation Expert | Published Researcher | Data Storytelling & Decision Intelligence
  MEARL | Global Health Security | Data-Driven Solutions to Improve Healthcare Access
---
