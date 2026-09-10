---
title: Exclude external AI systems from a metric
description: Exclude one or more external AI systems from a specific metric, without changing that metric's configuration for every other system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-exclude-ai-systems-external.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure evaluation scoring for external AI systems, Configure, Monitoring and evaluating AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Exclude external AI systems from a metric

Exclude one or more external AI systems from a specific metric, without changing that metric's configuration for every other system.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

You can optionally exclude one or more AI systems from a single metric without affecting other external AI systems. For example, if one agent occasionally handles data that would otherwise fail a secrets detection metric, you can exclude just that agent from that one metric while still scoring it against everything else.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  On the **AI evaluations** sub-tab, select **External AI systems**.

3.  In the Evaluation metrics for Agentic AI section, find the metric that you want to exclude AI systems from.

4.  In the **Excluded AI systems** column, select the pencil icon.

5.  In the side panel, search or filter to find the AI systems that you want to exclude.

    -   Fixed filters limit the systems to those that are managed, agentic, and have evaluation enabled.
    -   You can find systems where a low score reflects a mismatch with the metric rather than an actual issue by viewing AI systems in the **Lowest performing** tab.
    -   You can find systems that consistently perform well on this metric and don't need continued scrutiny by viewing AI systems in the **Highest performing** tab.
6.  Select the AI systems that you want to exclude.

    Each selected AI system appears as a removable pill after the list.

7.  Select **Save**.

    If a selected metric is currently used in a published evaluation template or a compliance evaluation, the exclusion isn't saved, and you're shown which templates or evaluations are using it so you can resolve that first.


## Result

The metric no longer evaluates the AI systems that you excluded. They remain subject to every other metric in your global configuration, and their existing scores for other metrics are unaffected.

**Parent Topic:**[Configure evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-external-ai-systems.md)

**Related topics**  


[Activate evaluation scoring for external AI systems]()

[Configure global metrics for external AI systems]()

[Configure asset-specific metrics for external AI systems]()

