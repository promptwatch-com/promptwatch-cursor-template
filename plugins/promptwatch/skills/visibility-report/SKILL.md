---
name: visibility-report
description: Generate a comprehensive AI visibility report — brand mentions, sentiment, visibility trends across LLMs. Use when the user asks "how visible is my brand", "visibility report", "how are we doing in AI", or wants a dashboard-style overview.
---

# AI Visibility Report

Generate a comprehensive report on the user's brand visibility across AI/LLM responses.

## Step 1: Identify context

Call `list_projects` to identify the project. If multiple exist, ask which one. Store the `projectId`.

Call `list_monitors` with the projectId to get monitors and their current visibility metrics. This gives a quick overview.

## Step 2: Gather data

Make these calls (use the last 30 days as default date range unless the user specifies otherwise):

1. **`get_visibility_time_series`** — visibility score over time
2. **`get_mentions_time_series`** — brand mention frequency over time
3. **`get_sentiment_time_series`** — sentiment trends
4. **`get_responses_summary`** — total responses and mention counts
5. **`get_response_sentiment_distribution`** — positive/neutral/negative breakdown
6. **`get_top_competitors`** — who else is being mentioned

## Step 3: Compile the report

Present findings as a structured report:

### Report Structure

1. **Executive Summary** — one-paragraph overview of visibility health
2. **Visibility Score** — current score, trend direction, percentage change
3. **Mention Volume** — total mentions, trend over period
4. **Sentiment Analysis** — distribution (positive/neutral/negative), trend direction
5. **Competitor Landscape** — top competitors mentioned alongside the brand
6. **Per-Monitor Breakdown** — if multiple monitors, break down metrics per monitor
7. **Recommendations** — actionable next steps based on the data

### Formatting

- Use percentages and directional indicators (up/down arrows or text)
- Compare current period vs. previous period when data allows
- Highlight anomalies or significant changes
- Keep it scannable — use tables for multi-row data
