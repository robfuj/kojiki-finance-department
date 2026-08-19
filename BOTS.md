# Bots of Finance  (docx S5 candidate menu)

These are the **Major sub-functions** of Finance from the spec. Each is a bot — a
child decision system that can be instantiated to do the actual work.

## Install flow (matches the Orientation Protocol)
1. **Orient** — the agent runs the Kojiki Orientation Protocol (name / industry /
   jurisdiction / siblings).
2. **Research** — the agent researches the field and decides which sub-functions this
   specific org needs.
3. **Install** — instantiate only the chosen bots:
   ```bash
   cd bots
   python3 install_bots.py brand growth performance-marketing
   ```
   (use the slugs listed below; omit args to install all). Each installed bot becomes a
   full decision system under `bots/<slug>/` with README + AGENT.md + schemas + a stub
   decision record, and registers under this department's group_id for handoffs.

Total candidates: 8.

- `accounting` — **Accounting**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
- `fp-a` — **FP&A**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
- `treasury` — **Treasury**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
- `tax` — **Tax**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
- `financial-control` — **Financial Control**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
- `capital-management` — **Capital Management**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
- `investor-relations` — **Investor Relations**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
- `financial-strategy` — **Financial Strategy**  ·  titles: CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director
