# Comprehensive Financial Modeling Course

## Based on "Cash Flow For Dummies" and Industry Best Practices

---

# Course Overview

Financial modeling is the art and science of building a mathematical representation of a company's financial performance. As the CFA Institute notes, "Models synthesize a vast amount of information to help users make better investment and business decisions."

This course builds directly on the mathematics foundation you've already developed and applies those skills to real-world business scenarios. Each module builds on the previous one, using actual company examples and Excel-based practice.

**Pre-requisites:** Completion of the Comprehensive Mathematics Course (Modules 1-4, or equivalent understanding of accounting, time value of money, and basic algebra)

**Goal:** By the end of this course, you will be able to build a complete three-statement financial model from scratch, perform company valuations, and analyze complex transactions like mergers and leveraged buyouts.

---

# Module 1: Foundations of Financial Modeling

## 1.1 What Is Financial Modeling?

### Learning Objectives
- Understand the purpose and use of financial models
- Identify the key components of a financial model
- Recognize the connection between modeling and business decision-making

### Core Concepts

**Definition**
Financial modeling is the process of creating a mathematical representation of a company's financial performance. As one expert puts it, "Financial modeling isn't just about playing with numbers in Excel—it's about truly understanding the business, its revenue drivers, and how money flows through the company."

**Why Models Matter**
- **Decision-making:** Models help evaluate investments, acquisitions, and strategic choices
- **Valuation:** Models determine what a company is worth
- **Planning:** Models forecast future cash needs and performance
- **Risk assessment:** Models test how changes in assumptions affect outcomes

### Practice Problems

1. **Identifying Model Purpose**
   For each scenario, identify what type of model would be most appropriate:
   - A private equity firm considering acquiring a company
   - A startup seeking to raise capital from investors
   - A company deciding whether to build or buy a new factory
   - A bank evaluating a loan application

2. **Real-World Application**
   From the book: "The balance sheet, income statement, and statement of cash flows fit together like pieces in a puzzle."
   - Why is it important that a financial model integrates all three statements?
   - What happens if a model only focuses on the income statement?

## 1.2 Understanding Financial Statements (Review)

### Learning Objectives
- Review the three primary financial statements
- Understand how they connect and interact
- Identify key drivers in each statement

### Core Concepts

**The Three-Statement Model**
The foundation of all financial modeling is the three-statement model, which links:
1. **Income Statement** (Profit & Loss) - Shows profitability over time
2. **Balance Sheet** - Shows financial position at a point in time
3. **Cash Flow Statement** - Shows how cash moves through the business

**The Interconnection**

```
Income Statement
     ↓
Net Income flows to:
     ↓
Cash Flow Statement (Operating section)
     ↓
Cash balance flows to:
     ↓
Balance Sheet (Cash account)
     
Meanwhile, Balance Sheet changes (A/R, Inventory, A/P) flow back to:
     ↓
Cash Flow Statement (Working Capital changes)
```

### Practice Problems

1. **Statement Linking**
   - If a company reports $100,000 in net income, where does this appear on the cash flow statement?
   - If accounts receivable increases by $50,000, how does this affect cash flow?
   - If the company borrows $200,000, where does this appear?

2. **Real-World Application**
   From the book: "The cash flow from operating activities is the most important section of the statement of cash flows."
   - Why is operating cash flow more important than net income for understanding a company's health?

---

# Module 2: Excel for Financial Modeling

## 2.1 Essential Excel Skills

### Learning Objectives
- Master Excel functions used in financial modeling
- Understand best practices for model design
- Build efficient, error-free spreadsheets

### Core Concepts

**Essential Excel Functions for Modeling**

| Function | Use | Example |
|----------|-----|---------|
| `SUM()` | Adding totals | `=SUM(B2:B12)` |
| `AVERAGE()` | Calculating means | `=AVERAGE(C3:C10)` |
| `IF()` | Conditional logic | `=IF(Revenue>100000,"Bonus","No Bonus")` |
| `VLOOKUP()` | Finding values in tables | `=VLOOKUP(A2,Table,2,FALSE)` |
| `INDEX/MATCH` | Advanced lookups | `=INDEX(C:C,MATCH(A2,B:B,0))` |
| `NPV()` | Net present value | `=NPV(rate,value1,value2...)` |
| `IRR()` | Internal rate of return | `=IRR(values,guess)` |
| `XNPV()` | NPV with specific dates | `=XNPV(rate,values,dates)` |
| `XIRR()` | IRR with specific dates | `=XIRR(values,dates,guess)` |

**Best Practices for Model Design**
1. **One formula per row** - Never hard-code numbers in formulas
2. **Separate inputs from calculations** - Use an assumptions tab
3. **Color coding** - Blue for inputs, black for formulas, green for links
4. **Consistent formatting** - Thousands separators, decimal alignment
5. **Error checking** - Use `ISERROR()` and `IFERROR()` functions

### Practice Problems

1. **Excel Functions**
   - Create a formula that calculates the average of cells B2 through B12
   - Write an IF statement that returns "Profitable" if profit > 0 and "Loss" if profit ≤ 0
   - How would you calculate the present value of $10,000 received annually for 5 years at 8%?

2. **Real-World Application**
   From the book: "Most companies prepare budgets on an annual basis, with monthly projections for the next 12 months."
   - Build a simple Excel model that forecasts monthly sales for the next year based on 20% annual growth.

## 2.2 Model Structure and Design

### Learning Objectives
- Design a well-structured financial model
- Understand optimal model flow
- Create presentation-ready output

### Core Concepts

**Standard Model Structure**

```
Tab 1: Cover Page (Model title, company name, date, version control)
Tab 2: Executive Summary (Key metrics, charts, summary tables)
Tab 3: Assumptions (All inputs in one place, color-coded)
Tab 4: Income Statement (Forecasted P&L)
Tab 5: Balance Sheet (Forecasted balance sheet)
Tab 6: Cash Flow Statement (Forecasted cash flows)
Tab 7: Supporting Schedules (Depreciation, debt, working capital)
Tab 8: Valuation (DCF, comparable analysis)
Tab 9: Sensitivity Analysis (Scenario testing)
```

**The Assumptions Tab**
The assumptions tab is the single most important sheet in your model. All inputs should be:
- Clearly labeled
- Color-coded (typically blue for inputs)
- Well-documented with sources
- Easily changeable for scenario testing

### Practice Problems

1. **Model Design**
   - Sketch the tab structure for a model of a retail company
   - What assumptions would you include for a manufacturing company?
   - How would you handle historical data versus forecasted data?

2. **Real-World Application**
   From the book: "The business plan can come in a multitude of formats and include all types of information, data, graphs, charts, analyses, and more."
   - Design a cover page and executive summary tab for a model of ACME Distribution, Inc.

---

# Module 3: Building the Three-Statement Model

## 3.1 Forecasting the Income Statement

### Learning Objectives
- Forecast revenue based on business drivers
- Project costs and expenses
- Calculate net income and key profitability metrics

### Core Concepts

**Revenue Forecasting**
Revenue is typically the starting point for any model. Common approaches include:

1. **Top-down approach:** Start with market size and estimate market share
2. **Bottom-up approach:** Start with unit sales and multiply by price
3. **Historical growth approach:** Apply historical growth rates
4. **Driver-based approach:** Link revenue to key business drivers

**Cost Forecasting**
Costs are typically categorized as:
- **Variable costs** - Change with revenue (COGS, sales commissions)
- **Fixed costs** - Don't change with revenue (rent, salaries)
- **Semi-variable costs** - Partially change with revenue

### Practice Problems

1. **Revenue Forecasting**
   - A company sells 10,000 units at $50 per unit. Revenue grows 5% annually. Forecast revenue for 5 years.
   - A software company has 1,000 customers paying $100/month. Churn is 5% annually and new customers are 200 per year. Forecast revenue for 3 years.

2. **Cost Forecasting**
   - Variable costs are 60% of revenue. Fixed costs are $200,000 growing at 3% annually. Forecast total costs.
   - Depreciation is $50,000 per year. How does this affect the income statement versus the cash flow statement?

3. **Real-World Application**
   From the book: "The business earned $600,000 bottom-line profit for the year just ended, which equals sales revenue minus all expenses."
   - If revenue is $12,000,000 and expenses are $11,400,000, what is the profit?
   - If profit is 5% of revenue, what are expenses as a percentage of revenue?

## 3.2 Forecasting the Balance Sheet

### Learning Objectives
- Project balance sheet items based on business drivers
- Understand working capital relationships
- Ensure the balance sheet balances

### Core Concepts

**Working Capital Projections**
Working capital items are typically linked to revenue or expenses:

| Item | Driver | Typical Relationship |
|------|--------|---------------------|
| Accounts Receivable | Revenue | Days Sales Outstanding (DSO) |
| Inventory | COGS | Days Inventory Outstanding (DIO) |
| Accounts Payable | COGS or Operating Expenses | Days Payable Outstanding (DPO) |

**Fixed Asset Projections**
- Capital expenditures (CAPEX) are forecasted based on business plans
- Depreciation is calculated based on asset lives
- Net PP&E = Prior PP&E + CAPEX - Depreciation

**Debt Projections**
- Existing debt is tracked with repayment schedules
- New debt is added as needed (often to fund cash shortfalls)
- Interest expense is calculated based on average debt balances

### Practice Problems

1. **Working Capital Projections**
   - Revenue is $10,000,000 with DSO of 45 days. What is Accounts Receivable?
   - COGS is $6,000,000 with DIO of 60 days. What is Inventory?
   - COGS is $6,000,000 with DPO of 30 days. What is Accounts Payable?

2. **Fixed Asset Projections**
   - PP&E is $1,000,000 with CAPEX of $200,000 per year and depreciation of $100,000 per year. Forecast PP&E for 3 years.
   - An asset costs $500,000 and is depreciated over 10 years. What is annual depreciation using straight-line?

3. **Real-World Application**
   From the book: "Accounts receivable, inventory, and prepaid expenses are used in recording revenue and expenses."
   - If sales grow 25%, how would you expect accounts receivable to change?
   - If the company is managing inventory more efficiently, what happens to the DIO ratio?

## 3.3 Forecasting the Cash Flow Statement

### Learning Objectives
- Project cash flow from operating activities
- Project cash flow from investing activities
- Project cash flow from financing activities
- Ensure the model "balances" (cash reconciles)

### Core Concepts

**Cash Flow from Operations**
```
Net Income
+ Depreciation & Amortization
+ Decrease in Accounts Receivable (or - Increase)
+ Decrease in Inventory (or - Increase)
+ Increase in Accounts Payable (or - Decrease)
+ Increase in Accrued Expenses (or - Decrease)
= Cash Flow from Operations
```

**Cash Flow from Investing**
```
- Capital Expenditures
- Acquisitions
+ Asset Sales
= Cash Flow from Investing
```

**Cash Flow from Financing**
```
+ New Debt Borrowings
- Debt Repayments
+ Equity Issuances
- Dividends
= Cash Flow from Financing
```

**The "Plug"**
When the model doesn't balance (i.e., the balance sheet doesn't balance), a "plug" is needed. Common plugs include:
- Cash (the balancing figure)
- Revolver debt (short-term borrowing)
- Equity (if the company needs to raise capital)

### Practice Problems

1. **Cash Flow Projections**
   - Net Income: $100,000, Depreciation: $20,000, A/R Increase: $30,000, Inventory Decrease: $10,000, A/P Increase: $15,000. Calculate Operating Cash Flow.
   - CAPEX: $50,000, Asset Sales: $10,000. Calculate Investing Cash Flow.
   - New Debt: $40,000, Debt Repayment: $20,000, Dividends: $5,000. Calculate Financing Cash Flow.

2. **Model Balancing**
   - If the model shows cash increasing by $80,000 but the balance sheet shows a $60,000 increase, what's wrong?
   - How would you fix a model that doesn't balance?

3. **Real-World Application**
   From the book: "The statement of cash flows is the dominant financial statement when a business isn't generating enough cash flow."
   - Build a complete cash flow forecast for ACME Distribution using the projections from Chapters 8-9.

---

# Module 4: Advanced Modeling Techniques

## 4.1 Sensitivity Analysis and Scenario Modeling

### Learning Objectives
- Build scenario analysis into models
- Perform sensitivity analysis on key drivers
- Understand the impact of changing assumptions

### Core Concepts

**Scenario Analysis**
Models should include multiple scenarios:
- **Base Case:** Most likely outcome
- **Best Case:** Optimistic assumptions
- **Worst Case:** Pessimistic assumptions
- **Armageddon Case:** Disaster scenario

**Sensitivity Analysis**
Test how changes in key assumptions affect outcomes:
- Revenue growth ± 10%
- Gross margin ± 200 basis points
- DSO ± 10 days
- Interest rate ± 100 basis points

**Data Validation and Scenario Control**
Use Excel's data validation to create drop-down menus that switch between scenarios.

### Practice Problems

1. **Scenario Building**
   - Create three scenarios for ACME Distribution:
     - Base: 10% revenue growth, 25% gross margin
     - Best: 20% revenue growth, 28% gross margin
     - Worst: -5% revenue growth, 22% gross margin
   - What is the cash flow impact in each scenario?

2. **Sensitivity Analysis**
   - For a DCF valuation, test how changes in WACC (±1%) affect valuation
   - Test how changes in terminal growth rate (±0.5%) affect valuation

3. **Real-World Application**
   From the book: "The what-if projection technique is a highly effective business management strategy."
   - Build a sensitivity table showing how profit changes with different revenue growth and gross margin assumptions.

## 4.2 Discounted Cash Flow (DCF) Valuation

### Learning Objectives
- Understand the theory of DCF valuation
- Calculate free cash flow
- Determine the appropriate discount rate
- Calculate terminal value

### Core Concepts

**The DCF Framework**
The value of a business is the present value of its expected future cash flows.

```
Enterprise Value = PV of Free Cash Flows + PV of Terminal Value
Equity Value = Enterprise Value - Net Debt
```

**Free Cash Flow Calculation**
```
Free Cash Flow = EBIT × (1 - Tax Rate) + Depreciation - CAPEX - Change in Working Capital
```

**Weighted Average Cost of Capital (WACC)**
```
WACC = (E/V) × Re + (D/V) × Rd × (1 - Tax Rate)
```
Where:
- E = Market value of equity
- D = Market value of debt
- V = E + D
- Re = Cost of equity (CAPM)
- Rd = Cost of debt

**Terminal Value**
Calculated using either:
1. **Perpetuity Growth Method:** TV = FCF × (1+g) / (WACC - g)
2. **Exit Multiple Method:** TV = EBITDA × Multiple

### Practice Problems

1. **Free Cash Flow Calculation**
   - EBIT: $500,000, Tax Rate: 30%, Depreciation: $50,000, CAPEX: $100,000, Change in Working Capital: $20,000. Calculate FCF.

2. **WACC Calculation**
   - Equity: $800,000, Debt: $200,000, Cost of Equity: 12%, Cost of Debt: 6%, Tax Rate: 30%. Calculate WACC.

3. **DCF Valuation**
   - Forecast FCF for 5 years: $100,000, $120,000, $140,000, $160,000, $180,000
   - WACC: 10%
   - Terminal Growth: 3%
   - Calculate Enterprise Value and Equity Value (Net Debt: $200,000)

4. **Real-World Application**
   From the book: "The value of an asset relates to the present value of expected future cash flows on that asset."
   - Value ACME Distribution using DCF analysis

---

# Module 5: Valuation Methods

## 5.1 Comparable Company Analysis (Trading Comps)

### Learning Objectives
- Identify comparable companies
- Calculate valuation multiples
- Apply multiples to the target company

### Core Concepts

**Common Valuation Multiples**
| Multiple | Formula | Use |
|----------|---------|-----|
| P/E | Price / Earnings | Mature, profitable companies |
| EV/EBITDA | Enterprise Value / EBITDA | Most common for all companies |
| EV/Revenue | Enterprise Value / Revenue | Early-stage or unprofitable companies |
| P/BV | Price / Book Value | Financial institutions |

**Steps in Comparable Company Analysis**
1. **Select comparables:** Same industry, similar size, similar growth
2. **Calculate multiples:** For each comparable company
3. **Apply multiples:** To the target company's metrics
4. **Sensitivity:** Test different multiples

### Practice Problems

1. **Comparable Analysis**
   - Company A: EV/EBITDA = 12x
   - Company B: EV/EBITDA = 14x
   - Company C: EV/EBITDA = 10x
   - Target EBITDA = $50,000,000
   - What is the target's implied enterprise value?

2. **Multiples Application**
   - Revenue: $100,000,000
   - EBITDA: $20,000,000
   - Industry average EV/Revenue = 2x
   - Industry average EV/EBITDA = 8x
   - What is the implied valuation range?

3. **Real-World Application**
   From the book: "Relative valuation estimates the value of an asset by looking at the pricing of 'comparable' assets relative to a common variable like earnings, cash flows, book value or sales."
   - Compare ACME Distribution to its peers using valuation multiples.

## 5.2 Precedent Transaction Analysis

### Learning Objectives
- Understand transaction multiples
- Identify relevant precedent transactions
- Apply transaction multiples to valuation

### Core Concepts

**Transaction Multiples**
Similar to trading comps but based on acquisition prices:
- EV/EBITDA (based on transaction price)
- EV/Revenue (based on transaction price)
- Premiums paid (over market price)

**Key Considerations**
- Control premium (acquirers pay more than market price)
- Synergies (buyer expects cost savings or revenue growth)
- Deal structure (cash vs. stock vs. mix)

### Practice Problems

1. **Transaction Analysis**
   - Similar acquisitions in the industry: EV/EBITDA = 10x, 12x, 11x, 13x
   - Target EBITDA = $30,000,000
   - What is the implied acquisition value?

2. **Control Premium**
   - Market price: $50/share
   - Acquisition price: $65/share
   - What is the control premium?

3. **Real-World Application**
   - If ACME Distribution were acquired, what would be a reasonable valuation based on precedent transactions?

---

# Module 6: Leveraged Buyout (LBO) Modeling

## 6.1 Introduction to LBO Models

### Learning Objectives
- Understand the purpose of LBO models
- Identify the key components of an LBO
- Calculate returns on LBO investments

### Core Concepts

**What is an LBO?**
A leveraged buyout model answers one critical question: "If we buy this company today, how much money could we make when we sell it later?"

**How LBOs Work**
- Private equity firms borrow a significant portion of the purchase price
- The acquired company's cash flows are used to repay the debt
- The goal is to generate high returns on the equity invested

**The Five Steps of an LBO** (Harvard Business School)
1. **Project future earnings:** Estimate EBITDA at exit (typically 5 years)
2. **Select an exit multiple:** Based on comparable company valuations
3. **Calculate enterprise value:** EBITDA × Exit Multiple
4. **Determine equity value:** Enterprise Value - Remaining Debt
5. **Find the investor's share:** Equity Value × Ownership Stake

**Key Return Metrics**
- **Internal Rate of Return (IRR):** Annualized rate of return
- **Multiple of Money (MoM):** Total cash returned ÷ Total cash invested

### Practice Problems

1. **Basic LBO Calculation**
   - Purchase price: $500,000,000
   - Debt used: $350,000,000
   - Equity invested: $150,000,000
   - EBITDA at exit (Year 5): $100,000,000
   - Exit multiple: 8x
   - Remaining debt at exit: $200,000,000
   - Calculate: Exit Enterprise Value, Exit Equity Value, IRR, MoM

2. **Paper LBO**
   - Purchase price: $200,000,000
   - Debt: 60% of purchase price
   - EBITDA Year 1: $20,000,000, growing 10% annually
   - Exit multiple: 7x
   - Calculate returns (use approximations)

3. **Real-World Application**
   From the book: "The LBO model is used in the private equity industry to calculate the return on an investment for transactions such as buyouts, growth equity investments, investments in secondaries, and for some private credit transactions."
   - Build a full LBO model for a hypothetical acquisition.

---

# Module 7: Mergers & Acquisitions (M&A) Modeling

## 7.1 Introduction to M&A Models

### Learning Objectives
- Understand the purpose of M&A models
- Identify the key components of a merger model
- Analyze the impact of a transaction on shareholders

### Core Concepts

**What is an M&A Model?**
An M&A model analyzes the financial impact of a merger or acquisition, including:
- Accretion/dilution analysis (impact on EPS)
- Synergy analysis (cost savings and revenue enhancements)
- Purchase price allocation

**Components of a Merger Model**
1. **Assumptions:**
   - Buyer and target financials
   - Synergy assumptions
   - Purchase price and financing
2. **Transaction Calculations:**
   - Purchase price allocation
   - Sources and uses of funds
   - Goodwill creation

**Accretion/Dilution Analysis**
- **Accretive:** Transaction increases EPS
- **Dilutive:** Transaction decreases EPS
- **Breakeven:** EPS unchanged

### Practice Problems

1. **Accretion/Dilution**
   - Acquirer EPS: $2.00, Target EPS: $1.50
   - Exchange ratio: 0.8 shares of Acquirer for each Target share
   - What is the pro forma EPS?

2. **Synergy Analysis**
   - Cost synergies: $50,000,000
   - Revenue synergies: $30,000,000
   - Integration costs: $20,000,000
   - Tax rate: 30%
   - What is the net synergy value?

3. **Real-World Application**
   From the book: "Business valuation is the number one factor in determining a value of a business."
   - Model a merger between two companies in the same industry.

---

# Module 8: Specialized Modeling Applications

## 8.1 Real Estate Modeling

### Learning Objectives
- Understand real estate investment modeling
- Calculate key real estate metrics
- Build a real estate pro forma

### Core Concepts

**Key Real Estate Metrics**
- **Net Operating Income (NOI):** Revenue - Operating Expenses
- **Cap Rate:** NOI / Property Value
- **Cash-on-Cash Return:** Annual Cash Flow / Equity Invested
- **Debt Service Coverage Ratio (DSCR):** NOI / Debt Service

**Real Estate Pro Forma**
```
Gross Revenue
- Vacancy Allowance
= Effective Gross Revenue
- Operating Expenses
= Net Operating Income (NOI)
- Debt Service
= Cash Flow Before Tax
- Income Tax
= Cash Flow After Tax
```

### Practice Problems

1. **Real Estate Metrics**
   - Property Value: $10,000,000
   - NOI: $800,000
   - What is the Cap Rate?
   - If the Cap Rate is 8%, what is the property value?

2. **Real Estate Pro Forma**
   - 100 units at $1,500/month
   - Vacancy: 5%
   - Operating Expenses: 40% of EGR
   - Debt: $7,000,000 at 6% for 30 years
   - Equity: $3,000,000
   - Calculate: NOI, DSCR, Cash-on-Cash Return

3. **Real-World Application**
   - Evaluate a real estate investment opportunity using a full financial model.

## 8.2 Project Finance Modeling

### Learning Objectives
- Understand project finance modeling
- Build a project finance model
- Calculate project returns

### Core Concepts

**Project Finance Key Concepts**
- **Construction Phase:** Capital-intensive period with no revenue
- **Operating Phase:** Revenue generation begins
- **Debt Service:** Project cash flows repay debt

**Key Metrics**
- **Project IRR:** Return on the entire project
- **Equity IRR:** Return to equity investors
- **Debt Service Coverage Ratio (DSCR):** Cash Flow / Debt Service
- **Loan Life Coverage Ratio (LLCR):** PV of Cash Flow / Debt

### Practice Problems

1. **Project Finance**
   - Construction cost: $100,000,000
   - Operating cash flow: $15,000,000/year for 20 years
   - Construction: 2 years
   - Debt: 70% of cost at 7%
   - Calculate: Project IRR, Equity IRR

2. **DSCR Calculation**
   - Annual cash flow: $12,000,000
   - Annual debt service: $8,000,000
   - What is DSCR?

3. **Real-World Application**
   - Build a project finance model for a solar power plant.

---

# Module 9: Model Auditing and Quality Control

## 9.1 Model Auditing

### Learning Objectives
- Understand the importance of model auditing
- Identify common modeling errors
- Implement quality control procedures

### Core Concepts

**Common Modeling Errors**
1. **Hard-coded numbers** in formulas (instead of cell references)
2. **Circular references** (formulas that reference themselves)
3. **Inconsistent formulas** across rows or columns
4. **Wrong sign conventions** (positive vs. negative)
5. **Off-by-one errors** in timing
6. **Balance sheet not balancing**

**Auditing Checklist**
- [ ] All inputs are on a separate assumptions tab
- [ ] All formulas are consistent
- [ ] Balance sheet balances
- [ ] Cash flow statement reconciles
- [ ] No circular references
- [ ] No hard-coded numbers in formulas
- [ ] Sensitivity analysis works
- [ ] Scenarios switch correctly

### Practice Problems

1. **Error Identification**
   - Review a model and identify errors
   - Fix the errors and explain what was wrong

2. **Auditing Process**
   - Create an audit checklist for a three-statement model
   - Audit a sample model and document findings

3. **Real-World Application**
   From the book: "Financial reports should be based on correct accounting methods. And it should go without saying that financial statements should be fair and honest."
   - Audit a financial model for a real company and identify any issues.

---

# Module 10: Final Project

## Project: Complete Financial Model of a Public Company

### Requirements

Select a public company and build a complete financial model:

### Part 1: Data Gathering
- Download 5-10 years of historical financial statements
- Research the company's business model and key drivers
- Identify comparable companies for valuation

### Part 2: Model Building
- Build a three-statement model with 5-year forecasts
- Include supporting schedules (depreciation, debt, working capital)
- Build scenario analysis (base, best, worst)

### Part 3: Valuation
- Perform DCF valuation
- Perform comparable company analysis
- Perform precedent transaction analysis

### Part 4: Sensitivity Analysis
- Test key assumptions
- Create sensitivity tables
- Identify value drivers

### Part 5: Executive Summary
- Summarize key findings
- Include charts and graphs
- Make investment recommendation

### Part 6: Presentation
- Prepare a professional presentation
- Present to "investment committee"

---

# Course Summary and Next Steps

## Mathematical Concepts Used in Financial Modeling

| Module | Topic | Key Mathematical Concepts |
|--------|-------|--------------------------|
| 1 | Foundations | Accounting, financial statement analysis |
| 2 | Excel Skills | Functions, formulas, data validation |
| 3 | Three-Statement Model | Algebra, ratios, working capital |
| 4 | Advanced Techniques | Sensitivity analysis, scenario modeling |
| 5 | Valuation Methods | DCF, NPV, IRR, multiples |
| 6 | LBO Modeling | IRR, MoM, leverage calculations |
| 7 | M&A Modeling | Accretion/dilution, synergy analysis |
| 8 | Specialized Models | Real estate metrics, project finance |
| 9 | Auditing | Error checking, quality control |
| 10 | Final Project | Integration of all skills |

## Recommended Learning Path

1. **Start with simple, boring companies**
   - Pick a company with predictable revenue (Walmart, utility companies)
   - Watch someone else build the model first
   - Then try building it yourself from a template

2. **Practice, practice, practice**
   - Build models for different companies
   - Try different modeling scenarios
   - Test your assumptions

3. **Learn from others**
   - Review at least 3-4 examples of someone building a financial model
   - Study professional models
   - Get feedback on your models

4. **Move to more complex models**
   - After mastering basic models, try LBO and M&A models
   - Add more sophisticated scenario analysis
   - Incorporate Monte Carlo simulation

## Additional Resources

1. **CFA Institute Financial Modeling Module**
   - 10-20 hours of content
   - Build a presentation-ready model

2. **Corporate Finance Institute (CFI)**
   - Free and paid courses
   - Industry certification

3. **Breaking Into Wall Street**
   - Free tutorials and paid courses
   - Real-world examples

4. **Wall Street Prep**
   - Free three-statement model course
   - Professional templates

5. **NSE Academy Financial Modelling Course**
   - 12-hour self-paced course
   - Case study approach

---

# Comprehensive Financial Modeling Course: From Complete Novice to Pro

## A Step-by-Step Guide with Detailed Explanations and Examples

---

# Course Introduction

**Welcome!** This course is designed for people with **zero prior experience** in financial modeling. We start from the very beginning—assuming you don't even know what a balance sheet is—and build up step by step.

Think of this like learning a new language. At first, everything seems foreign. But with practice, it becomes natural.

### What You'll Learn

By the end of this course, you'll be able to:
- Understand financial statements and how they connect
- Build a complete 3-statement financial model in Excel
- Forecast a company's future performance
- Value a company using multiple methods
- Present your findings professionally

### How This Course Works

Each module has the same structure:
1. **Learning Objectives** - What you'll be able to do
2. **Core Concepts** - The theory explained in plain English
3. **Step-by-Step Excel Instructions** - Exactly what to click and type
4. **Practice Problems** - Exercises to reinforce learning
5. **Solutions** - Check your work

### What You'll Need

- **Microsoft Excel** (any recent version will work)
- **A calculator** (your phone works fine)
- **Patience and persistence** (this is a skill, not a talent)

---

# Module 1: Understanding Financial Statements

## 1.1 What Is a Financial Statement?

Think of a financial statement like a report card for a business. Just as your report card shows how you're doing in school, financial statements show how a business is performing and how healthy it is financially.

There are **three main financial statements**:
1. **Income Statement** (also called Profit & Loss, or P&L)
2. **Balance Sheet**
3. **Cash Flow Statement**

Let's understand each one.

---

## 1.2 The Income Statement (Profit & Loss)

### What It Shows

The income statement answers one simple question: **"Did the business make money?"**

It's like your personal budget:
- **Revenue** = Money coming in (like your salary)
- **Expenses** = Money going out (like rent, groceries)
- **Profit** = Revenue minus Expenses

### A Simple Example

Let's use a lemonade stand example:

| Item | Amount |
|------|--------|
| Revenue (Lemonade sales) | $100 |
| Cost of Lemons | $20 |
| Cost of Sugar | $10 |
| Cost of Cups | $5 |
| Total Expenses | $35 |
| **Profit** | **$65** |

This is the most basic income statement. Your business made $100, spent $35, and kept $65.

### A Real Business Example

Here's a simplified income statement for a real company:

**ACME Distribution, Inc. Income Statement**
**For the Year Ended December 31, 2010**

| Line Item | Amount |
|-----------|--------|
| Revenue (Sales) | $8,043,750 |
| Cost of Goods Sold (COGS) | $6,032,813 |
| **Gross Profit** | **$2,010,937** |
| Selling, General & Admin Expenses | $1,395,000 |
| Depreciation Expense | $250,000 |
| Interest Expense | $125,938 |
| Other Expenses | $50,000 |
| **Net Profit Before Tax** | **$190,000** |
| Income Tax Expense | $0 |
| **Net Profit (Net Income)** | **$190,000** |

### Key Terms Explained

**Revenue (Sales)**
- Money from selling products or services
- In the lemonade stand: money from selling lemonade

**Cost of Goods Sold (COGS)**
- Direct cost of making or buying what you sell
- In the lemonade stand: lemons, sugar, cups

**Gross Profit**
- Revenue minus COGS
- Shows profit before paying for other expenses
- In the lemonade stand: $100 - $35 = $65

**Operating Expenses (SG&A)**
- Costs of running the business (rent, salaries, advertising)
- Also called selling, general, and administrative expenses

**Depreciation**
- Non-cash expense for using long-term assets
- Example: If a delivery truck costs $100,000 and lasts 10 years, each year's depreciation is $10,000

**Interest Expense**
- Cost of borrowing money

**Net Income (Profit)**
- The "bottom line"
- What's left after all expenses

### Key Insight

> **From the book**: "Profit is the excess of revenue over expenses (and loss is the excess of expenses over revenue)."

---

## 1.3 The Balance Sheet

### What It Shows

The balance sheet answers: **"What does the business own, and what does it owe?"**

Think of it as a snapshot of the business at one specific moment in time (like a photograph).

The balance sheet follows one simple formula:

```
Assets = Liabilities + Owner's Equity
```

**Assets** = What the business owns (cash, inventory, equipment)
**Liabilities** = What the business owes (loans, unpaid bills)
**Owner's Equity** = What's left for the owners

### A Simple Example

Your lemonade stand balance sheet on July 1:

**Assets:**
- Cash in drawer: $100
- Lemons: $20
- Cups: $5
- **Total Assets: $125**

**Liabilities:**
- Money borrowed from mom: $50
- **Total Liabilities: $50**

**Owner's Equity:**
- Your investment: $75
- **Total Equity: $75**

Check: $125 = $50 + $75 ✓

### A Real Business Example

**ACME Distribution, Inc. Balance Sheet**
**December 31, 2010**

| Assets | Amount | Liabilities & Equity | Amount |
|--------|--------|---------------------|--------|
| Cash | $230,000 | Accounts Payable | $385,000 |
| Accounts Receivable | $705,000 | Accrued Liabilities | $215,000 |
| Inventory | $450,000 | Line of Credit | $350,000 |
| Prepaid Expenses | $75,000 | Current Debt | $250,000 |
| **Total Current Assets** | **$1,460,000** | **Total Current Liabilities** | **$1,275,000** |
| | | | |
| Property, Plant & Equipment | $2,140,000 | Notes Payable | $800,000 |
| Accumulated Depreciation | ($800,000) | Capital Leases | $100,000 |
| Net PP&E | $1,340,000 | Subordinated Debt | $250,000 |
| | | **Total Long-Term Liabilities** | **$1,150,000** |
| Other Assets | $470,000 | | |
| | | **Total Liabilities** | **$2,425,000** |
| | | | |
| | | Common Equity | $100,000 |
| | | Retained Earnings | $555,000 |
| | | Current Earnings | $190,000 |
| | | **Total Equity** | **$845,000** |
| **Total Assets** | **$3,270,000** | **Total Liabilities & Equity** | **$3,270,000** |

### Key Terms Explained

**Assets (What the company owns)**

**Cash** - Money in bank accounts
**Accounts Receivable** - Money customers owe the business
**Inventory** - Products the business has to sell
**Prepaid Expenses** - Things paid for in advance (like insurance)
**Property, Plant & Equipment (PP&E)** - Long-term assets (buildings, machines, vehicles)
**Accumulated Depreciation** - Total depreciation taken so far (reduces asset value)

**Liabilities (What the company owes)**

**Accounts Payable** - Bills the business hasn't paid yet
**Accrued Liabilities** - Expenses incurred but not yet paid (like wages owed)
**Line of Credit** - Short-term borrowing from a bank
**Current Debt** - Portion of long-term debt due within one year
**Notes Payable** - Long-term loans from banks

**Equity (Owner's stake)**

**Common Equity** - Money owners invested
**Retained Earnings** - Profits kept in the business (not paid to owners)

### Balance Sheet Rules

1. **Assets are on the left**, liabilities and equity on the right
2. **Current assets** = expected to be used or converted to cash within one year
3. **Current liabilities** = expected to be paid within one year
4. **Total Assets MUST equal Total Liabilities + Total Equity**
5. **The balance sheet is a snapshot** (at a specific date)

---

## 1.4 The Cash Flow Statement

### What It Shows

The cash flow statement answers: **"Where did cash come from, and where did it go?"**

This is crucial because **profit doesn't equal cash flow**. A company can show a profit but have no cash!

> **From the book**: "Earning a profit does not mean that the business's cash balance went up the same amount."

### Three Categories of Cash Flow

1. **Operating Activities** - Cash from daily business operations
2. **Investing Activities** - Cash from buying/selling long-term assets
3. **Financing Activities** - Cash from borrowing or repaying debt, and from owners

### A Simple Example

Your lemonade stand cash flow:

| Cash Flow Type | Amount |
|----------------|--------|
| Cash from customers | $100 |
| Cash paid for supplies | ($35) |
| **Net Cash from Operations** | **$65** |
| Cash spent on new stand | ($20) |
| **Net Cash from Investing** | **($20)** |
| Cash borrowed from mom | $50 |
| **Net Cash from Financing** | **$50** |
| **Total Change in Cash** | **$95** |

This means cash increased by $95 during the period.

### A Real Business Example

**ACME Distribution, Inc. Cash Flow Statement**
**For the Year Ended December 31, 2010**

| Item | Amount |
|------|--------|
| **Operating Activities** | |
| Net Income | $190,000 |
| Depreciation | $250,000 |
| Increase in A/R | ($69,130) |
| Increase in Inventory | ($50,000) |
| Increase in A/P | ($115,000) |
| **Net Cash from Operations** | **$440,000** |
| | |
| **Investing Activities** | |
| Fixed Asset Additions | $0 |
| Change in Other Assets | $30,000 |
| **Net Cash from Investing** | **$220,000** |
| | |
| **Financing Activities** | |
| Debt Repayments | ($250,000) |
| **Net Cash from Financing** | **($220,000)** |
| | |
| **Net Change in Cash** | **$175,869** |
| **Beginning Cash** | **$54,131** |
| **Ending Cash** | **$230,000** |

### Key Insight

> **From the book**: "Understanding the difference between profit and cash flow is extremely important. Many business managers confuse profit and cash flow, which can have serious consequences."

---

## 1.5 How the Statements Connect

### The Big Picture

The three statements are like a puzzle that fits together. Here's how they connect:

1. **Net Income** from the Income Statement goes to:
   - The Cash Flow Statement (as starting point for operating cash flow)
   - The Balance Sheet (as an increase to Retained Earnings)

2. **Changes in Balance Sheet items** (like A/R, Inventory, A/P) go to:
   - The Cash Flow Statement (as adjustments to net income)

3. **Cash** from the Cash Flow Statement goes to:
   - The Balance Sheet (as ending cash balance)

### Visual Connection

```
Income Statement
     ↓
Net Income
     ↓     ↓
Cash Flow    Balance Sheet
Statement    (Retained Earnings)
     ↓
Cash Ending
     ↓
Balance Sheet
(Cash Balance)
```

### Practice Exercise

For the practice problems below, use these company financials:

**XYZ Company Income Statement (Year Ended 12/31/23)**

| Item | Amount |
|------|--------|
| Revenue | $1,000,000 |
| COGS | $600,000 |
| Gross Profit | $400,000 |
| Operating Expenses | $250,000 |
| Depreciation | $50,000 |
| Interest Expense | $20,000 |
| Net Profit Before Tax | $80,000 |
| Taxes (30%) | $24,000 |
| **Net Income** | **$56,000** |

**XYZ Company Balance Sheet (12/31/23 compared to 12/31/22)**

| Item | 2022 | 2023 | Change |
|------|------|------|--------|
| Cash | $100,000 | $? | ? |
| A/R | $150,000 | $180,000 | +$30,000 |
| Inventory | $200,000 | $190,000 | -$10,000 |
| PP&E (Net) | $500,000 | $550,000 | +$50,000 |
| **Total Assets** | **$950,000** | **?** | |
| A/P | $120,000 | $140,000 | +$20,000 |
| Debt | $300,000 | $300,000 | $0 |
| Equity | $530,000 | $? | |
| **Total L+E** | **$950,000** | **?** | |

---

## Practice Problems - Module 1

### Problem 1: Income Statement

A business has $500,000 in revenue and $300,000 in COGS. What is gross profit?

### Problem 2: Balance Sheet

A company has $800,000 in assets and $350,000 in liabilities. What is owner's equity?

### Problem 3: Cash Flow

Net income is $50,000. Depreciation is $10,000. A/R increases by $5,000. A/P increases by $3,000. What is cash from operations?

### Problem 4: Statement Connections

Using the XYZ Company data above:
1. What is the ending balance sheet total?
2. What is ending equity?
3. What is ending cash?
4. Why does net income not equal cash?

---

## Solutions - Module 1

### Problem 1
Gross Profit = Revenue - COGS = $500,000 - $300,000 = **$200,000**

### Problem 2
Owner's Equity = Assets - Liabilities = $800,000 - $350,000 = **$450,000**

### Problem 3
Cash from Operations = Net Income + Depreciation - Increase in A/R + Increase in A/P
= $50,000 + $10,000 - $5,000 + $3,000 = **$58,000**

### Problem 4

1. **Total Assets (2023)** = Cash + A/R + Inventory + PP&E (net)
   But we need to find cash first...

2. **Ending Equity** = Beginning Equity + Net Income - Dividends (assuming no dividends)
   = $530,000 + $56,000 = **$586,000**

3. **Total Liabilities + Equity** = A/P + Debt + Equity
   = $140,000 + $300,000 + $586,000 = **$1,026,000**

4. **Total Assets** = Total Liabilities + Equity = **$1,026,000**

5. **Cash** = Total Assets - A/R - Inventory - PP&E
   = $1,026,000 - $180,000 - $190,000 - $550,000 = **$106,000**

6. **Net income ($56,000) ≠ Cash increase ($6,000)** because:
   - $30,000 increase in A/R uses cash
   - $10,000 decrease in inventory provides cash
   - $20,000 increase in A/P provides cash
   - $50,000 depreciation doesn't use cash
   - $50,000 spent on PP&E uses cash
   Net effect = -$30,000 + $10,000 + $20,000 + $50,000 - $50,000 = $0
   So cash only increased by $6,000

---

## Module 1 Summary

### Key Takeaways

1. **The Income Statement** shows if a business made a profit
   - Revenue minus Expenses = Profit

2. **The Balance Sheet** shows what a business owns and owes
   - Assets = Liabilities + Equity (must always balance!)

3. **The Cash Flow Statement** shows where cash comes from and goes
   - Operating + Investing + Financing = Change in Cash

4. **The three statements are interconnected** and must reconcile

### Key Vocabulary

| Term | Definition |
|------|------------|
| Revenue | Money from sales |
| COGS | Direct cost of goods sold |
| Gross Profit | Revenue minus COGS |
| Operating Expenses | Business operating costs |
| Net Income | Profit after all expenses |
| Assets | What the company owns |
| Liabilities | What the company owes |
| Equity | Owner's stake |
| A/R | Money customers owe |
| A/P | Money the company owes |
| Depreciation | Non-cash expense for asset use |

---

# Module 2: Excel Basics for Financial Modeling

## 2.1 Getting Started with Excel

### What is Excel?

Excel is a spreadsheet program. Think of it like a giant table with rows and columns. Each box (called a "cell") can hold:
- Numbers
- Text
- Formulas (calculations)

### Excel's Grid

```
     A      B      C      D
1    _____  _____  _____  _____
2    _____  _____  _____  _____
3    _____  _____  _____  _____
4    _____  _____  _____  _____
```

- **Columns** are letters (A, B, C...)
- **Rows** are numbers (1, 2, 3...)
- **Cells** are combinations (A1, B2, C3...)
- We write formulas in cells

---

## 2.2 Essential Excel Skills

### Basic Navigation

| Action | How To |
|--------|--------|
| Select a cell | Click on it |
| Enter data | Type and press Enter |
| Edit a cell | Double-click or press F2 |
| Move between cells | Arrow keys |
| Select a range | Click and drag |

### Basic Math Operations

| Operation | Symbol | Example |
|-----------|--------|---------|
| Addition | + | =A1+B1 |
| Subtraction | - | =A1-B1 |
| Multiplication | * | =A1*B1 |
| Division | / | =A1/B1 |
| Power | ^ | =A1^2 |

### Important Excel Rules

1. **Every formula starts with an equals sign (=)**
2. **Use cell references, not hard-coded numbers** in formulas
3. **Copy formulas down** to save time
4. **Color code your work** (blue = inputs, black = formulas)

---

## 2.3 Building Your First Model

### Step 1: Set Up Your Worksheet

Open Excel and create a new blank workbook.

**We'll build a simple income statement.**

1. In cell A1, type: "MY FIRST FINANCIAL MODEL"
2. In cell A3, type: "INCOME STATEMENT"
3. In cell A5, type: "Revenue"
4. In cell A6, type: "COGS"
5. In cell A7, type: "Gross Profit"
6. In cell A8, type: "Operating Expenses"
7. In cell A9, type: "Net Income"

### Step 2: Add Inputs

In cell B5, enter: 1000000 (this is our revenue)
In cell B6, enter: 600000 (this is our COGS)
In cell B8, enter: 250000 (this is our operating expenses)

### Step 3: Write Formulas

In cell B7, type: **=B5-B6**
This calculates Gross Profit = Revenue - COGS
Press Enter. You should see 400000.

In cell B9, type: **=B7-B8**
This calculates Net Income = Gross Profit - Operating Expenses
Press Enter. You should see 150000.

### Step 4: Format Your Model

1. Select cells B5:B9
2. Click the "$" symbol in the Number group on the Home tab
3. This formats numbers as currency

### Step 5: Test Your Model

Change cell B5 to 1200000 (increase revenue by 20%)
Notice that B7 and B9 automatically update.

### Why This Matters

You've just built your first financial model! Whenever you change an input (like revenue), all the calculations update automatically.

---

## 2.4 Essential Excel Functions for Modeling

### 1. SUM - Adding Things Up

Adds a range of numbers.

**Example:** Sum all expenses
```
=SUM(B2:B10)
```

### 2. AVERAGE - Finding the Mean

Calculates the average of a range.

**Example:** Average of 3 years of revenue
```
=AVERAGE(B2:D2)
```

### 3. IF - Making Decisions

Returns different values based on a condition.

**Format:** =IF(condition, value_if_true, value_if_false)

**Example:** If profit > 0, say "Profitable"; if not, say "Loss"
```
=IF(B9>0,"Profitable","Loss")
```

### 4. VLOOKUP - Finding Information

Finds a value in a table.

**Example:** Find the price of an item in a price list
```
=VLOOKUP(A2,Price_Table,2,FALSE)
```

### 5. NPV - Net Present Value

Calculates the present value of future cash flows.

**Example:** PV of $10,000 per year for 3 years at 10%
```
=NPV(0.10,10000,10000,10000)
```

### 6. IRR - Internal Rate of Return

Calculates the rate of return for a series of cash flows.

**Example:** IRR for a $100,000 investment with $40,000 annual returns for 3 years
```
=IRR(-100000,40000,40000,40000)
```

---

## 2.5 Practice Building

### Exercise 1: Simple Income Statement

Build an income statement with:
- Revenue = 2,500,000
- COGS = 1,500,000
- Operating Expenses = 600,000
- Interest Expense = 50,000
- Taxes = 40% of pre-tax profit

### Exercise 2: Simple Balance Sheet

Build a balance sheet with:
- Cash = 300,000
- A/R = 500,000
- Inventory = 400,000
- A/P = 200,000
- Debt = 600,000
- Equity = ?

Make sure Assets = Liabilities + Equity

### Exercise 3: Simple Cash Flow

Build a cash flow statement with:
- Net Income = 200,000
- Depreciation = 50,000
- Increase in A/R = 30,000
- Decrease in Inventory = 20,000
- Increase in A/P = 15,000
- CAPEX = 100,000
- Debt Repayment = 50,000

Calculate:
1. Cash from Operations
2. Cash from Investing
3. Cash from Financing
4. Net Change in Cash

---

## Solutions - Module 2

### Exercise 1

| Item | Formula | Result |
|------|---------|--------|
| Revenue | 2,500,000 | 2,500,000 |
| COGS | 1,500,000 | 1,500,000 |
| Gross Profit | =B5-B6 | 1,000,000 |
| Operating Exp | 600,000 | 600,000 |
| EBIT | =B7-B8 | 400,000 |
| Interest | 50,000 | 50,000 |
| Pre-Tax Profit | =B9-B10 | 350,000 |
| Taxes (40%) | =B11*0.4 | 140,000 |
| Net Income | =B11-B12 | 210,000 |

### Exercise 2

| Item | Formula | Result |
|------|---------|--------|
| Cash | 300,000 | 300,000 |
| A/R | 500,000 | 500,000 |
| Inventory | 400,000 | 400,000 |
| Total Assets | =SUM(B2:B4) | 1,200,000 |
| | | |
| A/P | 200,000 | 200,000 |
| Debt | 600,000 | 600,000 |
| Equity | =B8-B9 | 400,000 |
| Total Liab+Equity | =SUM(B8:B10) | 1,200,000 |

### Exercise 3

| Item | Formula | Result |
|------|---------|--------|
| Net Income | 200,000 | 200,000 |
| Depreciation | 50,000 | 50,000 |
| Inc in A/R | -30,000 | -30,000 |
| Dec in Inventory | 20,000 | 20,000 |
| Inc in A/P | 15,000 | 15,000 |
| Cash from Operations | =SUM(B2:B6) | 255,000 |
| CAPEX | -100,000 | -100,000 |
| Cash from Investing | =B8 | -100,000 |
| Debt Repayment | -50,000 | -50,000 |
| Cash from Financing | =B10 | -50,000 |
| **Net Change in Cash** | =B7+B9+B11 | **105,000** |

---

## Module 2 Summary

### Key Takeaways

1. **Every formula starts with an equals sign (=)** - This is the most important rule!
2. **Use cell references** - Never type numbers into formulas
3. **Color code your work** - Blue for inputs, black for formulas
4. **Test your model** - Change inputs to make sure everything updates
5. **Start simple** - You can always add complexity later

### Excel Functions to Remember

| Function | What It Does |
|----------|--------------|
| =SUM() | Adds numbers |
| =AVERAGE() | Finds the average |
| =IF() | Makes decisions |
| =VLOOKUP() | Finds information |
| =NPV() | Calculates present value |
| =IRR() | Calculates rate of return |

---

# Module 3: Building a 3-Statement Model

## 3.1 Overview of the 3-Statement Model

### What Is a 3-Statement Model?

A 3-statement model is a complete financial model that includes:
1. **Income Statement** (forecast)
2. **Balance Sheet** (forecast)
3. **Cash Flow Statement** (forecast)

These three statements are linked together so that:
- Changes in the Income Statement flow to the Balance Sheet
- Changes in the Balance Sheet flow to the Cash Flow Statement
- Changes in Cash flow back to the Balance Sheet

### Why This Matters

> **From the book**: "The three financial statements fit together like pieces in a puzzle."

When you build a 3-statement model, you're creating a complete picture of a company's finances. This is the foundation of all financial analysis.

---

## 3.2 Step-by-Step Model Building

### The Company We'll Model

Let's model ACME Distribution, Inc. We'll use the historical data from the book and project it forward.

### Step 1: Set Up the Workbook

**Create a new Excel workbook** with these tabs:
1. **Assumptions** (all inputs go here)
2. **Income Statement** (forecast)
3. **Balance Sheet** (forecast)
4. **Cash Flow** (forecast)
5. **Supporting Schedules** (depreciation, debt, etc.)
6. **Output** (summary charts)

### Step 2: The Assumptions Tab

This is the most important sheet. ALL inputs go here.

**Set up the Assumptions tab:**

| Cell | Label | Value | Description |
|------|-------|-------|-------------|
| B2 | Revenue Growth | 10.0% | Annual revenue growth |
| B3 | Gross Margin | 25.0% | Gross profit as % of revenue |
| B4 | SG&A % Revenue | 17.5% | SG&A as % of revenue |
| B5 | DSO | 45 | Days sales outstanding |
| B6 | DIO | 60 | Days inventory outstanding |
| B7 | DPO | 30 | Days payable outstanding |
| B8 | Tax Rate | 30.0% | Effective tax rate |
| B9 | CAPEX Growth | 5.0% | Annual CAPEX growth |
| B10 | Depreciation Life | 10 | Years to depreciate assets |

**Color coding**: Make input cells BLUE (fill color) to distinguish them from formulas.

### Step 3: The Income Statement Tab

**Set up the Income Statement:**

| Cell | Label | Formula |
|------|-------|---------|
| A5 | Year | |
| B5 | 2022 (Historical) | |
| C5 | 2023 | |
| D5 | 2024 | |
| E5 | 2025 | |
| F5 | 2026 | |
| G5 | 2027 | |

**Row 6-10: Revenue Section**

| Row | Label | 2022 Formula | 2023 Formula |
|-----|-------|--------------|--------------|
| 6 | Revenue | Enter actual | =F6*(1+Assumptions!B2) |
| 7 | COGS | Enter actual | =F6*(1-Assumptions!B3) |
| 8 | Gross Profit | =F6-F7 | =F6-F7 |
| 9 | Gross Margin | =F8/F6 | =F8/F6 |

**Row 11-15: Expense Section**

| Row | Label | 2022 Formula | 2023 Formula |
|-----|-------|--------------|--------------|
| 11 | SG&A | Enter actual | =F6*Assumptions!B4 |
| 12 | Depreciation | Enter actual | From depreciation schedule |
| 13 | Interest Expense | Enter actual | From debt schedule |
| 14 | Other Expense | Enter actual | =F14 (assume same) |
| 15 | Total Expenses | =SUM(F11:F14) | =SUM(F11:F14) |

**Row 16-18: Profit Section**

| Row | Label | 2022 Formula | 2023 Formula |
|-----|-------|--------------|--------------|
| 16 | EBIT | =F8-F15 | =F8-F15 |
| 17 | Pre-Tax Profit | =F16 | =F16 |
| 18 | Taxes | =F17*Assumptions!B8 | =F17*Assumptions!B8 |
| 19 | Net Income | =F17-F18 | =F17-F18 |

### Step 4: Supporting Schedule - Depreciation

**Create a Depreciation schedule:**

| Cell | Label | Formula |
|------|-------|---------|
| A25 | Opening PP&E | from Balance Sheet |
| A26 | CAPEX | =Assumptions!B9*previous CAPEX |
| A27 | Depreciation | =A28/Assumptions!B10 |
| A28 | Closing PP&E | =A25 + A26 - A27 |

### Step 5: The Balance Sheet Tab

**Set up the Balance Sheet:**

| Cell | Label | 2022 Formula | 2023 Formula |
|------|-------|--------------|--------------|
| B30 | Cash | from Cash Flow | from Cash Flow |
| B31 | A/R | =F6*Assumptions!B5/365 | =G6*Assumptions!B5/365 |
| B32 | Inventory | =F7*Assumptions!B6/365 | =G7*Assumptions!B6/365 |
| B33 | Prepaids | =F33 (assume same) | =G33 (assume same) |
| B34 | Total Current Assets | =SUM(B30:B33) | =SUM(B30:B33) |
| B35 | PP&E (net) | from Depreciation | from Depreciation |
| B36 | Other Assets | =F36 (assume same) | =G36 (assume same) |
| B37 | **Total Assets** | **=SUM(B34:B36)** | **=SUM(B34:B36)** |
| | | | |
| B40 | A/P | =F32*Assumptions!B7/365 | =G32*Assumptions!B7/365 |
| B41 | Accrued Liab | =F41 (assume same) | =G41 (assume same) |
| B42 | Current Debt | from Debt schedule | from Debt schedule |
| B43 | Total Current Liabilities | =SUM(B40:B42) | =SUM(B40:B42) |
| B44 | Long-Term Debt | from Debt schedule | from Debt schedule |
| B45 | Other Liabilities | =F45 (assume same) | =G45 (assume same) |
| B46 | **Total Liabilities** | **=SUM(B43:B45)** | **=SUM(B43:B45)** |
| | | | |
| B48 | Common Equity | =F48 | =G48 |
| B49 | Retained Earnings | =F49 + Net Income | =F49 + Net Income |
| B50 | **Total Equity** | **=SUM(B48:B49)** | **=SUM(B48:B49)** |
| B51 | **Total Liab + Equity** | **=B46+B50** | **=B46+B50** |

### Step 6: The Cash Flow Statement

**Set up the Cash Flow Statement:**

| Cell | Label | 2022 Formula | 2023 Formula |
|------|-------|--------------|--------------|
| B55 | Net Income | from Income Statement | from Income Statement |
| B56 | Depreciation | from Depreciation sch | from Depreciation sch |
| B57 | Change in A/R | =-(B31-F31) | =-(C31-B31) |
| B58 | Change in Inventory | =-(B32-F32) | =-(C32-B32) |
| B59 | Change in A/P | =B40-F40 | =C40-B40 |
| B60 | Change in Accruals | =B41-F41 | =C41-B41 |
| B61 | Cash from Operations | =SUM(B55:B60) | =SUM(B55:B60) |
| | | | |
| B63 | CAPEX | from Depreciation | from Depreciation |
| B64 | Cash from Investing | =B63 | =B63 |
| | | | |
| B66 | New Debt | from Debt schedule | from Debt schedule |
| B67 | Debt Repayment | from Debt schedule | from Debt schedule |
| B68 | Cash from Financing | =B66+B67 | =B66+B67 |
| | | | |
| B70 | Total Change in Cash | =B61+B64+B68 | =B61+B64+B68 |
| B71 | Beginning Cash | from Balance Sheet | =B70+B71 |
| B72 | Ending Cash | =B70+B71 | =B70+B71 |

### Step 7: The "Plug" - Making It Balance

**The hard part**: The balance sheet must balance. If it doesn't, we need a "plug."

Common plugs:
1. **Cash** - Let cash be the balancing figure
2. **Revolver** - Short-term borrowing
3. **Equity** - New equity issuance

**For ACME, we'll use Cash as the plug:**

In the Cash Flow Statement, set Ending Cash = Balance Sheet Cash (make both formulas reference the same cell).

If the model doesn't balance, adjust the plug until it does.

---

## 3.3 Detailed Walkthrough

### Entering Historical Data

Start by entering ACME's historical data from the book:

**Historical Income Statement (2022)**

| Item | Amount |
|------|--------|
| Revenue | $8,043,750 |
| COGS | $6,032,813 |
| Gross Profit | $2,010,937 |
| SG&A | $1,395,000 |
| Depreciation | $250,000 |
| Interest | $125,938 |
| Other | $50,000 |
| Pre-Tax Profit | $190,000 |
| Taxes | $0 |
| Net Income | $190,000 |

**Historical Balance Sheet (2022)**

| Asset | Amount | Liability/Equity | Amount |
|-------|--------|------------------|--------|
| Cash | $230,000 | A/P | $385,000 |
| A/R | $705,000 | Accruals | $215,000 |
| Inventory | $450,000 | Line of Credit | $350,000 |
| Prepaids | $75,000 | Current Debt | $250,000 |
| PP&E (net) | $1,340,000 | Long-Term Debt | $1,150,000 |
| Other Assets | $470,000 | Common Equity | $100,000 |
| | | Retained Earnings | $555,000 |
| Total Assets | $3,270,000 | Total L+E | $3,270,000 |

### Forecasting Assumptions

| Assumption | Value | Rationale |
|------------|-------|-----------|
| Revenue Growth | 10% | Company expects market growth |
| Gross Margin | 25% | Historical level maintained |
| SG&A % Revenue | 17.5% | Slight improvement from 17.3% |
| DSO | 45 days | Current A/R collection time |
| DIO | 60 days | Current inventory holding time |
| DPO | 30 days | Current payment time |
| Tax Rate | 30% | Normal corporate tax rate |
| CAPEX Growth | 5% | Gradual capacity expansion |
| Depreciation Life | 10 years | Weighted average asset life |

---

## Practice Problems - Module 3

### Problem 1: Revenue Forecast

Using the assumptions, forecast revenue for 2023-2027:
- 2022 Revenue = $8,043,750
- Growth = 10% per year

### Problem 2: A/R Forecast

Calculate A/R for each forecast year:
- Use DSO = 45 days
- Hint: A/R = Revenue × (DSO/365)

### Problem 3: Gross Profit Forecast

Calculate Gross Profit for each forecast year:
- Gross Margin = 25%

### Problem 4: Complete the Model

Using all the steps above, complete the full 3-statement model for ACME Distribution.

---

## Solutions - Module 3

### Problem 1

| Year | Formula | Result |
|------|---------|--------|
| 2022 | Actual | $8,043,750 |
| 2023 | =8,043,750*1.10 | $8,848,125 |
| 2024 | =8,848,125*1.10 | $9,732,938 |
| 2025 | =9,732,938*1.10 | $10,706,231 |
| 2026 | =10,706,231*1.10 | $11,776,854 |
| 2027 | =11,776,854*1.10 | $12,954,539 |

### Problem 2

| Year | Revenue | DSO/365 | A/R |
|------|---------|---------|-----|
| 2023 | $8,848,125 | 0.1233 | $1,091,000 |
| 2024 | $9,732,938 | 0.1233 | $1,200,000 |
| 2025 | $10,706,231 | 0.1233 | $1,320,000 |
| 2026 | $11,776,854 | 0.1233 | $1,452,000 |
| 2027 | $12,954,539 | 0.1233 | $1,597,000 |

### Problem 3

| Year | Revenue | Gross Margin | Gross Profit |
|------|---------|--------------|--------------|
| 2023 | $8,848,125 | 25% | $2,212,031 |
| 2024 | $9,732,938 | 25% | $2,433,234 |
| 2025 | $10,706,231 | 25% | $2,676,558 |
| 2026 | $11,776,854 | 25% | $2,944,214 |
| 2027 | $12,954,539 | 25% | $3,238,635 |

### Problem 4: Complete Model Summary

**Income Statement (2023)**

| Item | Amount |
|------|--------|
| Revenue | $8,848,125 |
| COGS | $6,636,094 |
| Gross Profit | $2,212,031 |
| SG&A (17.5%) | $1,548,422 |
| Depreciation | $275,000 |
| Interest | $125,000 |
| Other | $50,000 |
| Pre-Tax Profit | $213,609 |
| Taxes (30%) | $64,083 |
| Net Income | $149,526 |

**Balance Sheet (2023)**

| Asset | Amount | Liability | Amount |
|-------|--------|-----------|--------|
| Cash | $286,612 | A/P | $588,647 |
| A/R | $1,091,000 | Accruals | $215,000 |
| Inventory | $1,090,865 | Current Debt | $250,000 |
| Prepaids | $75,000 | Line of Credit | $350,000 |
| PP&E | $1,415,000 | Long-Term Debt | $1,150,000 |
| Other Assets | $470,000 | Equity | $648,830 |
| Total | $4,428,477 | Total | $4,428,477 |

---

## Module 3 Summary

### Key Takeaways

1. **The 3-statement model is the foundation** of all financial analysis
2. **Start with the Income Statement**, then Balance Sheet, then Cash Flow
3. **Use supporting schedules** for depreciation and debt
4. **The model must balance** - Assets must equal Liabilities + Equity
5. **Cash is often the plug** that makes it balance

### The Model Flow

```
Assumptions → Income Statement → Balance Sheet → Cash Flow
                    ↓                  ↓              ↓
               Net Income        Working Capital    Cash
                    ↓                  ↓              ↓
                Retained            Debt/Equity    Cash Balance
                Earnings              Changes       (balances BS)
```

---

# Module 4: Forecasting and Sensitivity Analysis

## 4.1 Understanding Forecasts

### What Is Forecasting?

Forecasting is predicting what will happen in the future. In financial modeling, we forecast:
- Revenue
- Expenses
- Assets
- Liabilities
- Cash Flow

### Types of Forecasts

1. **Short-term** (1-3 months) - Detailed, specific
2. **Medium-term** (1-3 years) - Broader assumptions
3. **Long-term** (5-10 years) - Strategic, high-level

> **From the book**: "The nearer-term the projection, the more detailed the information and results being produced."

---

## 4.2 Revenue Forecasting Methods

### Method 1: Historical Growth

Apply past growth rates to the future.

**Example**: Revenue grew 10% last year. Forecast 10% growth for the next 5 years.

**Formula**: =Revenue_Prior × (1 + Growth_Rate)

### Method 2: Top-Down (Market Share)

Start with the total market size and estimate market share.

**Example**:
- Total market = $100,000,000
- Company market share = 10%
- Revenue = $100,000,000 × 10% = $10,000,000

### Method 3: Bottom-Up (Unit Sales)

Multiply expected unit sales by price.

**Example**:
- Units sold = 10,000
- Price per unit = $100
- Revenue = 10,000 × $100 = $1,000,000

### Method 4: Driver-Based

Link revenue to key business drivers.

**Example** (Software company):
- Customers = 1,000
- Average revenue per customer = $5,000/year
- Revenue = 1,000 × $5,000 = $5,000,000

---

## 4.3 Expense Forecasting

### Variable Expenses

Change with revenue.

**Examples**: COGS, Sales commissions

**Forecast**: Variable Expense = Revenue × % of Revenue

### Fixed Expenses

Don't change with revenue.

**Examples**: Rent, Salaries

**Forecast**: Fixed Expense = Prior Period × (1 + Inflation)

### Semi-Variable Expenses

Partially change with revenue.

**Example**: Utility costs, Some labor costs

**Forecast**: Fixed component + Variable component

---

## 4.4 Scenario Analysis

### What Is Scenario Analysis?

Testing different "what if" scenarios to see how results change.

### Common Scenarios

1. **Base Case** - Most likely outcome
2. **Best Case** - Optimistic assumptions
3. **Worst Case** - Pessimistic assumptions

### How to Build Scenarios

**Step 1**: Create an assumptions table with scenario switches.

**Step 2**: Use Excel's CHOOSE function to switch between scenarios.

**Example**:
```
=CHOOSE(Scenario_Number, Base_Revenue, Best_Revenue, Worst_Revenue)
```

Where Scenario_Number = 1 for Base, 2 for Best, 3 for Worst

### Practice: Building Scenarios

**ACME Distribution Scenarios**

| Assumption | Base | Best | Worst |
|------------|------|------|-------|
| Revenue Growth | 10% | 20% | 5% |
| Gross Margin | 25% | 28% | 22% |
| SG&A % Revenue | 17.5% | 16.0% | 19.0% |
| DSO | 45 days | 40 days | 50 days |
| DIO | 60 days | 55 days | 65 days |
| DPO | 30 days | 35 days | 25 days |
| CAPEX Growth | 5% | 10% | 2% |

---

## 4.5 Sensitivity Analysis

### What Is Sensitivity Analysis?

Testing how changes in one assumption affect the result.

### The Goal

Identify which assumptions have the biggest impact.

### How to Build a Sensitivity Table

**Step 1**: Create a data table with the output you want to test.

**Example**: How does Net Income change with different revenue growth and gross margin?

**Step 2**: Set up the table in Excel.

```
     |   10%   12%   14%   16%   18%   20%   ← Revenue Growth
-----|--------------------------------------
22%  |   X1    X2    X3    X4    X5    X6   ← Gross Margin
23%  |   X7    X8    X9    X10   X11   X12
24%  |   X13   X14   X15   X16   X17   X18
25%  |   X19   X20   X21   X22   X23   X24
26%  |   X25   X26   X27   X28   X29   X30
27%  |   X31   X32   X33   X34   X35   X36
```

**Step 3**: Use Excel's Data Table function.

1. Select the table
2. Go to Data → What-If Analysis → Data Table
3. Set Row input cell = Revenue Growth
4. Set Column input cell = Gross Margin

---

## Practice Problems - Module 4

### Problem 1: Revenue Forecasting

A company has 500 customers paying $1,000 per month. Customer churn is 5% per year. New customers are added at 10% per year.

Forecast revenue for 3 years.

### Problem 2: Scenario Building

Build three scenarios for ACME Distribution:
- Base: Use the assumptions from Module 3
- Best: 20% revenue growth, 28% gross margin
- Worst: -5% revenue growth, 22% gross margin

Calculate Net Income for each scenario.

### Problem 3: Sensitivity Analysis

Test how ACME's Net Income changes with different revenue growth rates (5% to 15% in 2% increments) and gross margins (23% to 27% in 1% increments).

---

## Solutions - Module 4

### Problem 1

**Year 1**:
- Customers = 500 × (1 - 0.05 + 0.10) = 525
- Revenue = 525 × $1,000 × 12 = $6,300,000

**Year 2**:
- Customers = 525 × (1 - 0.05 + 0.10) = 551
- Revenue = 551 × $1,000 × 12 = $6,615,000

**Year 3**:
- Customers = 551 × (1 - 0.05 + 0.10) = 579
- Revenue = 579 × $1,000 × 12 = $6,945,000

### Problem 2

**Base Case**:
- Revenue = $8,848,125
- Gross Profit = $2,212,031
- SG&A = $1,548,422
- Net Income = $149,526

**Best Case**:
- Revenue = $9,652,500
- Gross Profit = $2,702,700
- SG&A = $1,544,400
- Net Income = $525,210

**Worst Case**:
- Revenue = $7,641,563
- Gross Profit = $1,681,144
- SG&A = $1,451,897
- Net Income = -$107,327

### Problem 3

Sensitivity Table showing Net Income (in thousands):

```
          | 5%     7%     9%     11%    13%    15%
----------|-----------------------------------------
23%       | -$127  -$87   -$47   -$7    $33    $73
24%       | -$50   -$5    $40    $85    $130   $175
25%       | $27    $77    $127   $177   $227   $277
26%       | $104   $159   $214   $269   $324   $379
27%       | $181   $241   $301   $361   $421   $481
```

**Key insight**: Revenue growth has a bigger impact than gross margin changes.

---

## Module 4 Summary

### Key Takeaways

1. **Revenue is usually the most important forecast** - it drives everything else
2. **Use multiple forecasting methods** to cross-check your estimates
3. **Scenarios help you prepare for uncertainty** - always test best and worst cases
4. **Sensitivity analysis shows what really matters** - focus on the key drivers
5. **Document all assumptions** - so you know why you forecasted what you did

### Best Practices

1. **Start with historical data** - understand the past before predicting the future
2. **Use multiple methods** - don't rely on just one approach
3. **Be realistic** - don't over-optimize
4. **Stress test** - assume things will go wrong
5. **Update regularly** - forecasts become outdated quickly

---

# Module 5: Valuation Methods

## 5.1 Introduction to Valuation

### What Is Valuation?

Valuation is answering the question: **"What is this company worth?"**

### Why Value a Company?

1. **To buy or sell** a business
2. **To raise capital** (investors want to know what they're buying)
3. **For financial reporting** (fair value accounting)
4. **To settle disputes** (partnership disagreements, divorce, etc.)

### Three Main Valuation Methods

1. **Discounted Cash Flow (DCF)** - Value based on future cash flows
2. **Comparable Company Analysis (Trading Comps)** - Value based on similar companies
3. **Precedent Transaction Analysis (Transaction Comps)** - Value based on similar acquisitions

> **From the book**: "The number one factor in determining a value of a business is its cash flow from operating activities."

---

## 5.2 Discounted Cash Flow (DCF)

### What Is DCF?

DCF values a company based on the present value of its expected future cash flows.

### Why Use DCF?

1. **Focuses on cash** - not accounting profits
2. **Forward-looking** - based on future expectations
3. **Theoretically sound** - based on the time value of money

### The DCF Formula

```
Enterprise Value = PV of Free Cash Flows + PV of Terminal Value
```

### Step 1: Project Free Cash Flows

**Free Cash Flow Formula**:
```
FCF = EBIT × (1 - Tax Rate) + Depreciation - CAPEX - Change in Working Capital
```

**Example** (ACME Distribution, 2023):
- EBIT = $213,609
- Tax Rate = 30%
- Depreciation = $275,000
- CAPEX = $262,500
- Change in Working Capital = ?

Calculate:
1. EBIT × (1 - Tax) = $213,609 × 0.70 = $149,526
2. Add Depreciation = $149,526 + $275,000 = $424,526
3. Subtract CAPEX = $424,526 - $262,500 = $162,026
4. Subtract Change in WC = ?

Change in WC = Change in A/R + Change in Inventory - Change in A/P
= ($1,091,000 - $705,000) + ($1,090,865 - $450,000) - ($588,647 - $385,000)
= $386,000 + $640,865 - $203,647 = $823,218

FCF = $162,026 - $823,218 = **-$661,192**

**Note**: Negative FCF is common for growing companies because they invest heavily in working capital.

### Step 2: Project FCF for 5-10 Years

| Year | 2023 | 2024 | 2025 | 2026 | 2027 |
|------|------|------|------|------|------|
| EBIT | $214K | $243K | $274K | $308K | $345K |
| Tax (30%) | ($64K) | ($73K) | ($82K) | ($92K) | ($104K) |
| + Depreciation | $275K | $289K | $303K | $318K | $334K |
| - CAPEX | ($263K) | ($276K) | ($290K) | ($305K) | ($320K) |
| - Change in WC | ($823K) | ($588K) | ($625K) | ($663K) | ($704K) |
| **FCF** | **($661K)** | **($405K)** | **($420K)** | **($434K)** | **($449K)** |

### Step 3: Calculate Terminal Value

**Terminal Value** = Value at the end of the projection period.

**Perpetuity Growth Method**:
```
TV = FCF_{n+1} / (WACC - g)
```
Where:
- FCF_{n+1} = FCF in the year after the projection period
- WACC = Weighted Average Cost of Capital
- g = Terminal growth rate (usually GDP growth, 2-3%)

**Exit Multiple Method**:
```
TV = EBITDA × Multiple
```

**Example (Perpetuity Growth)**:
- FCF in Year 5 = -$449,000 (this is a problem because it's negative!)
- Let's assume FCF Year 6 = -$100,000 (still negative, but less)
- WACC = 10%
- g = 3%
- TV = (-$100,000) / (0.10 - 0.03) = -$1,428,571

**This is why we need to fix the negative FCF problem!**

### Step 4: Calculate Present Value

**Present Value Formula**:
```
PV = FCF / (1 + WACC)^Year
```

**Example**:
- FCF Year 1 = -$661,192
- WACC = 10%
- PV = -$661,192 / (1.10)^1 = -$601,084

### Step 5: Calculate Enterprise Value

```
Enterprise Value = PV of FCF + PV of Terminal Value
```

**Example**:
- PV of FCF = Sum of all PVs
- PV of Terminal Value = Terminal Value / (1 + WACC)^n

**The problem**: Negative FCF makes DCF difficult.

**Solution**: Use EBITDA-based valuation for growing companies.

---

## 5.3 Comparable Company Analysis

### What Is Comparable Company Analysis?

Valuing a company by comparing it to similar publicly traded companies.

### Steps

1. **Select comparable companies**
   - Same industry
   - Similar size
   - Similar growth
   - Similar profitability

2. **Calculate multiples for comparables**
   - EV/EBITDA
   - EV/Revenue
   - P/E

3. **Apply multiples to the target**
   - Value = Target metric × Multiples

### Common Multiples

| Multiple | Formula | When to Use |
|----------|---------|-------------|
| EV/EBITDA | Enterprise Value / EBITDA | Most common |
| EV/Revenue | Enterprise Value / Revenue | Early-stage companies |
| P/E | Price / Earnings | Profitable companies |
| P/BV | Price / Book Value | Financial institutions |

### Example: ACME Distribution

**Comparable Companies**:

| Company | EV/EBITDA | EV/Revenue |
|---------|-----------|------------|
| Company A | 12x | 2.0x |
| Company B | 14x | 2.5x |
| Company C | 10x | 1.8x |
| Company D | 13x | 2.2x |
| **Average** | **12.25x** | **2.125x** |

**ACME Distribution**:
- EBITDA = EBIT + Depreciation = $213,609 + $275,000 = $488,609
- Revenue = $8,848,125

**Valuation**:
- Using EV/EBITDA: $488,609 × 12.25 = $5,985,460
- Using EV/Revenue: $8,848,125 × 2.125 = $18,802,266

The average of these two = $12,393,863

### Key Insight

Comparable company analysis shows the market value range, while DCF shows the intrinsic value. Both are useful, and the best valuation uses both methods.

---

## 5.4 Precedent Transaction Analysis

### What Is Precedent Transaction Analysis?

Valuing a company based on what other companies paid in similar acquisitions.

### Why It's Different

**Control Premium**: Acquirers pay more than market price for control.

**Example**: Company trades at $50/share, but is acquired for $65/share (30% premium).

### Steps

1. **Find similar transactions**
2. **Calculate transaction multiples**
3. **Apply multiples to target**

### Example

**Similar Transactions**:

| Transaction | EV/EBITDA | Premium |
|-------------|-----------|---------|
| Company X bought Company Y | 11x | 25% |
| Company A bought Company B | 13x | 30% |
| Company M bought Company N | 10x | 20% |
| **Average** | **11.33x** | **25%** |

**ACME Distribution**:
- EBITDA = $488,609
- Valuation = $488,609 × 11.33 = $5,536,023
- Add control premium (25%): $5,536,023 × 1.25 = $6,920,029

---

## Practice Problems - Module 5

### Problem 1: DCF Calculation

A company has the following projected FCFs:
- Year 1: $100,000
- Year 2: $120,000
- Year 3: $140,000
- Year 4: $160,000
- Year 5: $180,000

WACC = 12%
Terminal growth = 3%

Calculate:
1. Present Value of FCFs
2. Terminal Value (perpetuity growth)
3. Enterprise Value

### Problem 2: Comparable Analysis

A company has EBITDA of $10,000,000 and Revenue of $50,000,000.

Comparable companies trade at:
- EV/EBITDA: 8x, 9x, 10x, 11x, 12x
- EV/Revenue: 1.5x, 1.6x, 1.7x, 1.8x, 1.9x

Calculate the valuation range.

### Problem 3: Precedent Transactions

Similar acquisitions have EV/EBITDA multiples of:
- 8.5x, 9.0x, 9.5x, 10.0x, 10.5x

Control premiums are 20-30%.

Calculate the valuation range for a company with EBITDA of $15,000,000.

---

## Solutions - Module 5

### Problem 1

**PV of FCFs**:

| Year | FCF | PV Factor | Present Value |
|------|-----|-----------|---------------|
| 1 | $100,000 | 1/(1.12)^1 = 0.893 | $89,286 |
| 2 | $120,000 | 1/(1.12)^2 = 0.797 | $95,663 |
| 3 | $140,000 | 1/(1.12)^3 = 0.712 | $99,636 |
| 4 | $160,000 | 1/(1.12)^4 = 0.636 | $101,693 |
| 5 | $180,000 | 1/(1.12)^5 = 0.567 | $102,113 |
| **Total PV** | | | **$488,391** |

**Terminal Value**:
- FCF Year 6 = $180,000 × 1.03 = $185,400
- TV = $185,400 / (0.12 - 0.03) = $2,060,000
- PV of TV = $2,060,000 / (1.12)^5 = $1,168,641

**Enterprise Value** = $488,391 + $1,168,641 = **$1,657,032**

### Problem 2

**EV/EBITDA Range**:
- Low: $10,000,000 × 8 = $80,000,000
- High: $10,000,000 × 12 = $120,000,000
- Average: $10,000,000 × 10 = $100,000,000

**EV/Revenue Range**:
- Low: $50,000,000 × 1.5 = $75,000,000
- High: $50,000,000 × 1.9 = $95,000,000
- Average: $50,000,000 × 1.7 = $85,000,000

**Overall Valuation Range**: $75,000,000 - $120,000,000

### Problem 3

**Multiples**:
- Low: 8.5x
- Average: 9.5x
- High: 10.5x

**EBITDA = $15,000,000**

**Premiums**: 20-30%

**Valuation Range (Multiples only)**:
- Low: $15,000,000 × 8.5 = $127,500,000
- Average: $15,000,000 × 9.5 = $142,500,000
- High: $15,000,000 × 10.5 = $157,500,000

**With Control Premium**:
- Low: $127,500,000 × 1.20 = $153,000,000
- High: $157,500,000 × 1.30 = $204,750,000

**Valuation Range**: $153,000,000 - $204,750,000

---

## Module 5 Summary

### Key Takeaways

1. **There are three main valuation methods**: DCF, Comparable Companies, and Precedent Transactions

2. **DCF is theoretically the best** but requires many assumptions

3. **Comparable companies** show what the market is paying for similar companies

4. **Precedent transactions** show what acquirers have paid for control

5. **Use multiple methods** and triangulate to a value range

6. **Valuation is art, not science** - different analysts will get different numbers

### Best Practices

1. **Use at least two methods** - triangulate to a value range
2. **Be conservative** - valuations are often too optimistic
3. **Sensitivity test** - show how the value changes with assumptions
4. **Document everything** - so you can explain your logic
5. **Update regularly** - valuations change with market conditions

---

# Module 6: Final Project

## Project Instructions

### Overview

You'll build a complete financial model for a public company and present your findings.

### Part 1: Choose a Company

**Choose a publicly traded company** from an industry you understand. Good options for beginners:

1. **Retail**: Walmart (WMT), Target (TGT), Costco (COST)
2. **Tech**: Apple (AAPL), Microsoft (MSFT), Google (GOOGL)
3. **Consumer**: Coca-Cola (KO), PepsiCo (PEP)
4. **Industrial**: General Electric (GE), Boeing (BA)

**Download financial statements from the SEC (EDGAR) or Yahoo Finance.**

### Part 2: Build the Model

**Tab 1: Assumptions**
- Document all your assumptions
- Color code (blue = inputs)

**Tab 2: Historical Financials**
- 5 years of historical data
- Income Statement, Balance Sheet, Cash Flow

**Tab 3: Forecast**
- 5-year forecast
- Income Statement, Balance Sheet, Cash Flow
- Must balance!

**Tab 4: Valuation**
- DCF valuation
- Comparable company analysis
- Precedent transaction analysis

**Tab 5: Sensitivity**
- Test key assumptions
- Show scenario analysis

**Tab 6: Executive Summary**
- Key metrics
- Charts
- Recommendations

### Part 3: Write the Report

**Cover Page**: Company name, date, your name

**Executive Summary**: 1-2 page summary of findings

**Valuation Summary**: 2-3 pages explaining your valuation

**Recommendations**: 1-2 pages with specific recommendations

### Part 4: Presentation

**Create a professional presentation** (PowerPoint or similar)
- 5-10 slides
- Charts and graphs
- Clear recommendations

## Grading Criteria

1. **Excel Model (40%)**
   - Accuracy (does it balance?)
   - Formatting (professional)
   - Assumptions (documented)

2. **Analysis (30%)**
   - Quality of analysis
   - Reasonableness of assumptions
   - Valuation range

3. **Report (20%)**
   - Clarity
   - Organization
   - Recommendations

4. **Presentation (10%)**
   - Professionalism
   - Clarity
   - Handling questions

---

## Model Checklist

### Excel Model

- [ ] All tabs are named correctly
- [ ] Assumptions tab has ALL inputs
- [ ] Inputs are color-coded blue
- [ ] Formulas are color-coded black
- [ ] Links are color-coded green
- [ ] Income Statement balances
- [ ] Balance Sheet balances
- [ ] Cash Flow Statement reconciles
- [ ] DCF has all components
- [ ] Sensitivity tables work
- [ ] No hard-coded numbers in formulas
- [ ] Formatting is consistent
- [ ] Charts are labeled

### Report

- [ ] Cover page
- [ ] Executive summary
- [ ] Company overview
- [ ] Industry analysis
- [ ] Key assumptions explained
- [ ] Historical performance
- [ ] Forecasted performance
- [ ] Valuation methodology
- [ ] Valuation results
- [ ] Sensitivity analysis
- [ ] Recommendations
- [ ] Appendices

### Presentation

- [ ] 5-10 slides
- [ ] Title slide
- [ ] Company overview
- [ ] Key assumptions
- [ ] Financial summary
- [ ] Valuation
- [ ] Sensitivity
- [ ] Recommendations
- [ ] Q&A slide

---

## Congratulations!

You've completed the Comprehensive Financial Modeling Course. You now have the skills to:
1. Read and understand financial statements
2. Build complete 3-statement models
3. Forecast company performance
4. Value companies using multiple methods
5. Present your findings professionally

### Next Steps

1. **Practice, practice, practice!** Build models for different companies
2. **Learn advanced topics** - LBO models, M&A models, project finance
3. **Study industry best practices** - Read Wall Street research reports
4. **Consider certification** - CFA, FMVA, etc.
5. **Apply your skills** - At work, or to evaluate investments

### Additional Resources

| Resource | What It Offers |
|----------|----------------|
| CFI | Free and paid modeling courses |
| Breaking Into Wall Street | Free tutorials |
| Wall Street Prep | Professional templates |
| Macabacus | Excel add-in for modeling |
| FactSet/Bloomberg | Professional data services |

---

**End of Course**
