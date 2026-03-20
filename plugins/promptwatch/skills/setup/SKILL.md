---
name: setup
description: Onboard a user to PromptWatch — list projects, create a project, set up monitors, add brands and competitors. Use when the user says "set up promptwatch", "create a project", "add a monitor", or needs help getting started.
---

# PromptWatch Setup

Help the user get started with PromptWatch. Follow these steps in order, skipping any the user has already completed.

## Step 1: List existing projects

Call `list_projects` to see if the user already has projects. Show them and ask which one to work with, or offer to create a new one.

## Step 2: Create a project (if needed)

Ask for:
- **name** — the brand/product name
- **website** — the website URL to track

Optional: `countryCode`, `languageCode` for geo-targeting.

Call `create_project` with these values.

## Step 3: Set up the brand

Call `create_brand` with:
- `relation: "self"` — marks this as the user's own brand
- The brand name and URL from the project

Then ask if there are competitors to track. For each, call `create_brand` with `relation: "competitor"`.

## Step 4: Create a monitor

A monitor groups prompts under a specific tracking context (e.g., a product category, topic area).

Ask the user what topic/category they want to monitor. Call `create_monitor` with:
- `name` — descriptive name for the monitor
- `models` — which LLMs to track (call `list_models` first to show available options)

Optional: `languageCode`, `countryCode`, `personaId` for targeted monitoring.

## Step 5: Add prompts

Prompts are the actual questions that get sent to LLMs. Ask the user for prompts relevant to their monitor. Types:
- `informational` — "What is the best X?"
- `comparison` — "Compare X vs Y"
- `recommendation` — "Recommend a tool for X"

Use `create_prompt` for a single prompt or `create_prompts_bulk` for multiple.

## Step 6: Confirm setup

Summarize what was created: project, brands, monitors, prompts. Suggest the user check back in 24h for initial data, then use skills like `visibility-report` or `citation-analysis`.
