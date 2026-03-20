---
name: citation-analysis
description: Analyze which sources LLMs cite when mentioning the brand — top domains, pages, citation rank, self-citation frequency. Use when the user asks "who cites us", "citation report", "where are LLMs getting their info", or wants to understand citation sources.
---

# Citation Analysis

Analyze the citation landscape — which sources LLMs reference when answering prompts related to the user's brand.

## Step 1: Identify context

Call `list_projects` to get the projectId. If multiple exist, ask which one.

Optionally call `list_monitors` to let the user filter by a specific monitor.

## Step 2: Gather citation data

Make these calls (default: last 30 days):

1. **`get_citations`** — overall citation analytics: top domains, URLs, traffic estimates, authority scores
2. **`get_citation_top_pages`** — most-cited pages with average rank position
3. **`get_citation_domains_by_llm`** — which domains each LLM model prefers
4. **`get_citation_llm_sources`** — which LLMs cite the most, and their source preferences
5. **`get_citation_rank_analysis`** — the user's domain citation rank over time
6. **`get_self_citation_frequency`** — how often the brand's own domain gets cited
7. **`get_citation_domains_over_time`** — citation trends by domain

## Step 3: Compile the report

### Report Structure

1. **Self-Citation Health** — is the brand's own site being cited? Frequency and trend
2. **Citation Rank** — average position when cited, trend over time
3. **Top Citing Sources** — which external domains appear most alongside the brand
4. **Per-LLM Breakdown** — which models cite differently (e.g., ChatGPT vs Perplexity vs Gemini)
5. **Top Cited Pages** — specific URLs that LLMs reference most
6. **Competitor Citations** — domains that compete for citation slots
7. **Recommendations** — content to create or optimize to improve citation presence

### Key Insights to Surface

- Pages the user controls that are highly cited (opportunity to optimize)
- Competitor domains that appear in citations (threats to address)
- LLMs that under-cite the brand vs. over-cite competitors
- Citation rank trends — improving or declining?
