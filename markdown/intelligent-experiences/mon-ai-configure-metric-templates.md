---
title: Configure an evaluation metric template
description: Adjust the scoring formula for a metric template to change which metrics contribute to quality or safety scores, or to change how much weight each metric carries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-configure-metric-templates.html
release: zurich
topic_type: task
last_updated: "2026-04-03"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Configure an evaluation metric template

Adjust the scoring formula for a metric template to change which metrics contribute to quality or safety scores, or to change how much weight each metric carries.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

You can adjust a metric's influence on the score, add metrics previously tracked for visibility only, or remove metrics that aren't required by editing a metric template. Changes apply to new evaluation sessions only. Existing sessions keep the scores they were originally calculated with.

For the full list of quality and safety metrics, see [Evaluation metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-evaluation-metrics-reference.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  Select the **Metric templates** sub-tab.

3.  Select the metric template that you want to edit.

4.  Update the metric template as needed.

    For example:

    -   Select the primary metric, which is required for every measure.
    -   Adjust a metric's weight to increase or decrease its influence on the score.
    -   Add a metric by selecting **+ Add metrics** and assigning a weight.
    -   Remove a metric from the formula.
    After any change, verify that all weights still sum to 100%.

    **Note:** Only metrics that are enabled for scoring on the AI evaluations page are available to add. See [Activate evaluation scoring for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-servicenow-ai-system.md) and [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

5.  Verify the updated formula by expanding the **How is this score calculated?** section.


## Result

The updated formula is applied to new evaluation sessions. Scores on the monitoring overview reflect the updated formula as new data is collected.

**Parent Topic:**[Configuring monitoring and evaluations in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configuring-aict-evaluations.md)

