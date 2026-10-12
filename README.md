# Hi, I'm Rajkumar 👋

**Technical Architect · Test Automation · AI/ML · Quantitative Finance**

I build production-grade systems at the intersection of software engineering, AI, and financial analysis. Here's what I'm working on:

---

## 🔭 Active Projects

### 📈 NSE/BSE Stock Analyser *(Public)*
> Institutional-grade Indian equity research engine

Fully automated daily screener that filters 5,000+ NSE/BSE stocks down to the top 100 through a 3-stage funnel, gates every buy candidate against the market regime, and delivers a professional Excel dashboard every morning — with forensic fundamentals, evidence-backed news analysis, and real outcome tracking for every pick.

**Stack**: Python · GitHub Actions · SQLite · openpyxl · LLM via OpenAI-compatible API · Windows Task Scheduler (local NSE data job)
**Highlights**:
- 15-condition Gold filter + market-regime gate (Nifty vs 20-day SMA with a tolerance band)
- Regime-aware stop-loss and target, sized from each stock's own volatility (ATR)
- LLM news extraction that must quote the headline behind every fact — no invented numbers
- Outcome tracking with a parallel *shadow* trailing stop, so exit rules change on evidence, not intuition
- Altman Z · Beneish M · Piotroski · Sharpe/Sortino/Calmar · survivorship audit
- 92 regression tests, each guard verified to fail when its bug is reintroduced

🔗 [View Repository](https://github.com/rajiniottesting-coder/Sharemarket_Analyser_tool)

---

### 🤖 Multi-Agent Test Automation Framework *(Private)*
> Enterprise-grade QA orchestration using AI agents

A six-agent pipeline — Impact Analyst → Test Designer → Coder → Reviewer → Runner → Reporter — that takes a Jira story to a reviewed, executed pull request. There is no orchestrator: state lives in Jira labels, marker comments and the PR, and a person approves at every gate.

**Stack**: Python · Playwright · pytest-bdd · any OpenAI-compatible LLM · Pydantic · Jira Cloud · GitHub Actions
**Highlights**:
- **Change-impact analysis (Agent 0)** — a code graph (scenario → step → method → selector) plus LLM judgement finds the existing tests a changed story affects; a person approves, rejects or retires each one, and a closed-unmerged PR is undone automatically
- Plan-then-generate code, one file at a time, behind a 28-check static validator gate with targeted repair
- Every model reply validated against a Pydantic schema; every model writer grounded in real method signatures
- Swappable tools behind two Protocols (Tracker, RepoHost); per-story token and cost ledger posted to Jira
- ~2,780 offline unit tests, including a guard that fails if any framework file names the application under test

**Engineering principles**: application-agnostic framework code (verified by swapping in a different target app), validator/repair loops, adversarial break-it verification for every guard
**Status**: Active development — Agent 0 live and in validation
*(Code is private — available for review upon request)*

---

### 🧠 AI/ML Learning & Experimentation *(Private)*
> Applied machine learning and deep learning projects

Hands-on implementations covering classical ML (scikit-learn), deep learning (PyTorch, TensorFlow), data visualisation (matplotlib, seaborn, plotly), and exploratory data analysis — with Google Colab notebooks.

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

- **Institutional-quality engineering** — every project ships with regression tests, proper documentation, and production-grade error handling
- **AI-augmented workflows** — using LLMs not as toys but as production components, with guardrails that make their output verifiable
- **Honest measurement** — if a system produces numbers (stock picks, test results, model accuracy), those numbers must be verifiable and auditable

---

## 📫 Get in touch

- 💼 [LinkedIn](https://www.linkedin.com/in/raj-kumar-7b32ab21b)
- 📧 rajiniottesting@gmail.com
- 🐙 [GitHub](https://github.com/rajiniottesting-coder)

---

*Private repositories are available for review upon request — reach out via LinkedIn or email.*
