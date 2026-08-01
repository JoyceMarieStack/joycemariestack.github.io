# joycemariestack.github.io

Jekyll personal site using the **Hydejack Lite** (free) theme, via the `jekyll-theme-hydejack` gem — not the `github-pages` gem.

## Local dev

Ruby is managed by rbenv, pinned via `.ruby-version` (3.3.6). rbenv shims aren't on `PATH` by default in a fresh shell — run `eval "$(rbenv init -)"` before any `bundle`/`jekyll` command, or they'll silently use system Ruby (2.6.x) and fail dependency resolution.

```
eval "$(rbenv init -)"
bundle install
bundle exec jekyll build
bundle exec jekyll serve
```

## Deployment

GitHub Pages' default "Deploy from a branch" build only supports themes on its own allowlist — `jekyll-theme-hydejack` isn't on it. This repo deploys via `.github/workflows/pages.yml`, which builds with Bundler (the real `Gemfile`) and deploys via `actions/deploy-pages`. **Pages source in repo settings must be set to "GitHub Actions"**, not "Deploy from a branch," or the workflow's output is ignored (and you'll get failure emails from GitHub's own legacy builder trying and failing to find `jekyll-theme-hydejack` — recognizable by `/github/workspace/` paths and a `github-pages` gem version in the error).

**`Gemfile.lock` must stay committed, never gitignored.** It was gitignored once (a leftover from a generic Jekyll template) and CI broke with a bare `bundler ... exit code 17` — re-resolving dependencies from scratch on every push means any tiny upstream gem release can silently break the build with no code change here. Keep it locked to what's verified locally.

## Sitemap

- `/` (`index.md`) — short hook only, no nav-duplicate link list (nav in sidebar covers navigation)
- `/about/` (`about.md`) — full narrative + avatar photo
- `/projects/` (`projects.md`) — hardcoded per-project write-ups (not data-driven; `_data/projects.yml` was deleted once the content became bespoke prose instead of a generic loop)
- `/how-i-work/` (`how-i-work.md`) — in primary nav
- `/blog/` (`blog.md`) — **not a local Jekyll blog.** Links out to the Joyce Stack newsletter on Commune. Don't add `_posts/` expecting it to show here.

Nav is controlled by `menu:` in `_config.yml`.

## Writing voice

Copy on this site follows the tone/communication rules in `~/.claude/CLAUDE.md`
(user-level, not project-specific — applies everywhere, not just here). Key points:
dry/deadpan, no em dashes except pre-approved verbatim lines, no invented metrics,
no hedging. Read that file before drafting or editing any page copy.

## Known gotcha: raw HTML in Markdown

Kramdown only reliably recognizes a raw HTML block when the tag is **entirely on one line**, starting at column 0. Hydejack's `hy-img.html` include renders a multi-line `<img>` tag with blank/whitespace-only lines between attributes (from unused conditional branches) — using `{% include components/hy-img.html %}` directly in a page's Markdown source gets mangled into escaped, visible text instead of rendering as an image.

This *does* work inside `about.html`'s `<!--author-->` marker mechanism, because that substitution happens on already-converted HTML (post-kramdown), not raw Markdown source.

For any avatar/image added directly in a `.md` page's own content, write a single-line raw tag instead:

```html
<img src="/assets/img/avatar.jpg" alt="Joyce Stack" class="avatar" width="120" height="120" loading="lazy" />
```

## Site-wide CSS conventions (`_sass/my-style.scss`)

- **External links get the accent color automatically.** The rule targets
  the same selector the theme already uses to detect external links
  (`a[href*="://"]:not(.no-mark-external):not(.no-mark)`), not a manually
  applied class. Any link to an off-site URL gets colored automatically —
  don't add a `.external-link` class or similar per-link; it's redundant
  and was removed from `projects.md` for exactly this reason.
- **`.btn` links are always block-level, one per line, no icon.** The
  theme's `.btn` class is just `text-decoration: none` by default — nothing
  stops multiple `.btn` links from flowing onto the same line if they're
  written back-to-back in Markdown (this happened twice, on `/projects/`
  and `/blog/`, before the CSS was fixed). `.btn` is now `display: block`
  with its own `::after` icon suppressed (redundant since `.btn` link text
  always ends with its own "→"). This means new `.btn` links never need
  manual line-breaking in the Markdown source — the CSS handles it.

## Theme tier limits

Hydejack **Lite is free but has no portfolio or resume layout** — those are PRO-only ($99 one-time, adds portfolio/resume layouts, dark mode, search, removes branding). `/about/` and `/projects/` use the plain `about`/`page` layouts, hand-authored in Markdown, not the theme's project/resume system.

The "Powered by Hydejack" footer credit is hardcoded in the free version and can't be removed. `LICENSE.md`/`NOTICE.md`/`CHANGELOG.md` and their footer links were deliberately deleted from this site — that credit line is the only attribution kept.

## Sass deprecation warnings

`_config.yml`'s `sass:` block sets `quiet_deps` and `silence_deprecations` to suppress noisy but harmless warnings from Hydejack's own bundled Sass (old `@import` syntax, legacy color functions). These come from the theme, not this repo's code — don't try to "fix" them by editing vendored gem files.
