# ICU Overload Risk Assessment Across U.S. Hospital Regions Under COVID-19 Scenarios

### 🛠Tools Used  
![Excel](https://img.shields.io/badge/Excel-217346?logo=microsoft-excel&logoColor=white&style=flat)  ![Tableau](https://img.shields.io/badge/Tableau-E97627?logo=tableau&logoColor=white&style=flat)

### Project Type  
![Data Transformation](https://img.shields.io/badge/Data%20Transformation-purple)  ![Data Visualization](https://img.shields.io/badge/Data%20Visualization-blue)

---

## Table of Contents

1. [Project Background](#1-project-background)  
2. [Project Objectives](#2-project-objectives)  
3. [Data Structure Overview](#3-data-structure-overview)  
4. [Executive Summary](#4-executive-summary)  
5. [Insight Deep Dive](#5-insight-deep-dive)  
   - [Plot 1: Geographic Distribution of ICU Strain](#plot-1-geographic-distribution-of-icu-strain)  
   - [Plot 2: Overload Severity Under Varying Scenarios](#plot-2-overload-severity-under-varying-scenarios)  
   - [Plot 3: Persistent High-Risk HRRs Across All Scenarios](#plot-3-persistent-high-risk-hrrs-across-all-scenarios)  
   - [Plot 4: Scenario Sensitivity and Ranking Stability](#plot-4-scenario-sensitivity-and-ranking-stability)  
6. [Strategic Recommendations for ICU Overload Mitigation](#6-strategic-recommendations-for-icu-overload-mitigation)  
7. [Assumptions & Caveats](#7-assumptions--caveats)

---

## 1. Project Background

The COVID-19 pandemic exposed structural weaknesses in healthcare infrastructure, especially the limited surge capacity of ICU units across the U.S. Early in the pandemic, hospitals in certain regions faced severe strain, while others remained relatively unaffected. This variation highlighted the need for localized, scenario-based forecasting to inform future preparedness efforts.

With evolving variants, vaccination rates, and healthcare worker shortages, it became essential to assess how different infection scenarios might impact ICU capacity at the regional level. This project addresses that need by simulating ICU overload across 306 Hospital Referral Regions (HRRs) under varying COVID-19 infection rates and durations.

---

## 2. Project Objectives

This project aims to assess and visualize ICU overload risks under nine COVID-19 outbreak scenarios, focusing on three key objectives:

- **Identify** persistently high-risk HRRs that are vulnerable across multiple infection scenarios.
- **Quantify** how outbreak severity parameters (infection rate and pandemic duration) impact ICU strain.
- **Generate actionable recommendations** for healthcare planners, enabling targeted interventions and resource reallocation to prevent systemic ICU collapse.

---

## 3. Data Structure Overview

This project uses a dataset from the Harvard Global Health Institute that models hospital system capacity across 306 U.S. Hospital Referral Regions (HRRs) under nine COVID-19 infection scenarios. It combines baseline infrastructure data—such as total and available hospital and ICU beds—with projected demand based on varying infection rates (20%, 40%, 60%) over different timeframes (6, 12, 18 months).

**Key data fields include:**

- **Capacity metrics**: Total, available, and potentially available hospital and ICU beds.
- **Population stats**: Adult and senior population per HRR.
- **Scenario projections**: Estimated hospitalizations and ICU needs per scenario.
- **Stress indicators**: Percentage of beds required under each scenario.

While the full dataset covers general hospital capacity, this analysis focuses specifically on ICU bed shortages under stress.

---

## 4. Executive Summary

This project evaluates the risk of ICU overload across U.S. hospital referral regions using simulation data from nine pandemic scenarios. Across these scenarios, most regions are shown to exceed their ICU capacity, with smaller or rural HRRs consistently facing the highest strain.

Spatial analysis revealed that ICU pressure is widespread, but especially acute in certain high-density or structurally under-resourced areas like York, PA and Winston-Salem, NC. As infection severity increases (higher infection rates over shorter durations), ICU overload rises exponentially, with some HRRs experiencing demand 50–75 times greater than their available capacity.

Ranking analysis showed that some HRRs remain in the top tier of overload risk regardless of the scenario. These consistently high-risk regions include both small-market areas (e.g., Mason City, IA) and larger, coastal HRRs with existing high occupancy rates. Additionally, even small shifts in scenario parameters (e.g., from 12 to 18 months duration) significantly affect ICU burden, emphasizing the sensitivity of healthcare systems to pandemic dynamics.

These insights suggest that fixed vulnerabilities exist within the U.S. hospital system, and that localized, data-driven planning is critical. The project concludes with recommendations to enhance surge capacity in persistently high-risk HRRs, build rural ICU networks, and implement dynamic response plans tied to real-time infection rates.

---

## 5. Insight Deep Dive

### Plot 1: Geographic Distribution of ICU Strain
![Dashboard Screenshot](https://github.com/Chuqin5114/ICU_Overload_Analysis/blob/6ae9c1a5ee65586f7d9cdcab1b78c489122e2c19/image/ICU%20capacity%20map.png)

- **Widespread Overcapacity**: The majority of Hospital Referral Regions (HRRs) exhibit ICU occupancy rates exceeding 50%, signaling a systemic lack of surge capacity across the U.S.
- **Critical Hotspots**: Certain smaller HRRs—such as Winston-Salem, NC, and York, PA—demonstrate extreme ICU strain, with occupancy levels surpassing 75%. These regions have minimal buffer to accommodate any additional patient influx.
- **Urban-Rural Disparities**: Larger HRRs, particularly those along the East Coast and in urban centers, tend to have more total ICU beds but also higher occupancy. Conversely, rural HRRs often have significantly fewer beds, rendering them vulnerable despite lower population density.

### Plot 2: Overload Severity Under Varying Scenarios
![Dashboard Screenshot](https://github.com/Chuqin5114/ICU_Overload_Analysis/blob/6ae9c1a5ee65586f7d9cdcab1b78c489122e2c19/image/ICU%20Overload%20Index%20Histogram.png)

- **Nonlinear Risk Growth**: In mild scenarios (e.g., 20% infection rate over 18 months), most HRRs experience modest overload (Index 0–3). However, in severe scenarios (e.g., 60% infection rate over 6 months), the Overload Index escalates dramatically—ranging from 10 to as high as 75+ across regions.
- **Right-Skewed Risk Distribution**: Mild scenarios result in low overload for most HRRs with a few exceptions. In contrast, severe scenarios reveal a heavy tail of extreme overload, indicating that some HRRs could be overwhelmed by orders of magnitude beyond their capacity.

### Plot 3: Persistent High-Risk HRRs Across All Scenarios
![Dashboard Screenshot](https://github.com/Chuqin5114/ICU_Overload_Analysis/blob/6ae9c1a5ee65586f7d9cdcab1b78c489122e2c19/image/Top%2020%20Overload%20Index.png)

- **Consistent Overload Leaders**: A subset of HRRs, such as York, PA; Santa Cruz, CA; and Traverse City, MI, consistently rank among the highest in ICU overload across all nine pandemic scenarios. This persistent pattern suggests structural vulnerabilities not mitigated by scenario parameters.
- **Small but Stressed**: Many of these high-risk HRRs are small or mid-sized (e.g., Mason City, IA; Dubuque, IA), underscoring a mismatch between ICU infrastructure and potential demand in less populous areas.

### Plot 4: Scenario Sensitivity and Ranking Stability
![Dashboard Screenshot](https://github.com/Chuqin5114/ICU_Overload_Analysis/blob/6ae9c1a5ee65586f7d9cdcab1b78c489122e2c19/image/change%20in%20HRR%20Risk%20Ranking.png)

- **Fixed High-Risk Core**: The most vulnerable HRRs maintain top overload rankings regardless of changes in infection rate or pandemic duration. This stability points to chronic capacity shortfalls in these regions.
- **Parameter Sensitivity**: Longer outbreak durations generally reduce ICU overload, while higher infection rates significantly amplify it. These trends confirm that small changes in pandemic dynamics can yield disproportionate impacts on healthcare systems.

---

## 6. Strategic Recommendations for ICU Overload Mitigation

### 1. Prioritize Persistent High-Risk HRRs

- Deploy mobile ICU units or temporary field hospitals to HRRs consistently identified as high-risk, such as York, PA; Santa Cruz, CA; and Traverse City, MI.
- Establish formal patient transfer agreements between these HRRs and neighboring regions with available ICU capacity.

**Rationale**: HRRs with structurally limited ICU resources are unable to absorb even moderate case increases, making them priority candidates for targeted interventions.

### 2. Implement Dynamic Resource Allocation Based on Scenario Severity

- Define tiered response thresholds linked to real-time infection rates and ICU occupancy levels.
  - **Mild Scenario (IR ≤ 0.2)**: Activate local staffing reserves.
  - **Severe Scenario (IR ≥ 0.4)**: Reallocate ventilators, staff, and equipment from lower-risk to high-risk HRRs.
- Develop a national surge monitoring dashboard to guide proactive resource deployment.

**Rationale**: ICU overload rises exponentially in high-infection, short-duration scenarios. Early, dynamic redistribution of resources can prevent regional collapses from becoming national crises.

### 3. Address Structural Gaps in Rural and Small HRRs

**Actions**:

- Form regional ICU coalitions among neighboring rural HRRs (e.g., Iowa clusters) to pool capacity and develop shared contingency plans.
- Expand tele-ICU networks to provide remote specialist support, reducing the need for transfers.

**Rationale**: Persistent overload in smaller HRRs stems from inherently low bed counts. Scalable, networked solutions are essential to ensure continuity of care in these structurally vulnerable areas.

### 4. Optimize Capacity in High-Demand Urban HRRs

**Actions**:

- Cross-train non-ICU personnel and ease credentialing restrictions to expand surge staffing pools.
- Streamline discharge and step-down protocols to accelerate ICU bed turnover during surges.

**Rationale**: Many urban HRRs operate with high baseline ICU occupancy. Operational efficiency improvements are necessary to free up capacity during periods of elevated demand.

---

## 7. Assumptions & Caveats

- **Static Bed Capacity**: The model assumes ICU bed availability remains constant throughout the scenario timeline. In reality, hospitals may add beds or convert wards during surges.
- **Even Disease Distribution**: Infection spread is assumed to be evenly distributed within HRRs, not accounting for local clustering or variability in public health response.
- **Uniform Care Demand**: The analysis presumes a consistent proportion of infected individuals will require ICU care. It does not adjust for age, comorbidities, or vaccine-induced severity reductions.
- **No Staffing Constraints**: ICU capacity here refers only to physical beds, not accounting for staffing shortages or burnout, which are often more limiting in real-world surge situations.
- **No Policy Interventions**: The model does not incorporate mitigation effects such as mask mandates, vaccination campaigns, or lockdowns, which could drastically reduce ICU demand.
- **Pre-COVID Infrastructure Baseline**: ICU bed estimates are based on pre-pandemic surveys and do not reflect expansions or contractions that may have occurred since.

---
