# Hi, I'm Rajkumar 👋

**Technical Architect · Test Automation · AI/ML · Quantitative Finance**

I build production-grade systems at the intersection of software engineering, AI, and financial analysis. Here's what I'm working on:

---

## 🔭 Active Projects

### 📈 NSE/BSE Stock Analyser *(Public)*
> Automated Indian equity research engine

Fully automated daily screener that takes every stock traded on NSE and BSE that day — about 5,200, counting a company listed on both exchanges once — down to the top 100 through a 3-stage funnel, holds back its Gold picks when the market regime turns bearish, and emails an 8-sheet Excel dashboard every trading morning — with forensic fundamentals, headline-based news analysis, and real outcome tracking for every Gold pick.

**Stack**: Python · GitHub Actions · SQLite · pandas · openpyxl · LLM via OpenAI-compatible API · Gmail SMTP · Windows Task Scheduler (weekly local NSE data job)
**Highlights**:
- 15-condition Gold filter + market-regime gate (Nifty vs 20-day SMA with a tolerance band)
- 7 fair-value models (DCF, Graham, PE, PB, EV/EBITDA, DDM, PEG) blended into a composite fair value and margin of safety
- Stop-loss and target sized from each stock's own volatility (ATR) and volatility regime; risk-parity position sizing keeps each pick at or below ~1% portfolio risk
- LLM news analysis that keeps an insider, bulk-deal or regulatory flag only when the model quotes the headline behind it
- NSE pledge/promoter data from a weekly local fetch, used only while fresh (≤ 14 days) — an honest blank beats a stale number
- Outcome tracking with a parallel *shadow* trailing stop, so exit rules change on evidence, not intuition
- Altman Z · Beneish M · Piotroski F (approximated from free data) · Sharpe/Sortino/Calmar · survivorship audit
- Nearly 100 regression tests, green on Linux and Windows; new guards are verified to fail when their bug is reintroduced

**Status**: Live — runs every trading day; logic held steady while a clean outcome cohort builds up before the next tuning round

🔗 [View Repository](https://github.com/rajiniottesting-coder/Sharemarket_Analyser_tool)

---

### 🤖 Multi-Agent Test Automation Framework *(Public)*
> AI agents that take a Jira story to a reviewed, executed test pull request

A six-agent pipeline — Impact Analyst → Test Designer → Coder → Reviewer → Runner → Reporter — that takes a Jira story to a reviewed, executed pull request. There is no orchestrator: state lives in Jira labels, marker comments and the PR, and a person approves at every gate.

**Stack**: Python · Playwright · pytest-bdd · any OpenAI-compatible LLM · Pydantic · Jira Cloud · GitHub Actions
**Highlights**:
- **Change-impact analysis (Agent 0)** — a code graph (scenario → step → method → selector) plus LLM judgement finds the existing tests a changed story affects; a person approves, rejects or retires each one, and a closed-unmerged PR is undone automatically
- Plan-then-generate code, one file at a time, behind a 29-check static validator gate with targeted repair
- Every model reply validated against a Pydantic schema; every model writer grounded in real method signatures
- Swappable tools behind two Protocols (Tracker, RepoHost); per-story token and cost ledger posted to Jira
- Nearly 3,000 offline unit tests, including a guard that fails if any framework file names the application under test

**Engineering principles**: application-agnostic framework code (verified by swapping in a different target app), validator/repair loops, adversarial break-it verification for every guard
**Status**: Active development — Agent 0 live and in validation

🔗 [View Repository](https://github.com/rajiniottesting-coder/multi-agent-test-automation)

---

### 🧠 AI/ML Learning & Experimentation *(Private)*
> Coursework and machine-learning experiments

Coursework notebooks (Semester 1, Programming in AI) — Python, NumPy, pandas, matplotlib, image processing, classical ML with scikit-learn (regression, classification, PCA, clustering) and deep learning (an ANN on MNIST and an RNN on IMDB in TensorFlow; PyTorch networks trained on a Colab GPU) — plus data-visualisation experiments with seaborn and plotly, run in Jupyter and Google Colab.

**Stack**: Python · PyTorch · TensorFlow · scikit-learn · Jupyter
**Status**: Ongoing
*(Private repository — experimentation and learning workspace)*

---

## 🛠️ Tech Stack

**Languages**: Python · SQL
**AI/ML**: LLM integration (Claude, OpenAI-compatible APIs) · LangChain · TensorFlow · PyTorch · scikit-learn
**Test Automation**: Playwright · pytest · pytest-bdd · multi-agent pipelines · change-impact analysis · Jira Cloud
**Data & Finance**: pandas · SQLite · openpyxl · NSE/BSE market data
**DevOps**: GitHub Actions · CI/CD pipelines · branch protection · regression testing

---

## 📊 What I focus on

- **Institutional-quality engineering** — my production projects ship with regression tests, proper documentation, and production-grade error handling
- **AI-augmented workflows** — using LLMs not as toys but as production components, with guardrails that make their output verifiable
- **Honest measurement** — if a system produces numbers (stock picks, test results, model accuracy), those numbers must be verifiable and auditable

---

## 📫 Get in touch

- 💼 [LinkedIn](https://www.linkedin.com/in/raj-kumar-7b32ab21b)
- 📧 rajiniottesting@gmail.com
- 🐙 [GitHub](https://github.com/rajiniottesting-coder)

---

*The private learning repository is available for review on request — reach out via LinkedIn or email.*
