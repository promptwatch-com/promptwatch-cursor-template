---
name: content-gap-analysis
description: Identify content gaps where LLMs lack coverage of the brand and get actionable recommendations. Use when the user asks "what content should I create", "content gaps", "where am I missing", or wants to improve AI visibility through content.
---

# Content Gap Analysis

Identify prompts and topics where LLMs don't mention or adequately cover the user's brand, and provide actionable content recommendations.

## Step 1: Identify context

Call `list_projects` to get the projectId.

## Step 2: Get overview stats

Call **`get_content_gap_stats`** to understand the overall coverage picture — how many prompts have coverage vs. gaps.

## Step 3: Find gap prompts

Call **`list_content_gap_prompts`** with:
- `hasCoverage: false` to find prompts where the brand is NOT mentioned
- Sort by relevance or gap score
- Page through results if needed

Also call with `hasCoverage: true` to see where coverage exists (for comparison).

## Step 4: Deep-dive on specific gaps

For the most impactful gap prompts, call:
- **`get_content_gap_latest`** — latest analysis showing what LLMs say and why the brand is missing
- **`get_content_gap_recommendations`** — specific content recommendations to fill the gap

## Step 5: Check query fanouts

Call **`list_query_fanouts`** to see how ChatGPT expands queries — this reveals related questions the brand should also cover.

## Step 6: Compile the report

### Report Structure

1. **Coverage Overview** — X% of tracked prompts mention the brand, Y% have gaps
2. **High-Priority Gaps** — prompts with the most search/query volume where the brand is absent
3. **Content Recommendations** — specific pages or articles to create, grouped by topic
4. **Query Fanout Opportunities** — related questions to target
5. **Quick Wins** — gaps that could be filled with minor content updates
6. **Strategic Gaps** — gaps requiring new content or authority building

### Prioritization

Rank gaps by:
- Prompt type (recommendation prompts are highest intent)
- Number of LLMs where the gap exists
- Competitor presence (high competitor mention = urgent)
