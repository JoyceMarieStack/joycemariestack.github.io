# Hi, I'm Joyce 👋

### Docs as AI Infrastructure — making documentation work for AI agents, not just human readers

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/joycestack/)
[![Site](https://img.shields.io/badge/Site-joycemariestack.github.io-193747?style=for-the-badge)](https://joycemariestack.github.io/)

---

### 🔍 About Me

- 🧠 I treat Markdown corpora, ADRs, and architecture standards as datasets, and ask what an *agent* needs from them, not just a human reader.
- 📐 I built [**markdown-ia**](https://github.com/JoyceMarieStack/markdown-ia-skills), a Claude Code plugin with three skills that run in sequence — corpus discovery, content model discovery, and vocabulary governance — against a Markdown documentation corpus. Tested against real-world corpora (kubernetes/website, kubernetes/enhancements), not toy examples.
- 🕸️ I built an **ADR knowledge pipeline** that scraped 2,677 Architecture Decision Records across 174 repositories, clustered them semantically, and found that 62% rely on undifferentiated terms like *data*, *service*, and *api* — meaning most orgs can't reliably retrieve or govern their own decision history.
- 🧪 I run **empirical tests on what actually helps AI agents read docs**. 22 hypothesis-driven experiments later: Markdown linting rules had no measurable effect on accuracy. What mattered was whether content existed at all, and whether filenames used vocabulary an agent could navigate by.
- 🔒 I audit **permission boundaries and vocabulary drift** in enterprise documentation — the invisible failure modes where agents hallucinate or stall because a term isn't defined, or a link is auth-gated.
- 💸 I built a **token-cost scanner** for documentation, because nobody was asking what it actually costs an AI provider to read your docs at inference time.
- 📝 I write about what I find — an audit, not a solution. What I've learned and what I'm still figuring out.

### 🧰 Recent Projects

[**markdown-ia**](https://github.com/JoyceMarieStack/markdown-ia-skills) — Claude Code plugin: three skills for corpus discovery, content model discovery, and vocabulary governance on Markdown documentation corpora. Public, MIT licensed.

The rest of these are internal tools — not public repos, but the findings are real:

- **policy-corpus-audit** — classified 103 approved architecture standards into 167 knowledge objects with explicit chunk boundaries; found ~35% of linked normative content is auth-gated and unreachable to agents
- **adr-pipeline** — scraped and clustered 2,677 ADRs across 174 repos to surface undifferentiated vocabulary blocking retrieval and governance
- **termdrift** — audited synonym fragmentation across compliance specs; traced a MUST-level constraint that silently failed to propagate to enforcement
- **ai-agent-reading-experiments** — 22-experiment test harness isolating what actually affects agent reading accuracy — spoiler: not Markdown linting
- **agent-ready-docs** — CLI that scores repos on AI-agent readiness, built *before* the empirical evidence — and rebuilt once the evidence said otherwise
- **doc-cost** — scans a repo's Markdown and reports the token cost of reading it, per AI provider

### 🌱 How I work

I do my best work with autonomy, fast feedback, and room to chase the pattern nobody else has spotted. I'm direct — I'd rather raise the hard question early and have the work judged on its merits than manage around it. I want to keep learning; work that stops teaching me stops being worth doing. More on this on the [How I Work page](https://joycemariestack.github.io/how-i-work/).

### 📫 Elsewhere

[Site](https://joycemariestack.github.io/) · [Blog](https://joycemariestack.github.io/blog/) · [LinkedIn](https://www.linkedin.com/in/joycestack/) · [Contact](mailto:joyce@joycestack.com)
