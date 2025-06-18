# Empirical Analysis of Design Patterns and Software Maintainability

## 📖 Overview

This project is an empirical study that investigates how the use of **Gang of Four (GoF)** design patterns influences the **maintainability** of software systems. By analyzing multiple open-source Java projects, the study provides evidence on whether design patterns enhance or hinder key maintainability attributes such as complexity, coupling, and cohesion.

## 🎯 Objectives

- Detect and classify GoF design patterns in real-world Java projects.
- Compute key maintainability metrics (e.g., WMC, CBO, RFC, LCOM, LOC).
- Compare and analyze maintainability metrics for classes **with** and **without** design patterns.
- Visualize and interpret the impact of design patterns on software maintainability.
- Provide actionable insights for developers and architects on the judicious use of design patterns.

## ⚙️ Methodology

1. **Selection of Projects**
   - 30+ open-source Java projects with at least 5,000 LOC.
   - Variety in domains to ensure generalizability.

2. **Design Pattern Detection**
   - Used a GoF design pattern detection tool to analyze Java bytecode.
   - Recorded instances of 15 classic GoF patterns.

3. **Maintainability Metrics**
   - Used the CK-Meter tool to compute:
     - Weighted Methods per Class (WMC)
     - Coupling Between Objects (CBO)
     - Response for a Class (RFC)
     - Lack of Cohesion of Methods (LCOM)
     - Lines of Code (LOC)
     - Depth of Inheritance Tree (DIT)
     - Number of Children (NOC)
     - Fan-in and Fan-out

4. **Statistical Analysis**
   - Compared average metrics for classes **with** and **without** patterns.
   - Visualized results using bar plots.
   - Discussed implications on maintainability.

## 📊 Key Findings

| Metric | With Patterns | Without Patterns |
| ------ | -------------- | ---------------- |
| Weighted Methods per Class (WMC) | 15.57 | 10.43 |
| Coupling Between Objects (CBO) | 6.71 | 5.06 |
| Response for a Class (RFC) | 14.34 | 9.93 |
| Lack of Cohesion of Methods (LCOM) | 23.62 | 20.00 |
| Lines of Code (LOC) | 85.61 | 51.19 |
| Depth of Inheritance Tree (DIT) | ~2.07 | ~2.06 |
| Number of Children (NOC) | 0.63 | 0.17 |

> **Insight:** Design patterns tend to increase complexity and coupling but can provide structural benefits and reusability. Use them judiciously to balance maintainability and design flexibility.

## 🧰 Tech Stack & Tools

- 🟦 **Java** — Target language for analysis.
- 📦 **GoF Design Pattern Detector** — For automated pattern identification.
- 🧮 **CK-Meter** — For computing maintainability metrics.
- 📊 **Python** / **R** (optional) — For statistical analysis and visualization.

## 🚀 How to Reproduce

1. Clone the repo  
2. Install Java and analysis tools  
3. Run detection and metrics scripts (examples in `/pattern-detection` and `/metrics-analysis` folders)  
4. Analyze and visualize results using Python or R notebooks.
