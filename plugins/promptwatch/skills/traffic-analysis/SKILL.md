---
name: traffic-analysis
description: Analyze AI-referred traffic to the website — visitor trends, top pages, sources, devices, locations, and crawler activity. Use when the user asks "how much AI traffic do we get", "traffic from LLMs", "AI referral traffic", or wants to understand visitors coming from AI tools.
---

# AI Traffic Analysis

Analyze traffic referred to the user's website from AI tools and LLM platforms.

## Step 1: Identify context

Call `list_projects` to get projectId.

## Step 2: Gather traffic data

Make these calls (default: last 30 days):

1. **`get_visitor_total`** — total AI-referred visitor counts over time
2. **`get_visitor_trend`** — visitor trends broken down by referrer
3. **`get_visitor_referrer_stats`** — referrer stats with period-over-period comparison
4. **`get_visitor_top_pages`** — which pages receive the most AI-referred traffic
5. **`get_visitor_top_sources`** — top referral sources (ChatGPT, Perplexity, etc.)
6. **`get_visitor_top_browsers`** — browser distribution
7. **`get_visitor_top_devices`** — device distribution
8. **`get_visitor_top_locations`** — geographic distribution

## Step 3: Gather crawler data

1. **`get_crawler_trend`** — AI bot crawl activity over time
2. **`get_top_crawler_pages`** — most-crawled pages by AI bots

## Step 4: Compile the report

### Report Structure

1. **Traffic Overview** — total AI-referred visits, trend direction, period-over-period change
2. **Top Referral Sources** — which AI platforms drive the most traffic (table with counts and %)
3. **Top Landing Pages** — pages receiving the most AI traffic
4. **Geographic Breakdown** — where visitors are coming from
5. **Device & Browser** — how AI-referred visitors browse
6. **Crawler Activity** — which AI bots crawl the site, frequency trends
7. **Most Crawled Pages** — what AI bots are indexing
8. **Correlation Insights** — do crawled pages correlate with cited pages? Do citation improvements drive traffic?

### Key Insights

- Which AI platform drives the most valuable traffic
- Pages that get crawled but not cited (optimization opportunity)
- Pages that get cited but not crawled (may use cached data)
- Traffic growth/decline trends by source
