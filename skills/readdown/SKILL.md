---
name: readdown
description: Convert web pages and HTML to clean, LLM-optimized Markdown using readdown. Extracts article content, strips navigation/ads/boilerplate, and estimates token count.
---

# readdown — HTML to LLM-ready Markdown

Use the `fetch_markdown` and `convert_html` MCP tools provided by the readdown MCP server to convert web content to clean Markdown.

## When to use

- User asks to fetch, read, or summarize a web page
- User provides a URL and wants the content as Markdown
- User has HTML content that needs to be converted to Markdown
- User wants to know the token count of a web page

## Tools available

### fetch_markdown
Fetches a URL and converts it to clean Markdown with metadata.

Parameters:
- `url` (required): The web page URL to fetch
- `include_header` (optional, default true): Include title/author/date header
- `raw` (optional, default false): Extract full page instead of main article only

### convert_html
Converts an HTML string to Markdown.

Parameters:
- `html` (required): The HTML content
- `url` (optional): Base URL for resolving relative links
- `include_header` (optional, default true): Include metadata header
- `raw` (optional, default false): Full page vs article extraction

## Output format

The tools return clean Markdown with:
- Article content extracted (navigation, ads, sidebars removed)
- Token count estimate and character count
- Title, author, and date metadata when available
- Properly formatted headings, lists, tables, code blocks, links, and images
