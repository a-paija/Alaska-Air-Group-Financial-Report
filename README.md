## Project Background

Despite consistent revenue growth, the company faces a **structural profitability crisis**. Revenue grew **15.5x** since 1989, yet net income grew only **2.3x**. Management lacks visibility into the underlying drivers of margin erosion, making it difficult to identify where costs are spiraling, why operating leverage has failed, and how to restore sustainable profitability.

Without structured analysis, the organization is unable to answer critical business questions such as:
- Why has net margin collapsed from 15.2% to 0.7% despite record revenue?
- Why does cost growth consistently outpace revenue growth?
- Why is the company achieving diseconomies of scale rather than economies of scale?
- Why does free cash flow remain negative despite positive operating cash flow?
- How did debt more than double to $6.9B, and what is the path to deleveraging?

#### **Overall Goal: Diagnose the root causes of profitability decline and provide actionable recommendations to stabilize cost structure, restore efficiency, and generate sustainable margin expansion.**

> **Note:** Detailed recommendations and implementation actions are consolidated in the final section of this report.



**📄 An official report for stakeholders and business leaders can be found [here](link-to-pdf)**



## Data Structure & Initial Checks

### Data Sources

Financial data was sourced from **public financial records** available on Alaska Air Group's Investor & Shareholder Relations website, including:

- **Income Statements** – Revenue, Cost of Revenue, Operating Expenses, Net Income
- **Cash Flow Statements** – Operating Cash Flow, Free Cash Flow, Capital Expenditures
- **Balance Sheets** – Total Debt, Interest Expense, Total Liabilities, Equity

### Data Processing & Cleaning (Power Query)

Raw financial statements were extracted and consolidated using **Excel and Power Query**. The following steps were performed to ensure data accuracy and consistency:

1. **Data Extraction:** Downloaded annual financial statements from Alaska Air Group's investor relations portal (10-K filings, annual reports) covering 1989–2025.

2. **ETL Process (Power Query):**
   - Imported raw data from multiple Excel files and PDF extracts
   - Combined income statements, cash flow statements, and balance sheets into a single master dataset
   - Standardized fiscal year-end dates to ensure alignment across statements
   - Removed duplicate records and merged fragmented datasets
   - Aggregated data at the annual level for consistent period-over-period comparison

3. **Data Cleaning:**
   - Handled missing values by cross-referencing with supplementary filings (10-Q, 8-K)
   - Standardized currency formatting to consistent units (USD)
   - Ensured consistent naming conventions and field definitions
   - Flagged outliers and anomalies for review (e.g., 2001 restructuring charges, 2020 pandemic-driven write-offs)

4. **Metric Calculation:** Derived key performance indicators including:
   - Net Margin = Net Income / Revenue
   - Operating Margin = Operating Income / Revenue
   - Gross Margin = (Revenue – Cost of Revenue) / Revenue
   - Cost per Revenue = Total Expenses / Revenue
   - Interest Coverage = EBIT / Interest Expense
   - Free Cash Flow = Operating Cash Flow – Capital Expenditures
   - YoY Revenue Growth and YoY Expense Growth

### Final Dataset Structure

| Column | Description |
|--|-|
| Year | Fiscal year (1989–2025) |
| Revenue | Total revenue in USD |
| Net Income | Net income in USD |
| Net Margin | Net income / Revenue (%) |
| Operating Cash Flow | Cash from operations in USD |
| Free Cash Flow | Operating Cash Flow – CapEx in USD |
| Total Debt | Total debt obligations in USD |
| Cost of Revenue | Cost of goods/services sold in USD |
| Operating Expense | SG&A and other operating expenses in USD |
| Total Expenses | Cost of Revenue + Operating Expense in USD |
| Operating Income | Revenue – Total Expenses in USD |
| Interest Expense | Interest paid on debt in USD |
| EBITDA | Earnings before interest, taxes, depreciation, amortization |
| Operating Margin | Operating Income / Revenue (%) |
| Cost per Revenue | Total Expenses / Revenue ($) |



## Executive Summary

Alaska Air Group has grown revenue **15.5x** since 1989, from $917 million to $14.2 billion, and **130%** since 2021. Yet net income has multiplied only **2.3x** over 36 years, rising from $43 million to just $100 million, and has fallen **79%** in the last five. Net margin now sits at **0.7%**, down from 7.7%.

The company is scaling revenue but not scaling profit. The disconnect is driven by **five structural failures**:

| Driver | Core Problem | Root Cause |
|--|--||
| **1. Cost Volatility & Control** | Total costs remain highly unpredictable | External shocks + structural sensitivity |
| **2. Cost Efficiency Decline** | Cost per revenue worsened 26% since 2015 | Shocks disrupt operational discipline; costs rise with scale |
| **3. No Operating Leverage** | Revenue +130%, operating margin -7pp | Revenue growth absorbed by rising costs |
| **4. Margin Compression** | Net margin 15.2% → 0.7% | Cumulative outcome of inefficiency and lack of leverage |
| **5. Escalating Debt Burden** | Debt +115%, FCF negative | Shocks force borrowing; debt amplifies fragility |

> **The company's primary constraint is not revenue generation, but the ability to convert revenue into sustainable profit due to structural cost inefficiencies, a lack of operating leverage, and a compounding debt burden.**

Addressing these gaps represents a significant opportunity to unlock near-term margin recovery while improving long-term financial sustainability.



## Key Problem Drivers & Analysis

### 1. Cost Volatility & Control

While the company has improved operating efficiency over time, its cost structure has shifted toward high cost-of-revenue dependence, limiting operating leverage and preventing strong margin expansion despite revenue growth.

**What the Data Shows:**
- OpEx held at roughly **10% of revenue** since 2015 (well-controlled)
- Total costs remain highly unpredictable due to extreme swings in Cost of Revenue and one-time items
- Expense growth has outpaced revenue growth in **nearly every period analyzed**

**External Shocks & Structural Events:**

- **2008 Financial Crisis & Fuel Spike:** Record oil prices exceeding $100/barrel pushed fuel costs to an unprecedented share of revenue. Reactive cost measures created significant one-time charges and restructuring expenses.

- **2017 Virgin America Integration:** Merger-related costs contributed to a **44–50%** rise in operating expenses.

- **2020 COVID-19 Pandemic:** Passenger counts fell to 5% of prior-year levels, forcing a **50% capacity reduction** and over **4,000 workforce reductions**. Fuel prices fell, but non-fuel unit costs surged **26%** due to capacity cuts, and the company drew heavily on debt to preserve liquidity.

**Root Cause:** External shocks + structural sensitivity

**Implication:** Cost unpredictability complicates investment decisions, pricing strategy, and budgeting. External shocks force reactive cost-cutting, which generates further volatility. Recurring, large-scale cost disruptions constrain the company's ability to plan for sustainable profitability.



### 2. Cost Efficiency Decline

Cost per revenue improved significantly from the early turbulent years, reaching its best level in **2009 at $0.70 per dollar of revenue**. However, since then, efficiency has steadily declined, with cost per revenue worsening **26% to $0.96 in 2025**.

**What the Data Shows:**
- 2009: **$0.70** cost per revenue (Best performance)
- 2015: **$0.76** cost per revenue
- 2025: **$0.96** cost per revenue (**+26% deterioration**)

**Root Cause:** Shocks disrupt operational discipline; costs rise with scale

**Implication:** Each external shock resets the cost base higher, and the company has not recovered operational discipline between shocks. Growth amplifies the problem rather than solving it.



### 3. No Operating Leverage

**Expense Growth vs. Revenue Growth:** In multiple periods, cost growth exceeds revenue growth, indicating sustained margin pressure.

**Efficiency Gap (Operating Margin vs. Net Margin):** A persistent gap between operating and net margins indicates that non-operating costs continue to erode profitability beyond core operations.

**What the Data Shows:**
- 2021–2025: Revenue grew **130%**, yet operating margin fell from **10.9% to 3.9%** (−7pp)
- 2025: Operating margin stood at **3.9%** while net margin was **0.7%** (gap of 3.2pp)
- Gap has persisted across the period, averaging approximately **3 percentage points**

**Root Cause:** Revenue growth absorbed by rising costs

**Implication:** The combination of rising costs and persistent non-operating leakage means revenue growth delivers no margin benefit. The company is scaling revenue without scaling profit.



### 4. Margin Compression

Net margin has collapsed from **15.15% (2015) to 0.7% (2025)**.

**What the Data Shows:**
- 2015: **15.15%** net margin (Peak)
- 2020: **−37.13%** net margin (Pandemic shock)
- 2025: **0.7%** net margin
- **A 5% revenue decline** would wipe out all profitability

**Root Cause:** Cumulative outcome of inefficiency and lack of leverage

**Implication:** The company is structurally fragile. Margin compression is not cyclical; it is the logical result of a cost base that is volatile, inefficient, and unresponsive to scale. The 2020 shock exposed this fragility, and the company has not recovered a sufficient margin cushion since.



### 5. Escalating Debt Burden

**What the Data Shows:**

| Metric | 2019 | 2025 | Change |
|--|||--|
| Total Debt | $3.2B | $6.9B | **+115%** |
| Interest Expense | $63M | $235M | **+273%** |
| Free Cash Flow | $1,026M | −$339M | **−133%** |
| Interest Coverage | 17.1x | 1.6x | **−91%** |
| Interest / Operating Income | 6% | 42% | **+36pp** |

**Root Cause:** Shocks force borrowing; debt amplifies fragility

**Implication:** Debt is not a separate problem; it is a compounding factor. Each external shock forces borrowing, and borrowing in turn increases fixed obligations, making the company more vulnerable to the next shock. Negative free cash flow means the company cannot fund operations or growth internally, creating a self-reinforcing cycle: borrow to survive, pay more interest, borrow more to cover interest, and further erode profitability.

