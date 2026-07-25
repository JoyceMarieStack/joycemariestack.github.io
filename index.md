---
layout: default
title: Welcome
---

<section class="hero wrap">
  <h1>Joyce Stack</h1>
  <p class="role">Docs as AI Infrastructure</p>
  <p class="bio">Researching what AI-native repositories actually need to look like.</p>
  <div class="cta-row">
    <a class="btn btn-primary" href="#writing">Read my writing</a>
    <a class="btn btn-secondary" href="#projects">View projects</a>
  </div>
</section>

<section class="section wrap">
  <h2 class="section-title">What I do</h2>
  <div class="prose">
    <p>Twenty years in software. Developer, architect, API advocate. And now, apparently, the person who asks awkward questions of corpora.</p>
    <p>That last part wasn't planned. It started with a docs problem nobody assigned to me, which led to a question I hadn't taken seriously before: what does documentation actually need to look like when AI agents are reading it, not humans?</p>
    <p>Documentation debt doesn't disappear when you adopt AI. It compounds.</p>
    <p>What I keep finding: the problems that look like documentation problems aren't. They're about how engineering knowledge is structured, named, and organized, and whether humans and AI systems can actually use it. That's made me a better reader of engineering knowledge — which turns out to be the harder skill.</p>
    <p>Making the invisible visible — dashboards, gap analysis, cost checkers — that's the actual work.</p>
    <p>Short answer so far, on the research itself: structure barely matters. Terminology does. If a document fits in an agent's context window, it gets read in full — the headings and hierarchy you spent hours perfecting are close to irrelevant. What breaks agents is a term used three different ways across three different files. That's not a formatting problem. It's an instrumentation gap — the kind of thing that looks fine until you check whether it's actually verified everywhere it needs to be.</p>
    <p>I'm not sure that's documentation anymore. It's agent reliability work. Knowledge architecture.</p>
  </div>
</section>

<section class="section wrap" id="projects">
  <h2 class="section-title">Projects</h2>
  <div class="card-grid">
    <div class="card">
      <h3>Agent Ready Docs CLI</h3>
      <p>A command-line tool that checks whether a repository is actually usable by an AI coding agent — not "does it have a README," but "can an agent extract what it needs from what's here."</p>
      <a class="read-more" href="#" title="Add the link once this project is published">[→ read more]</a>
    </div>
    <div class="card">
      <h3>ADR Ingestion Pipeline</h3>
      <p>Architecture Decision Records are usually a graveyard: written once, never queried again. This pipeline cleans, clusters, and makes them queryable — turning years of buried decisions into something you can actually search.</p>
      <a class="read-more" href="#" title="Add the link once this project is published">[→ read more]</a>
    </div>
    <div class="card">
      <h3>Lexi</h3>
      <p>A gap analysis tool comparing how terms are <em>defined</em> in architecture standards against how they're actually <em>used</em> in spec documents. The gaps are the interesting part.</p>
      <a class="read-more" href="#" title="Add the link once this project is published">[→ read more]</a>
    </div>
    <div class="card">
      <h3>Docs Context &amp; Cost Checker</h3>
      <p>Measures how much of an AI coding tool's context window a repository's documentation actually consumes — and whether that spend is buying anything.</p>
      <a class="read-more" href="#" title="Add the link once this project is published">[→ read more]</a>
    </div>
    <div class="card">
      <h3>Docs-as-Code Standard</h3>
      <p>Started as a way of working. Became an official architectural standard. Nobody planned that; it just turned out to be the right answer often enough that it stuck.</p>
      <a class="read-more" href="#" title="Add the link once this project is published">[→ read more]</a>
    </div>
  </div>
</section>

<section class="section wrap">
  <h2 class="section-title">Research</h2>
  <div class="card-grid">
    <div class="card">
      <h3>Instrumentation Gaps in Spec-Driven Development: Evidence from Three Cases <span class="tag-inprogress">in progress</span></h3>
      <p>A legal requirement can be fully met at one layer of a system and silently unmet at another — and every document describing the system can still say it's fine. This is a study of why that happens and how to catch it before an audit does.</p>
      <a class="read-more" href="#" title="Add the link once this is published">[→ read more]</a>
    </div>
  </div>
  <p class="section-intro" style="margin-top: 20px;">This is empirical work, not a finished framework. I'm gathering cases, not selling conclusions.</p>
</section>

<section class="section wrap" id="writing">
  <h2 class="section-title">Writing</h2>
  <p class="section-intro">Recent posts on documentation, architecture, and what "AI-native" actually requires:</p>
  <div class="card-grid">
    <a class="card" href="docs/for-devs-who-want-fewer-interruptions">
      <h3>For Developers Who Want Fewer Interruptions</h3>
      <p>Write docs that deflect Slack questions, and beat the "Docs Feedback Loop of Doom."</p>
    </a>
    <a class="card" href="docs/getting-started-with-docs-as-code">
      <h3>Getting Started with Docs as Code</h3>
      <p>A practical starting point for teams that feel stuck moving off Confluence and into Markdown.</p>
    </a>
  </div>
</section>

<section class="section wrap">
  <h2 class="section-title">Elsewhere</h2>
  <p class="section-intro">
    <a href="#" title="Add your LinkedIn URL">[LinkedIn]</a> ·
    <a href="#" title="Add your GitHub URL">[GitHub]</a> ·
    <a href="#" title="Add your contact info">[Contact]</a>
  </p>
</section>
