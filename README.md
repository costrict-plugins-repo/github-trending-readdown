# readdown — Claude Code Plugin

Fetch web pages and convert HTML to clean, LLM-optimized Markdown directly in Claude Code.

## What it does

- **Fetch any URL** and get clean Markdown with article content extracted
- **Convert HTML** strings to Markdown
- **Token estimation** — know how much context window a page will use
- **Metadata extraction** — title, author, date
- Strips navigation, ads, sidebars, and boilerplate automatically

## Install

In Claude Code, run:

```
/install-plugin https://github.com/zcag/readdown-plugin
```

Or add manually to your Claude Code settings.

## Usage

Once installed, Claude can fetch and convert web pages:

> "Fetch https://example.com and summarize it"
> "Convert this HTML to markdown: <html>..."
> "How many tokens is this article?"

The plugin provides two MCP tools:

- **fetch_markdown** — fetch a URL and convert to Markdown
- **convert_html** — convert an HTML string to Markdown

## How it works

Uses [readdown](https://github.com/zcag/readdown) — a single-library replacement for `@mozilla/readability` + `turndown`. Extracts article content and converts to clean Markdown optimized for LLMs.

- No browser needed (uses linkedom, not Playwright/Puppeteer)
- Fast (~3ms per article)
- Small footprint (5KB core vs 65KB for readability+turndown)

## License

MIT
