# For Teams Feeling Stuck on Docs as Code and Looking for a Practical Starting Point

## Introduction

You want to do the right thing and improve the documentation in your team area.

You're time-poor.

You have documentation in Confluence. Some of it is in Markdown.

What even is Backstage? Do we even need it?

You've even bookmarked a time slot to "sort this out"… and somehow you feel completely paralysed.

Your head is about to explode 💥

## So. How do I start?

### 1. Start Small - Start Tracking Repeat Questions

Don't try to fix everything at once.

Start by tracking the repeat questions in Slack / meetings. Your goal is to reduce one category of repeat questions.

### 2. Identify patterns

There are a few easy ways to do this:

- Keep a basic counter on a team page of the types of questions asked each week
  (for example: "environment setup", "Kafka config")

- Chances are, you already know what these questions are.

- Group questions by theme, then decide what kind of document is actually needed:
  - How-to guide
  - Tutorial
  - Reference
  - Explanation (architecture or how something works)

### 3. Document Top 3 (Week 2)

Pick the top 3 most asked questions and write focused, lightweight docs.

```text
docs/
├── how-to/
│   └── deploy-first-module.md         # "How do I deploy?"
├── explanation/
│   └── repo-structure.md              # "Why so many folders?"
├── reference/
│   └── terraform-variable-reference.md # "What does this var do?"
```

### 4. Close the loop

Next time someone asks you can share a link to that document.

If something is unclear, take the feedback and iterate on the document.

Do not do what you would normally do: answer the question in Slack

**Why?**: this undermines the document and causes the Docs Feedback Loop of Doom

## Why this approach works?

**Addressing repeat questions:**

- Reduces interrupt-driven work (huge if you're a small team)

- Solves real problems based on real questions
  - There's no point writing a big tutorial if nobody needs it.

- Builds confidence through quick wins
  - You're exercising your "docs muscle"

- Creates a feedback loop
  - You'll know docs are working when the questions stop
    (and you consistently point people back to them)

## Pro Tips: Measure It

### Metrics

Track for 1 month:

- Questions asked Week 1: ___

- Questions asked Week 4: ___

- Time saved: (reduction × 5 min/question)

If this drops even 30%, you've proven ROI and can advocate for more docs time.

- Share your time savings after Week 4

- "I got back 2 hours/week by documenting these 5 things"

That's how documentation stops being "nice to have".

## Confluence Migration

Before you move Confluence docs into Markdown, ask your users one simple question.

**"Is this document useful?"**

- If yes → high priority

- If no → low priority or archive.

Check the readership stats on the page. How frequently are people referencing the document. Let real usage drive what you migrate.
