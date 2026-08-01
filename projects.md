---
layout: page
title: Recent Projects
description: >
  Recent experimental tooling for making engineering knowledge usable by AI agents.
---

1. this list will be replaced by the toc
{:toc .large-only}

Documentation debt doesn't disappear when you adopt AI. It compounds. These are the tools and investigations I've built to find out where, and what to do once you can see it.

---

### markdown-ia

**A Claude Code plugin for information-architecture analysis of Markdown documentation corpora**

Three skills, meant to run in sequence: corpus discovery (what exists, how it's organized, what's missing), content model discovery (inferring document types and metadata schemas without a predefined structure), and vocabulary governance (terminology, tagging, and taxonomy consistency). Tested against real corpora.
This is the one project here that's public. MIT licensed, free to use.

[View on GitHub →](https://github.com/JoyceMarieStack/markdown-ia-skills)

---

### policy-corpus-audit

**Structuring 103 architecture standards into something an agent can actually use**

I applied a five-facet content model to classify 103 approved architecture standards, decomposed the corpus into 167 discrete knowledge objects with explicit chunk boundaries, and distilled each standard down to its MUST / MUST NOT / SHOULD / MAY imperatives with cross-reference paths for dependency traversal.

The finding that mattered most wasn't in the content: it was in the permission boundaries. Roughly a third of linked normative content sits behind authentication and is unreachable to an agent in a default configuration. No amount of restructuring fixes that until someone surfaces it. I also built a Knowledge Acquisition Cost model scoring the ten most convoluted compliance journeys by documents consulted, repositories crossed, and terminology shifts encountered, mapped directly to where agents hallucinate or stall.

[Read the write-up →](https://usecommune.com/n/joycestack/a/auditing-docs-for-ai-readiness-a-knowledge-engineering-self){:.btn}

---

### adr-pipeline

**2,677 architecture decisions, and a vocabulary too thin to search them**

An end-to-end pipeline that scraped 2,677 Architecture Decision Records from 174 repositories across four GitHub organizations, ran automated term extraction to build a controlled vocabulary with synonym mappings, and semantically clustered the results to surface what an organization has actually been deciding.

62% of ADRs lean on words like *data*, *service*, and *api*, terms with no discriminating signal. That means the corpus can't be reliably retrieved, filtered, or governed until the vocabulary is normalized first. The pipeline produces a per-ADR completeness score, an interactive discovery dashboard, and a standards compliance audit.

---

### termdrift

**When the same audit concept has four different names, and none of them are official**

A vocabulary pipeline auditing synonym fragmentation in enterprise compliance specs. I found four competing terms for the same audit concept spread across eight repositories (none defined in any approved standard) and traced how that fragmentation creates compliance gaps invisible to both human and LLM-assisted review.

A parallel experiment made the stakes concrete: a MUST-level immutability constraint failed to propagate to the database enforcement surface, because of a single missing SQL statement. Three separate AI critics reviewed the code and missed it. Vocabulary problems and enforcement problems turn out to be the same problem, wearing different clothes.

Not the same thing as markdown-ia's vocabulary governance skill. Different corpus, different pipeline, built independently. Vocabulary problems just keep showing up in this work.

---

### agent-ready-docs → ai-agent-reading-experiments

**I shipped the tool before I had evidence it measured anything real**

`agent-ready-docs` is a CLI that scores repositories on how well their documentation is structured for AI agents: file completeness, token cost per document, and more. I built it on intuition, before I had proof that any of it affected agent outcomes.

`ai-agent-reading-experiments` is the research that should have come first. A Python test harness gave an agent a controlled corpus of 45 documents and ran 22 hypothesis-driven experiments, each isolating a single variable, run 3–5 times across read-only and shell-enabled conditions. The honest finding: Markdown structure changed almost nothing. What mattered was whether the content existed at all, and whether filenames used vocabulary an agent could navigate by. Heading spacing, code fence labels, table pipe style: no measurable effect, in any condition tested. A missing file produces an honest failure. A missing section produces confident fabrication.

The lesson I keep relearning: build the outcome test before the metric you're going to ask people to optimize for.

[Agent Ready Docs — 5 Lessons Learned →](https://usecommune.com/n/joycestack/a/agent-ready-docs-5-lessons-learned){:.btn} [I Broke Every Table Formatting Rule →](https://usecommune.com/n/joycestack/a/i-broke-every-table-formatting-rule-and-claude-didn-t-care-e){:.btn} [My Docs Linter Passes Every Check →](https://usecommune.com/n/joycestack/a/my-docs-linter-passes-every-check-it-does-not-improve-agent){:.btn}

---

### doc-cost

**What does it cost an AI provider to read your documentation?**

Most teams don't think to ask. `doc-cost` scans every Markdown file in a repository, counts tokens with the same encoder used by GPT-4o and o-series models, and reports the financial cost per read, per provider. Documentation isn't free at inference time: a large `AGENTS.md` loaded into every session accumulates real spend across a team, and nobody's watching that number.

[Read the write-up →](https://usecommune.com/n/joycestack/a/how-much-context-do-your-docs-consume-experiments-in-finding){:.btn}

---

*Most of the projects above are internal work, not public repos, but real audits with real findings. If you want to talk through any of them, [get in touch](mailto:joyce@joycestack.com).*
