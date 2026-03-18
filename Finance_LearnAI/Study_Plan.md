# 6-Week Study Plan: Finance + AI Tools
## For the Finance Undergraduate with Minimal Software Development Experience

> **Goal:** Build practical AI fluency on top of your Finance degree — enough to build real applications, land high-paying jobs, and work confidently with Claude Code and AI agents
> **Time Required:** 1–2 hours per day (10–14 hours/week)
> **Cost:** $0 — all resources are free
> **Starting Point:** Finance knowledge ✓ | Software experience: minimal

---

## How to Use This Plan

- **Do not skip weeks** — each week builds on the previous one
- **Hands-on > reading** — every week has a mini-project; prioritize doing over watching
- **Use Claude Code from Day 1** — it is part of the learning, not a reward at the end
- **Finance first** — all exercises use financial data and scenarios; no abstract programming puzzles
- Mark each task `[x]` as you complete it to track momentum

---

## Pre-Week Setup (Day 0 — 1 Hour)

Complete these before Week 1:

- [ ] **Install Claude Code**
  - Follow: [Claude Code Quickstart](https://docs.anthropic.com/en/docs/claude-code/quickstart)
  - Free tier available — no credit card required to start

- [ ] **Install Python (via Anaconda)**
  - Download: [anaconda.com/download](https://www.anaconda.com/download) (free, Windows/Mac/Linux)
  - Anaconda includes Jupyter Notebook — your primary learning environment

- [ ] **Create a GitHub Account**
  - [github.com](https://github.com) — free
  - Create a repository called `finance-ai-projects`

- [ ] **Get a Free Alpha Vantage API Key**
  - [alphavantage.co](https://www.alphavantage.co/support/#api-key) — free tier includes 25 API calls/day
  - This gives you real stock market data for all exercises

- [ ] **Bookmark These References**
  - [Python for Finance (Official Docs)](https://pandas.pydata.org/docs/)
  - [Claude API Documentation](https://docs.anthropic.com)
  - [MCP Documentation](https://modelcontextprotocol.io/introduction)

---

## Week 1: Python Foundations for Finance

> **Theme:** Learn just enough Python to read Claude Code's output and run financial calculations
> **Mini-Project:** Build a stock return calculator in a Jupyter Notebook

### Day 1 — Python Basics (90 min)

**Learning Resources:**
- [Python for Everybody — Chapter 1 & 2](https://www.py4e.com/lessons) (free, beginner-friendly)
  - Variables, data types, basic operations
- [Google Colab Introduction](https://colab.research.google.com/notebooks/intro.ipynb) (free cloud notebooks, no install needed)

**Finance Exercise:**
Open Jupyter Notebook and ask Claude Code:
```
"Write Python code in a Jupyter notebook to calculate the following:
- Given a stock price of $150 today and $120 one year ago, calculate the annual return
- Calculate the same for 5 different stocks I'll give you
- Show the results in a formatted table"
```
Read through every line it writes. Ask Claude to explain anything you don't understand.

- [ ] Completed

---

### Day 2 — Working with Data: Pandas Basics (90 min)

**Learning Resources:**
- [Pandas Getting Started Tutorial](https://pandas.pydata.org/docs/getting_started/intro_tutorials/index.html) (official, free)
  - Focus on: "Reading data", "Selecting data", "Grouping data"
- [Kaggle: Pandas Course](https://www.kaggle.com/learn/pandas) (free, interactive, 4 hours total — do first 2 lessons today)

**Finance Exercise:**
Download any company's stock price history from Yahoo Finance as CSV, then ask Claude Code:
```
"Load this CSV file of stock price data. Calculate:
- Daily returns
- 30-day rolling average price
- Monthly high, low, and average
- Flag any day where the daily return exceeded +/- 3%
Show everything in a clean DataFrame."
```

- [ ] Completed

---

### Day 3 — Financial Data with Real APIs (60 min)

**Learning Resources:**
- [Alpha Vantage Documentation](https://www.alphavantage.co/documentation/) — read the "Stock Time Series" section
- [Requests Library Tutorial](https://realpython.com/python-requests/) (free, Real Python) — read "Making a GET request" section only

**Finance Exercise:**
Ask Claude Code:
```
"Using the Alpha Vantage API with my key [YOUR_KEY], write Python code to:
- Pull the last 30 days of daily prices for Apple (AAPL), Microsoft (MSFT), and JPMorgan (JPM)
- Calculate daily returns for each
- Calculate the correlation between their returns
- Print a correlation matrix"
```

- [ ] Completed

---

### Day 4 — Visualization (60 min)

**Learning Resources:**
- [Matplotlib Tutorial for Beginners](https://matplotlib.org/stable/tutorials/introductory/pyplot.html) (official, free)
- [Plotly Express Overview](https://plotly.com/python/plotly-express/) (free, interactive charts — better for finance dashboards)

**Finance Exercise:**
Ask Claude Code:
```
"Using the stock data from yesterday, create:
- A line chart comparing the cumulative returns of AAPL, MSFT, and JPM over 30 days
- A bar chart of monthly average returns
- Make it look professional with proper labels, title, and legend"
```

- [ ] Completed

---

### Day 5 — Mini-Project: Stock Performance Dashboard (90 min)

Build your first complete finance tool using Claude Code only.

**Prompt:**
```
"Build a Jupyter notebook that serves as a stock performance dashboard.
Given a list of stock tickers I provide:
1. Pull 90 days of price data using Alpha Vantage API
2. Calculate: total return, volatility (std dev of daily returns), Sharpe ratio (assume 4.5% risk-free rate)
3. Show a comparison table of all stocks ranked by Sharpe ratio
4. Plot cumulative returns on a single chart
5. Highlight the best and worst performing stock

Make the notebook clean with markdown headers explaining each section."
```

Save to your GitHub repository.

- [ ] Completed

---

### Week 1 Reflection Questions
- Can you read the Python code Claude generated and understand roughly what each section does?
- Can you change a number (like the risk-free rate) and re-run the notebook?
- What financial assumptions did Claude make that you would want to verify or change?

---

## Week 2: Excel + AI and Financial Modeling

> **Theme:** Supercharge your Excel skills with AI assistance and build financial models faster than ever
> **Mini-Project:** AI-assisted DCF model with sensitivity analysis

### Day 1 — Claude Code + Excel (60 min)

**Learning Resources:**
- [Excel Power Query Basics](https://support.microsoft.com/en-us/office/power-query-for-excel-help-2b433a85-ddfb-420b-9cda-fe0e60b82a94) (Microsoft, free)
- [XLOOKUP Tutorial](https://support.microsoft.com/en-us/office/xlookup-function-b7fd680e-6d10-43e6-84f9-88eae8bf5929) (Microsoft, free)

**Finance Exercise:**
Ask Claude Code:
```
"I have monthly expense data in a CSV file [describe your data structure].
Generate a Python script that:
- Reads the CSV
- Summarizes expenses by category
- Calculates month-over-month variance
- Exports a clean Excel file with a summary tab and a detail tab
- Adds conditional formatting: red for expenses >10% over prior month"
```

- [ ] Completed

---

### Day 2 — Building a 3-Statement Financial Model Structure (90 min)

**Learning Resources:**
- [Corporate Finance Institute: 3 Statement Model](https://corporatefinanceinstitute.com/resources/financial-modeling/3-statement-model/) (free access)
- [Wall Street Prep: Financial Modeling Fundamentals](https://www.wallstreetprep.com/knowledge/financial-modeling/) (free articles)

**Finance Exercise (Manual First, AI Second):**
1. Sketch the structure of a 3-statement model on paper: what flows from income statement to balance sheet to cash flow?
2. Then ask Claude Code:
```
"Build a 3-statement financial model template in Excel for a simple
retail company. Include:
- 5-year income statement with revenue, COGS, operating expenses
- Balance sheet with key working capital items
- Cash flow statement that reconciles to the balance sheet
- All three statements must link correctly
- Include a assumptions tab for inputs"
```
3. **Your job:** Verify that the model actually balances. Does the balance sheet balance? Does cash flow to the balance sheet?

- [ ] Completed

---

### Day 3 — DCF Valuation Model with Claude Code (90 min)

**Learning Resources:**
- [Investopedia: DCF Analysis](https://www.investopedia.com/terms/d/dcf.asp) (free)
- [Damodaran Online: DCF Valuation](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/valuation/dcfvest.htm) (NYU professor, free — use the "DCF Basics" section)

**Finance Exercise:**
```
"Build a DCF valuation model in Excel for a technology company with these specifications:
- 5-year explicit forecast period
- Revenue growth: 20%, 18%, 15%, 12%, 10% per year
- EBITDA margin: 25%, 26%, 27%, 27%, 28%
- D&A: 8% of revenue
- CapEx: 10% of revenue
- NWC change: 2% of revenue change
- Tax rate: 21%
- WACC: 10%
- Terminal growth rate: 3% (Gordon Growth Model)
- Include a sensitivity table: NPV across WACC (8-12%) and terminal growth (1-5%)
- Show enterprise value to equity value bridge assuming $500M debt, $50M cash, 100M diluted shares"
```

Review: Are the FCF numbers directionally correct? Is the terminal value reasonable relative to total enterprise value? (It should typically be 60–80% of total EV.)

- [ ] Completed

---

### Day 4 — Comparable Company Analysis Automation (60 min)

**Learning Resources:**
- [CFI: Comparable Company Analysis](https://corporatefinanceinstitute.com/resources/valuation/comparable-company-analysis/) (free)

**Finance Exercise:**
```
"Using the Alpha Vantage API, pull financial data for 5 companies in the same sector.
Build a Python script that creates a comparable company analysis (comps) table showing:
- EV/EBITDA, P/E, P/S, EV/Revenue multiples
- Revenue growth (LTM)
- EBITDA margin
- Show median and mean for each metric
- Highlight which company trades at the largest discount to peers on EV/EBITDA"
```

- [ ] Completed

---

### Day 5 — Mini-Project: Valuation Tool (90 min)

Ask Claude Code to combine the DCF and comps work:
```
"Build a Python notebook that takes a company ticker as input and outputs:
1. A DCF valuation using analyst consensus estimates from Alpha Vantage
2. A trading comps table with 5 comparable companies (I'll specify them)
3. A football field chart showing the valuation range from both methods
4. A one-paragraph summary of the implied upside/downside vs. current price"
```

Save to GitHub. This is your first portfolio project.

- [ ] Completed

---

## Week 3: SQL and Databases for Finance

> **Theme:** Learn to work with structured financial data in databases — the foundation of enterprise finance systems
> **Mini-Project:** Financial transaction analysis database

### Day 1 — SQL Fundamentals (90 min)

**Learning Resources:**
- [SQLZoo: Interactive SQL Tutorial](https://sqlzoo.net/wiki/SELECT_basics) (free, runs in browser — no install needed)
  - Complete: SELECT basics, WHERE, GROUP BY (Sections 0–5)
- [Mode Analytics SQL Tutorial](https://mode.com/sql-tutorial/) (free, excellent for finance data)
  - Complete: Basic SQL section

**Finance Exercise:**
Ask Claude Code to create a sample database:
```
"Create a SQLite database with the following tables:
- transactions (id, date, amount, category, account, description)
- accounts (id, name, type, balance)
- budget (id, category, monthly_budget)

Populate it with 100 realistic sample transactions for a small company.
Then write SQL queries to:
- Total spending by category this month
- Categories where actual > budget by more than 10%
- Weekly cash flow trend
- Top 10 largest transactions"
```
Read the SQL queries Claude writes. Can you understand what each line does?

- [ ] Completed

---

### Day 2 — Joins and Aggregations for Financial Analysis (60 min)

**Learning Resources:**
- [SQLZoo: JOIN operations](https://sqlzoo.net/wiki/The_JOIN_operation) (free, interactive)
- [W3Schools: SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp) (free, quick reference)

**Finance Exercise:**
```
"Write SQL queries against the database from yesterday to:
- Show month-over-month revenue growth (requires joining months)
- Calculate the running balance for each account over time
- Find all transactions where the same vendor was paid more than 3 times in a month
- Generate a pivot table showing spending by category by month"
```

- [ ] Completed

---

### Day 3 — Connecting Python to Databases (60 min)

**Learning Resources:**
- [SQLite3 Python Documentation](https://docs.python.org/3/library/sqlite3.html) (official, free)
- [Pandas read_sql Tutorial — Real Python](https://realpython.com/pandas-read-file-types/#read-from-a-database) (free)

**Finance Exercise:**
```
"Write a Python script that:
- Connects to the SQLite database
- Runs a query to get monthly spending by category
- Loads the result into a pandas DataFrame
- Plots it as a stacked bar chart
- Saves the chart as a PNG file"
```

- [ ] Completed

---

### Day 4 — Financial Database Design (60 min)

**Learning Resources:**
- [Database Design Tutorial — Lucidchart](https://www.lucidchart.com/pages/database-diagram/database-design) (free)

**Finance Exercise:**
Design (on paper first, then implement):
```
"Design and create a database schema for a personal investment portfolio tracker.
Tables needed:
- portfolio (positions: ticker, shares, cost_basis, purchase_date)
- prices (ticker, date, close_price) — to store historical data
- transactions (buy/sell history)
- dividends received

Create the tables, populate with sample data for 5 stocks,
and write a query that shows current portfolio value,
total gain/loss by position, and portfolio allocation by sector."
```

- [ ] Completed

---

### Day 5 — Mini-Project: Financial Analytics Dashboard (90 min)

```
"Build a complete financial analytics system:
1. SQLite database storing 6 months of mock company financial transactions
2. Python script that queries the database and generates:
   - Cash flow analysis by month
   - Budget vs. actual variance report
   - Expense anomaly detection (flag transactions >2 standard deviations from category average)
3. Export results to a clean Excel report with charts
4. Include a summary tab with key metrics: burn rate, runway, biggest expense categories"
```

Save to GitHub.

- [ ] Completed

---

## Week 4: AI Agents and MCP Servers

> **Theme:** Build your first AI agent for finance — connect Claude to real financial data
> **Mini-Project:** A financial research agent using MCP

### Day 1 — Understanding AI Agents (60 min)

**Learning Resources:**
- [Anthropic: Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) (free, authoritative)
  - Focus on: "What are agents?", "When to use agents vs. workflows"
- [CFA Institute: Agentic AI for Finance](https://rpc.cfainstitute.org/research/the-automation-ahead-content-series/agentic-ai-for-finance) (free)
  - Read the "Workflow patterns" section

**Conceptual Exercise:**
On paper, design an agent for one finance workflow you know well. For each step ask:
- Is this step predictable enough to automate?
- What data does it need?
- What decision does it make?
- What action does it take?

Example: *"Earnings analysis agent: (1) Detect earnings release → (2) Pull transcript → (3) Extract key metrics → (4) Compare to estimates → (5) Draft summary"*

- [ ] Completed

---

### Day 2 — Setting Up MCP Servers (90 min)

**Learning Resources:**
- [MCP Introduction Documentation](https://modelcontextprotocol.io/introduction) (official, free)
- [Claude Code MCP Guide](https://docs.anthropic.com/en/docs/claude-code/mcp) (official, free)

**Hands-on Exercise:**
Install and configure the Yahoo Finance MCP server:
1. Open Claude Code
2. Follow the guide at [github.com/Alex2Yang97/yahoo-finance-mcp](https://github.com/Alex2Yang97/yahoo-finance-mcp)
3. Ask Claude Code to help with any setup issues — describe exactly what error you see

Then test it by asking Claude:
```
"Using the Yahoo Finance MCP, pull Apple's current stock price,
P/E ratio, and analyst consensus target price.
Compare the current price to the consensus target and calculate the implied upside."
```

- [ ] Completed

---

### Day 3 — Using Multiple MCP Data Sources (90 min)

**Learning Resources:**
- [financial-datasets MCP GitHub](https://github.com/financial-datasets/mcp-server) — setup guide
- [Alpha Vantage MCP](https://mcp.alphavantage.co/) — documentation

**Hands-on Exercise:**
Configure at least 2 MCP servers (Yahoo Finance + financial-datasets or Alpha Vantage), then ask Claude:
```
"I want to analyze Microsoft (MSFT) as an investment.
Using available data sources:
1. Pull the last 4 quarters of financial statements
2. Calculate revenue growth, EBITDA margin trend, and free cash flow conversion
3. Get the current valuation multiples
4. Compare these to the 5-year historical averages
5. Write a 3-paragraph investment summary with a bull case and bear case"
```

This is a task that would take an analyst 3–4 hours. Notice how long it takes Claude with MCP access.

- [ ] Completed

---

### Day 4 — Building a Simple Finance Agent (90 min)

**Learning Resources:**
- [Claude API: Tool Use Documentation](https://docs.anthropic.com/en/docs/build-with-claude/tool-use) (official, free)
- [Anthropic Cookbook: Tool Use Examples](https://github.com/anthropics/anthropic-cookbook) (free, GitHub)

**Finance Exercise:**
Ask Claude Code:
```
"Build a Python script that creates a simple investment research agent.
The agent should:
1. Accept a company name or ticker as input
2. Use Alpha Vantage API to pull: current price, P/E, EPS, revenue (TTM)
3. Use the financial-datasets MCP (or Alpha Vantage) to pull the income statement
4. Calculate: revenue growth YoY, net margin, P/E vs. sector average (hardcode sector averages I provide)
5. Output a structured research note: company overview, key financial metrics, valuation assessment, one-line recommendation

Test it on 3 different companies."
```

- [ ] Completed

---

### Day 5 — Mini-Project: Portfolio Monitor Agent (2 hours)

This is your most ambitious project so far:
```
"Build a portfolio monitoring agent in Python that:
1. Takes a list of stock tickers and share counts as input (my portfolio)
2. Pulls current prices using Yahoo Finance MCP or Alpha Vantage
3. Calculates: current value, cost basis (I'll provide), gain/loss per position, % allocation
4. Pulls latest news headlines for each holding
5. Flags any position where: price dropped >5% today, news sentiment appears negative, or allocation drifted >5% from target
6. Generates a morning briefing report as a formatted text file

This should run every morning and save the report with a timestamp."
```

Save to GitHub. This is portfolio project #2.

- [ ] Completed

---

## Week 5: Data Privacy, Compliance, and Responsible AI in Finance

> **Theme:** Develop the compliance and governance mindset that makes you valuable in regulated finance environments
> **Mini-Project:** Build a compliance-aware AI workflow

### Day 1 — Financial Regulation Basics (90 min)

**Learning Resources:**
- [SEC 2026 Examination Priorities (Official PDF)](https://www.sec.gov/files/2026-exam-priorities.pdf) — read the AI section
- [FINRA 2026 Annual Regulatory Oversight Report — GenAI Section](https://www.finra.org/rules-guidance/guidance/reports/2026-finra-annual-regulatory-oversight-report/gen-ai) (free)
- [FINRA: Regulatory Notice on AI Use](https://www.finra.org/rules-guidance/notices) (search for AI notices, free)

**Study Exercise:**
Read both documents and create a personal cheat sheet answering:
- What must a firm be able to demonstrate to regulators about its AI use?
- What are the 3 biggest compliance risks FINRA flagged for AI agents in finance?
- What does "supervisory system" mean in the context of an AI tool?

- [ ] Completed

---

### Day 2 — Data Privacy Frameworks (60 min)

**Learning Resources:**
- [GDPR for Dummies — GDPR.eu](https://gdpr.eu/what-is-gdpr/) (free, plain English overview)
- [CCPA Overview — California AG](https://oag.ca.gov/privacy/ccpa) (official, free)
- [PCI DSS Overview — PCI Security Standards Council](https://www.pcisecuritystandards.org/pci_security/) (free summary)

**Study Exercise:**
Map each regulation to a practical scenario:
- *If I build a client investment dashboard, what GDPR obligations apply if any EU clients use it?*
- *If my app processes credit card data, what PCI DSS requirements kick in?*
- *What data can I safely send to Claude.ai vs. what requires an enterprise agreement?*

Then ask Claude Code:
```
"Given a finance application that handles client names, investment portfolios,
and transaction history, help me create a data classification matrix showing:
- What data categories exist
- Risk level for each
- Whether it can be used with external AI tools
- What anonymization or masking would be needed to reduce risk"
```

- [ ] Completed

---

### Day 3 — Building Compliant AI Workflows (90 min)

**Learning Resources:**
- [Navigating AI Compliance: A Risk-Based Framework — AdvisorEngine](https://www.advisorengine.com/action-magazine/articles/navigating-ai-compliance-a-risk-based-framework-for-financial-services-in-2026) (free)
- [Generative AI in Financial Services: Practical Compliance Playbook — Shumaker Law](https://www.shumaker.com/insight/client-alert-generative-artificial-intelligence-in-financial-services-a-practical-compliance-playbook-for-2026/) (free)

**Hands-on Exercise:**
Redesign your portfolio monitor agent from Week 4 with compliance controls:
```
"Review my portfolio monitor agent code. Add the following compliance controls:
1. PII masking — replace client names with anonymized IDs in all logs
2. Audit trail — log every API call, timestamp, and output to a local file
3. Data validation — reject any input that looks like a Social Security Number
4. Output watermarking — add 'AI-Generated, Human Review Required' to all reports
5. Error handling — if the AI output seems implausible (e.g., returns >100%), flag for human review rather than outputting"
```

- [ ] Completed

---

### Day 4 — AI Risk Classification Exercise (60 min)

**Learning Resources:**
- [NIST AI Risk Management Framework](https://www.nist.gov/system/files/documents/2023/01/26/AI%20RMF%201.0.pdf) (free PDF, read Executive Summary and Section 2)

**Exercise:**
Create a risk classification table for 6 different AI use cases in finance. For each, assess:
- Risk level (High/Medium/Low)
- Data sensitivity
- Regulatory exposure
- Required controls
- Whether human-in-the-loop is required

| Use Case | Risk | Controls Needed |
|---|---|---|
| Portfolio rebalancing recommendation | High | Human approval required |
| Market research summarization | Low | Review before distribution |
| Client email draft generation | Medium | Compliance review |
| Expense category classification | Low | Sample audit |
| Credit decision support | High | Full explainability + human decision |
| Earnings transcript analysis | Low | Verify data sources |

Then ask Claude:
```
"Given this risk classification framework, help me write a one-page
AI Use Policy for a small investment advisory firm. It should cover:
approved tools, data handling rules, human review requirements, and record-keeping."
```

- [ ] Completed

---

### Day 5 — Mini-Project: Compliance Documentation Generator (90 min)

```
"Build a Python tool that generates compliance documentation for AI use in finance.
Given a description of an AI use case (input as text), generate:
1. A risk classification (High/Medium/Low) with justification
2. A list of applicable regulations (SEC/FINRA/GDPR/PCI based on use case type)
3. A required controls checklist
4. A simple audit log template (CSV format)
5. A human review checklist for the specific use case

Test it on three scenarios:
- A client-facing robo-advisor
- An internal expense reporting automation
- An AML transaction screening tool"
```

Save to GitHub. This demonstrates compliance awareness that few candidates have.

- [ ] Completed

---

## Week 6: Capstone — Build a Complete Finance AI Application

> **Theme:** Integrate everything into a single professional-grade project
> **Capstone Project:** Choose ONE of the three applications below and build it completely

### Choose Your Capstone (All Are Equivalent in Value)

---

### Option A: Investment Research Platform

**What you build:** A complete investment research tool that generates institutional-quality research notes

**Specification:**
```
"Build a complete investment research platform with the following capabilities:

1. Data Collection (using MCP servers):
   - Financial statements (income statement, balance sheet, cash flow)
   - Historical price data and valuation multiples
   - Recent news and analyst ratings
   - Macroeconomic context (interest rates, sector data)

2. Analysis Engine:
   - DCF valuation with your assumptions
   - Trading comps vs. 5 peer companies
   - Technical analysis: 50-day and 200-day moving averages, RSI
   - Quality score: based on ROE, debt/EBITDA, FCF conversion

3. Report Generation:
   - 2-page research note (PDF or Word format) with:
     - Investment thesis
     - Key financial metrics table
     - Valuation summary (football field chart)
     - Risks
     - Price target with methodology
   - Header with 'AI-Generated Content — Subject to Human Review'

4. Compliance:
   - Full audit trail of all data sources and timestamps
   - Flag any data that is >30 days old as potentially stale

Test with 2 different companies."
```

---

### Option B: Corporate FP&A Automation Suite

**What you build:** A complete FP&A toolset for a small to mid-size company

**Specification:**
```
"Build a corporate FP&A automation suite:

1. Data Infrastructure:
   - SQLite database for actuals (transactions by category, month, department)
   - Excel/CSV input for budget data
   - Historical data for 12 months

2. Automated Analysis:
   - Monthly budget vs. actual variance report by department and category
   - Trend analysis: 3-month rolling averages, YoY comparison
   - Anomaly detection: flag items >2 standard deviations from historical norm
   - Cash flow forecast: 13-week rolling cash flow projection

3. Reporting:
   - Executive dashboard: one-page PDF with key metrics
   - Detailed variance report: Excel with drill-down by category
   - Narrative generation: AI-written commentary explaining variances
   - Board pack section: formatted slides data (output as data for PowerPoint)

4. Compliance:
   - Audit trail for all calculations
   - Version control for budget vs. revised forecast
   - Access log (who ran what report, when)"
```

---

### Option C: AI-Powered Compliance Monitor

**What you build:** A compliance monitoring tool for a small financial advisory firm

**Specification:**
```
"Build a compliance monitoring system for a registered investment advisor (RIA):

1. Document Analysis:
   - Process client emails and communications for compliance keywords
   - Flag: promises of returns, suitability red flags, required disclosure language
   - Analyze trade confirmations for concentration risk violations

2. Portfolio Monitoring:
   - Daily check: any position >10% of a client portfolio (concentration limit)
   - Flag: drift from stated investment mandate
   - Detect: trades that might indicate front-running patterns

3. Regulatory Intelligence:
   - Parse SEC/FINRA notices (from RSS feeds or uploaded PDFs)
   - Flag items relevant to the firm's business activities
   - Generate weekly compliance digest

4. Reporting:
   - Weekly compliance report for CCO (Chief Compliance Officer)
   - Audit-ready log of all flagged items and resolutions
   - Summary statistics: flags this week, resolved, open items

5. Compliance Controls:
   - All client data anonymized in logs
   - VALID framework applied to every AI output
   - Human review required before any regulatory action"
```

---

### Capstone Schedule (Days 1–5)

**Day 1 — Architecture Design (60 min)**
Before writing any code, create a design document:
- What are the inputs?
- What are the outputs?
- What data sources are needed?
- What are the compliance considerations?
- What would a reviewer need to trust this tool?

Share the design with Claude and ask: *"Review my architecture. What am I missing? What could go wrong?"*

**Day 2–3 — Build Core Functionality (2–3 hours each)**
Use Claude Code iteratively:
- Start with data collection
- Add analysis layer
- Build reporting/output

**Day 4 — Add Compliance Controls and Testing (90 min)**
- Implement the VALID framework for outputs
- Add audit logging
- Test with edge cases (missing data, implausible outputs)

**Day 5 — Polish and Document (90 min)**
- Write a README explaining what the tool does, how to run it, and what compliance controls exist
- Record a 2-minute screen recording demonstrating the tool (use Loom — free)
- Push final version to GitHub

---

## Post-Plan: What to Do Next

### Immediate Next Steps After Week 6

**Build Your Portfolio:**
- [ ] Ensure all 3+ projects are on GitHub with clear README files
- [ ] Create a personal website (use GitHub Pages — free) showcasing your finance + AI work
- [ ] Write a brief LinkedIn post about each project (the market for this is thin; visibility matters)

**Continue Learning:**
- [ ] [AWS Certified AI Practitioner](https://aws.amazon.com/certification/certified-ai-practitioner/) — first credential to pursue (~2 months prep)
- [ ] [Kaggle: Intro to Machine Learning](https://www.kaggle.com/learn/intro-to-machine-learning) (free, 3 hours) — basics of how ML models work
- [ ] [freeCodeCamp: Data Analysis with Python](https://www.freecodecamp.org/learn/data-analysis-with-python/) (free, complete certification)

**Career Steps:**
- [ ] Apply to 5 internships from [github.com/jobright-ai/2026-Account-Internship](https://github.com/jobright-ai/2026-Account-Internship)
- [ ] Reach out to UA Culverhouse alumni in FinTech roles on LinkedIn (mentorship > job boards)
- [ ] Join: [r/financialcareers](https://www.reddit.com/r/financialcareers/), [r/learnpython](https://www.reddit.com/r/learnpython/) for community support

**Deepen Credentials:**
- [ ] CFA Level 1 (pairs exceptionally with AI skills for investment roles)
- [ ] [AWS Certified Generative AI Developer – Professional](https://aws.amazon.com/certification/certified-generative-ai-developer-professional/) (see AWS_GenAI_StudyPlan.md for full plan)

---

## Free Resource Master List

### Python
| Resource | What It Covers | Link |
|---|---|---|
| Python for Everybody (py4e) | Python from zero | [py4e.com](https://www.py4e.com/lessons) |
| Kaggle Python Course | Pandas, visualization | [kaggle.com/learn/python](https://www.kaggle.com/learn/python) |
| Real Python | Practical tutorials | [realpython.com](https://realpython.com) |
| freeCodeCamp Python | Full curriculum | [freecodecamp.org](https://www.freecodecamp.org/learn/data-analysis-with-python/) |

### Finance + Python
| Resource | What It Covers | Link |
|---|---|---|
| Python for Finance (Yves Hilpisch) | Finance-specific Python | Free preview chapters available |
| Quantopian Lectures (archived) | Quantitative finance | [github.com/quantopian/research_public](https://github.com/quantopian/research_public) |
| Alpha Vantage Documentation | Stock market API | [alphavantage.co/documentation](https://www.alphavantage.co/documentation/) |

### SQL
| Resource | What It Covers | Link |
|---|---|---|
| SQLZoo | Interactive SQL | [sqlzoo.net](https://sqlzoo.net) |
| Mode SQL Tutorial | Business analytics SQL | [mode.com/sql-tutorial](https://mode.com/sql-tutorial/) |
| W3Schools SQL | Quick reference | [w3schools.com/sql](https://www.w3schools.com/sql/) |

### AI / Claude Code
| Resource | What It Covers | Link |
|---|---|---|
| Claude Code Documentation | Official guide | [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code/quickstart) |
| Anthropic Cookbook | Code examples | [github.com/anthropics/anthropic-cookbook](https://github.com/anthropics/anthropic-cookbook) |
| MCP Documentation | Model Context Protocol | [modelcontextprotocol.io](https://modelcontextprotocol.io/introduction) |
| Building Effective Agents | Anthropic research | [anthropic.com/research/building-effective-agents](https://www.anthropic.com/research/building-effective-agents) |

### Financial Knowledge
| Resource | What It Covers | Link |
|---|---|---|
| Corporate Finance Institute (free) | Financial modeling, valuation | [corporatefinanceinstitute.com](https://corporatefinanceinstitute.com) |
| Investopedia | Financial concepts | [investopedia.com](https://www.investopedia.com) |
| Damodaran Online | Valuation, corporate finance | [pages.stern.nyu.edu/~adamodar](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/) |
| Wall Street Prep (free articles) | Financial modeling | [wallstreetprep.com/knowledge](https://www.wallstreetprep.com/knowledge/) |
| CFA Institute Research Foundation | Advanced finance topics | [rpc.cfainstitute.org](https://rpc.cfainstitute.org) |

### Compliance
| Resource | What It Covers | Link |
|---|---|---|
| FINRA 2026 Oversight Report | AI compliance rules | [finra.org/rules-guidance/guidance/reports/2026-finra-annual-regulatory-oversight-report](https://www.finra.org/rules-guidance/guidance/reports/2026-finra-annual-regulatory-oversight-report/gen-ai) |
| SEC 2026 Exam Priorities | SEC AI enforcement | [sec.gov/files/2026-exam-priorities.pdf](https://www.sec.gov/files/2026-exam-priorities.pdf) |
| GDPR Overview | Data privacy | [gdpr.eu](https://gdpr.eu/what-is-gdpr/) |
| NIST AI RMF | AI risk framework | [nist.gov/artificial-intelligence](https://www.nist.gov/artificial-intelligence) |

### MCP Servers for Finance
| Resource | What It Covers | Link |
|---|---|---|
| financial-datasets MCP | Fundamentals data | [github.com/financial-datasets/mcp-server](https://github.com/financial-datasets/mcp-server) |
| Yahoo Finance MCP | Prices, financials, news | [github.com/Alex2Yang97/yahoo-finance-mcp](https://github.com/Alex2Yang97/yahoo-finance-mcp) |
| Alpha Vantage MCP | Real-time market data | [mcp.alphavantage.co](https://mcp.alphavantage.co/) |
| finance-tools MCP | Macro data (FRED) | [github.com/VoxLink-org/finance-tools-mcp](https://github.com/VoxLink-org/finance-tools-mcp) |

---

## Weekly Time Budget

| Week | Total Hours | Split |
|---|---|---|
| Week 1 (Python basics) | 8–10 hrs | 4 hrs learning + 4–6 hrs hands-on |
| Week 2 (Excel + Modeling) | 8–10 hrs | 3 hrs learning + 5–7 hrs building |
| Week 3 (SQL) | 8–10 hrs | 4 hrs learning + 4–6 hrs building |
| Week 4 (Agents + MCP) | 10–12 hrs | 4 hrs learning + 6–8 hrs building |
| Week 5 (Compliance) | 8–10 hrs | 6 hrs learning + 2–4 hrs applying |
| Week 6 (Capstone) | 12–15 hrs | Full building project |
| **Total** | **54–67 hrs** | **~10 hrs/week** |

---

*You do not have to be perfect. You have to be started.*

*Every project you build, every concept you understand, every compliance risk you can articulate — that is real, compounding career capital that your peers who stayed purely in traditional finance are not building.*

*Six weeks from today, you will have three projects on GitHub, a working vocabulary in Python and SQL, practical experience with AI agents and MCP servers, and a compliance mindset that most finance professionals five years your senior do not have.*

*Start with Day 1. That is the only task on your list right now.*

---

*Study plan compiled: March 2026*
*All resources verified as free and publicly accessible*
