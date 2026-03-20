---
name: competitor-analysis
description: Deep competitive analysis in AI responses — compare brand visibility, sentiment, citations vs competitors across LLMs. Use when the user asks "how do we compare to competitors", "competitor analysis", "who's beating us in AI", or wants competitive intelligence.
---

# Competitor Analysis

Compare the user's brand against competitors across AI/LLM responses.

## Step 1: Identify context

Call `list_projects` to get projectId. Call `list_brands` with `relation: "competitor"` to see tracked competitors. If none exist, suggest using the `setup` skill to add competitors first.

## Step 2: Gather competitive data

Make these calls (default: last 30 days):

1. **`get_top_competitors`** — ranked list of most-mentioned competitors
2. **`get_competitor_heatmap`** — visibility matrix: competitors × LLM models
3. **`get_brand_visibility_over_time`** — visibility trend lines for all brands
4. **`get_mentions_time_series`** — mention volume over time (includes competitors)
5. **`get_citation_domains_over_time`** — how competitor domains trend in citations
6. **`get_citation_domains_by_llm`** — per-LLM citation preferences

## Step 3: Analyze responses

Call `list_responses` filtered by specific prompts to read actual LLM responses and see how competitors are positioned vs. the user's brand.

## Step 4: Compile the report

### Report Structure

1. **Competitive Overview** — ranked table of all brands by visibility score
2. **Head-to-Head Comparison** — user's brand vs. top 3 competitors with metrics
3. **LLM-by-LLM Breakdown** — which competitors dominate which LLMs (heatmap data)
4. **Visibility Trends** — who's gaining, who's declining over time
5. **Citation Battle** — whose content gets cited more and by which LLMs
6. **Sentiment Comparison** — how LLMs talk about each brand (positive/negative)
7. **Gap Opportunities** — prompts where competitors appear but the user's brand doesn't
8. **Strategic Recommendations** — specific actions to improve competitive position

### Key Metrics to Compare

- Visibility score (% of relevant prompts where mentioned)
- Mention frequency
- Citation rank
- Sentiment distribution
- Per-LLM strengths/weaknesses
