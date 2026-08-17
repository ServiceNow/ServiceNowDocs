---
title: Agents and skills inventory
description: The ServiceNow Otto for AI Control Tower plugin \(com.sn\_aict\_genai\) includes agents and skills that enhance the AI asset management and governance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-agents-skills.html
release: zurich
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [generative AI, agentic AI, agents, skills]
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# Agents and skills inventory

The ServiceNow Otto for AI Control Tower plugin \(com.sn\_aict\_genai\) includes agents and skills that enhance the AI asset management and governance.

## Agents and skills overview

The AI Control Tower agents and skills inventory details agent functions and skill descriptions within their respective interface plugins.

-   Agents perform tasks such as dormant asset deactivation, auto-populating AI asset descriptions, lifecycle task reminders, and outcome ranking.
-   Skills focus on tag generation, metadata enrichment recommendations, and AI governance insights including quality scoring and critical issue identification.
-   All agents are active with configurations and all skills are shipped inactive. The ServiceNow Otto for AI Control Tower \(`com.sn_aict_genai`\) plugin contains no agentic workflows.

**Note:** To use the agents and skills in AI Control Tower, install the ServiceNow Otto for AI Control Tower \(com.sn\_aict\_genai\) plugin.

## Agents

The agents are available on the AI Agent \[sn\_aia\_agent\] table and are active by default with their corresponding `sn_aia_agent_config` records. The agents are gated behind these interface plugins:

-   `com.sn_value_engine`
-   `com.sn_grc_ai_gov`
-   `com.sn_ai_opty_engine`

|Agent name|Interface plugin|Description|
|----------|----------------|-----------|
|Deactivate Dormant Asset|`com.sn_value_engine`|Autonomously analyzes and retires a single dormant AI asset by running comprehensive analysis and creating an offboarding change request.|
|AI Asset Description Auto-Populator|`com.sn_value_engine`|Generates and directly applies descriptions for AI assets missing description information. Uses vendor, model name, manufacturer, and category metadata.|
|Lifecycle Task Reminder Agent|`com.sn_grc_ai_gov`|Sends email reminders to assigned users for all overdue and dormant lifecycle tasks across high-priority AI assets.|
|Outcome Ranker Agent|`com.sn_ai_opty_engine`|Ranks AI insight outcomes by relevance per persona. Writes ranks via the Populate Outcome Ranks tool, then triggers prioritization recompute.|

## Skills

The skills are available on the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table. All six skills are shipped with inactive status and all the skills except for Tag Generator and Metadata Enrichment are gated behind these interface plugins:

-   `com.sn_ai_evaluations`
-   `com.sn_grc_ai_gov`

|Skill name|Interface plugin|Description|
|----------|----------------|-----------|
|AI Asset Tag Generator|Base plugin \(no gate\)|Derives tags for an AI asset based on its metadata, guided by existing tags present in the system.|
|AI Asset Metadata Enrichment Recommender|Base plugin \(no gate\)|Analyzes AI asset metadata and generates field-level enrichment recommendations using LLM inference and optional web search. Suggests values for description, use cases, and docs with confidence scoring.|
|Score and Categorization Insight|`com.sn_ai_evaluations`|Analyzes evaluated agent sessions to identify where quality and safety scores degrade across usage categories. Correlates session and trace-level metrics to pinpoint problem patterns.|
|Use and Purpose vs Intent Insight|`com.sn_ai_evaluations`|Compares an AI agent's registered use &amp; purpose against actual user interactions from session trace data. Detects divergence patterns and escalates meaningful mismatches.|
|Lifecycle Task Health Prioritization|`com.sn_grc_ai_gov`|Prioritizes lifecycle task health across AI governance tasks.|
|Critical Issue Identifier|`com.sn_grc_ai_gov`|Identifies and prioritizes critical AI governance issues.|

