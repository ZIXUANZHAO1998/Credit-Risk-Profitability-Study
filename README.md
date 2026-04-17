# Strategic Credit Risk & Profitability Analysis (2.2M Records)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Engineering-orange.svg)
![Tableau](https://img.shields.io/badge/Tableau-Visualization-blueviolet.svg)

## 🎯 Executive Summary
This project evaluates the risk-return profile of a **$30B+ loan portfolio** from LendingClub (2.26 million records). By building an optimized data pipeline, I identified a systemic pricing failure where credit risk outpaced interest income in high-risk segments.

**Key Finding:** Grades C through G exhibit a "Negative Spread," with the riskiest tier (Grade G) resulting in an **expected net loss of 12.5%** per dollar lent.

---

## 🛠️ Technical Workflow & Data Engineering
### 1. Large-Scale Data "Slimming"
- **The Challenge:** Raw dataset contained 145 columns and occupied **2.4GB**, causing memory overflows.
- **The Solution:** Implemented a memory-efficient loading strategy in Python, filtering for 10 mission-critical financial attributes.
- **Result:** Reduced memory footprint by **90%+**, improving processing speed from minutes to seconds.

### 2. Feature Engineering
- **Interest Calibration:** Converted string-based interest rates into numeric floats for mathematical modeling.
- **NPL Definition:** Synthesized a binary `is_bad` indicator to capture **Non-Performing Loans (NPL)**, including "Charged Off" and "Late" statuses.

---

## 📊 Business Insights
### 1. Risk-Yield Divergence (Figure 1)
- **The Scaling Gap:** While nominal interest rates increase linearly, the **Default Rate exhibits exponential growth**. 
- **The Crossing Point:** Beyond Grade B, the cost of risk exceeds the interest premium, rendering the current pricing model unsustainable.

### 2. Profitability Analysis (Figure 2)
- **Safe Zone:** Grades A and B maintain healthy net margins (~1.8% to 3.4%).
- **The Red Zone:** From Grade C onwards, net margin turns negative. The institution is essentially subsidizing high-risk borrowers with profits from safer tiers.

---

## 💡 Strategic Recommendations
1. **Immediate De-risking:** Suspend originations for Grades F and G until pricing models are recalibrated.
2. **Yield Adjustment:** Increase interest rates for mid-tier risk (Grades C/D) by **200-500 basis points**.
3. **Advanced Screening:** Incorporate secondary variables (DTI, Annual Income) to filter sub-segments within the high-risk grades.

---

## 📂 Repository Structure
- `Strategic Credit Risk & Profitability Analysis.ipynb`: Main Python notebook for data processing.
- `README.md`: Project documentation and executive summary.

---
*Note: For a full interactive experience and detailed visual analysis, please refer to my [Notion Case Study](https://www.notion.so/Project-1-Strategic-Credit-Risk-Profitability-Analysis-A-2-2M-Record-Study-3434961d87b5802b9afcfae633b3b869?source=copy_link).*
