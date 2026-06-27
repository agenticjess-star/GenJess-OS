---
name: firecrawl
 description: Elite web research and structured data extraction using Firecrawl. Use for wide-net discovery, deep site crawling, markdown extraction, and evidence gathering on any domain or topic.
license: MIT
metadata:
  version: "1.0"
  author: JAW (Jesse’s Agentic Workforce)
---

# Firecrawl Skill

You are an expert at using Firecrawl for high-quality, efficient web research.

## When to Use This Skill

- User asks for research on a topic, company, domain, or competitive landscape.
- Need to gather current, structured information from websites.
- Require markdown + metadata from multiple pages.
- Want to do wide discovery first (map) then targeted deep dives (crawl/batch).

## Core Principles

1. **Wide Net First**: Always start with `/map` for landscape discovery when possible (1 credit flat).
2. **Targeted Depth Second**: Follow up with `/crawl` or `/batch-scrape` on high-value URLs.
3. **Evidence Logging**: Every significant result should be logged as evidence with verification status.
4. **Append Context**: Intelligently add relevant context the user might have missed.
5. **Follow Evidence-First Sensemaking**: Frame → Uncertainty Map → Retrieve → Synthesize → Deliver.

## Recommended Workflow

1. Use `/map` on key domains with relevant `search` terms.
2. Review results and select the most promising URLs.
3. Use `/crawl` or `/batch-scrape` with `formats: ["markdown", "metadata"]` on selected URLs.
4. Store important findings with proper tags and verification status.
5. Synthesize into clear, actionable output.

## Parameters & Best Practices

- Prefer `map` for initial discovery (cheap + fast).
- Use higher `limit` values (50–200+) for meaningful coverage.
- Set `sitemap: "include"` when doing broad research.
- Use `includePaths` / `excludePaths` to focus crawls.
- Always request `markdown` + `metadata`.

## Error Handling

- If a crawl returns limited results, try adjusting `includePaths` or increasing `limit`.
- For dynamic/JS-heavy sites, note limitations and suggest alternatives.
- Log credit usage when doing large operations.

## Examples

**Good prompt for map:**
"Map the main sections and key pages of anthropic.com and firecrawl.dev related to agent skills and workflows."

**Good prompt for crawl:**
"Crawl the documentation sections of these repos with focus on skill definitions and workflow patterns."

This skill makes you significantly more effective at research than using generic web search alone.