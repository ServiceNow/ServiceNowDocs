---
title: Performance Analytics indicators and the database tables
description: Learn about the out-of-the-box Performance Analytics \(PA\) indicators and the database tables that the AI Control Tower uses to calculate value.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Performance Analytics indicators and the database tables

Learn about the out-of-the-box Performance Analytics \(PA\) indicators and the database tables that the AI Control Tower uses to calculate value.

## Out-of-the-box PA indicators

|Metric field|PA indicator name|Description|
|------------|-----------------|-----------|
|Usage – Agent|AIValue - Daily Agent Executions|AI agent actions|
|Usage – Skills|AIValue - Daily Skill Executions|AI skill executions|
|Usage – AI Workflow|AIValue - Daily Agent Workflow Executions|AI workflow executions|
|Time Saved|AIValue - Daily Average Skill Assist; AIValue - Daily Average Agent Workflow Assists; AIValue - Daily Average Agent Assist|1 assist = 1 minute saved|
|Time Saved \(Token\)|AIValue Average RWTS per Skill|Read/write token count; applicable for AI skills only|
|Acceptance Rate|AIValue.CreatorMetrics.AcceptedCalls|Total accepted creator calls|

## Key database tables

|Table|Purpose|
|-----|-------|
|`sys_gen_ai_usage_log`|Stores daily skill and agent execution counts and assist averages.|
|`sn_ai_disc_ai_usage`|Stores usage data for third-party \(external\) agent invocations.|

The AI Control Tower derives two common measures from the `sys_gen_ai_usage_log` table:

-   **Daily Skill Executions**: the count of records in `sys_gen_ai_usage_log` for a specific asset on the previous day.
-   **Daily Average Skill Assist**: the average of the assists column in `sys_gen_ai_usage_log` for a specific asset on the previous day.

