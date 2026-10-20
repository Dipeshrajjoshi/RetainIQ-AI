# RetainIQ AI
## AI-Powered Customer Retention and Sales Analytics Platform

> ⚠️ **This is an independent portfolio project built with 100% synthetic data.**
> It does not represent any real insurance company, real customers, or real business results.
> All figures are generated for educational and demonstration purposes only.

---

## Project Overview

RetainIQ AI is a full-stack data analytics portfolio project that simulates an insurance company's
analytics workflow. It demonstrates skills in:

- **SQL Server / T-SQL** — schema design, analytical queries, KPI calculation, data-quality checks
- **Python / Pandas** — data generation, inspection, cleaning, KPI reconciliation
- **Excel** — independent metric validation using SUMIFS, COUNTIFS, XLOOKUP, PivotTables
- **Power BI / DAX** — dimensional modelling, DAX measures, interactive reports
- **AI-assisted insights** — safe, citation-grounded narrative generation using an LLM API

Built by **Dipesh Raj Joshi** as a learning and portfolio project targeting Junior Data Analyst /
Reporting Analyst roles in Ontario.

---

## Architecture Overview

```
Synthetic Data (Python / Faker)
        │
        ▼
CSV Files (data/raw/)
        │
        ├──► SQL Server ──► Analytical Queries ──► KPI outputs
        │                                               │
        ├──► Python / Pandas ──► Cleaned data ──────────┤
        │                    └──► KPI reconciliation ───┤
        │                                               │
        ├──► Excel ──► Independent validation ──────────┤
        │                                               │
        ├──► Power BI ──► Dashboards ◄── DAX measures   │
        │                                               │
        └──► AI Module ◄── Verified KPI summary ────────┘
                     └──► Plain-English insights (grounded)
```

---

## Quick Start

### 1. Clone the repo
```bash
git clone https://github.com/Dipeshrajjoshi/retainiq-ai.git
cd retainiq-ai
```

### 2. Set up Python environment
```bash
pip install -r requirements.txt
```

### 3. Copy environment template
```bash
cp .env.example .env
# Edit .env and add your OpenAI key (optional — mock mode works without it)
```

### 4. Generate synthetic data
```bash
python python/generate_data.py
```

### 5. Run data inspection
```bash
python python/inspect_data.py
```

### 6. Open the notebook
```bash
jupyter lab notebooks/exploratory_analysis.ipynb
```

### 7. SQL Server setup (optional — scripts are valid deliverables even without a local instance)
- Install [SQL Server Developer Edition](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) (free)
  or use [Azure Data Studio](https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio)
- Run `sql/01_create_schema.sql` → `sql/02_load_data.sql` → remaining scripts in order

---

## Module Breakdown

| Module | Tool | Status |
|--------|------|--------|
| A – SQL analytics | SQL Server / T-SQL | 🔄 In progress |
| B – Python pipeline | Python / Pandas | 🔄 In progress |
| C – Excel validation | Excel | 🔄 In progress |
| D – Power BI dashboards | Power BI Desktop / DAX | 🔄 In progress |
| E – AI insights | OpenAI API | 🔄 In progress |

---

## Key KPIs Tracked

| KPI | Definition |
|-----|-----------|
| Active Policies | Policies with status = 'Active' at the report date |
| Lapsed Policies | Policies with status = 'Lapsed' in the period |
| Retention Rate | Active policies ÷ (Active + Lapsed) in the period |
| Lapse Rate | Lapsed ÷ (Active + Lapsed) in the period |
| Contact Rate | Contacted leads ÷ total leads in the period |
| Conversion Rate | Converted leads ÷ contacted leads in the period |
| Data Quality Issue Count | Records failing defined validation rules |

> Full definitions, formulas, and edge-case handling: see [docs/kpi_definitions.md](docs/kpi_definitions.md)

---

## Tests

See [tests/](tests/) for the test suite.

| Test Category | Executed | Passed | Failed | Notes |
|--------------|----------|--------|--------|-------|
| Data – PK uniqueness | ✅ | – | – | Run after generate_data.py |
| Data – FK integrity | ✅ | – | – | |
| Data – valid categories | ✅ | – | – | |
| SQL – KPI reconciliation | 🔄 | – | – | Requires SQL Server |
| Python – KPI reconciliation | ✅ | – | – | |
| AI – unsupported claims | ✅ | – | – | Mock mode |

> Results will be updated as each stage is completed.

---

## Known Limitations

See [docs/limitations.md](docs/limitations.md) for a full list.

Short summary:
- SQL Server is not available locally; T-SQL scripts are written for SQL Server dialect and must be run
  in SSMS, Azure Data Studio, or a Docker SQL Server container.
- No real customer data is used. Synthetic data may not reflect true insurance industry distributions.
- Power BI requires Power BI Desktop (Windows). Mac users must use a Windows VM or the Power BI service.
- AI insights are grounded in supplied metrics only; the LLM is not the source of truth for any number.

---

## Portfolio Notes

- **Synthetic data only** — no real PII, no real company data.
- All KPIs are defined before implementation and reconciled across tools.
- Design decisions and assumptions are documented throughout.
- The project is intentionally built in small, testable stages to demonstrate process, not just output.

---

## Contact

**Dipesh Raj Joshi**
dipeshjoshi1000@gmail.com
GitHub: [Dipeshrajjoshi](https://github.com/Dipeshrajjoshi)
