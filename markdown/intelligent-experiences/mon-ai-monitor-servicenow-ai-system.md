---
title: Activate evaluation scoring for ServiceNow AI systems
description: Assess the quality of your ServiceNow AI systems by activating evaluation scoring in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-monitor-servicenow-ai-system.html
release: zurich
topic_type: task
last_updated: "2026-07-13"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Activate evaluation scoring for ServiceNow AI systems

Assess the quality of your ServiceNow AI systems by activating evaluation scoring in AI Control Tower.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

ServiceNow AI systems are scored by the AI Skill Kit scoring engine. No additional configuration is required to collect trace data from ServiceNow AI systems.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  On the **AI evaluations** sub-tab, select **ServiceNow AI systems**.

3.  Set the **Activate** toggle to on.

4.  Update the sample rate.

    The sample rate determines what percentage of AI executions are evaluated. ServiceNow AI systems use a single sample rate for all metrics. The default is 100%. You can enter a lower percentage to evaluate fewer executions.

    1.  Enter the sample rate to use when evaluating ServiceNow AI systems.

    2.  Select **Update**.

5.  Review the quality metrics that are included by default.

    The following quality metrics are evaluated for ServiceNow AI systems by default.

    -   **Overall task completeness**

        Whether the agentic workflow completed its assigned task, including all required steps and proper resolution or escalation.

    -   **Tool calling correctness**

        Whether tool calls used correct parameters, formatting, and expected values.

    For a complete list of available metrics and their descriptions, see [Evaluation metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-evaluation-metrics-reference.md).

6.  Add or remove metrics that you want to evaluate.

    **Important:** Adding more metrics increases the visibility you gain into each session, but also increases assist usage to evaluate it. Select the metrics that give you the insight you need.

<table id="choicetable_add_remove_metrics_sn"><thead><tr><th align="left" id="d45256e222">

Option

</th><th align="left" id="d45256e225">

Description

</th></tr></thead><tbody><tr><td id="d45256e231">

**Add metrics**

</td><td>

1.  Select **+ Add metrics**.
2.  In the Add evaluation metrics panel, find or search for the metric that you want to add.
3.  Select the metric.
4.  Select **Done**.


</td></tr><tr><td id="d45256e261">

**Remove metrics**

</td><td>

1.  In the Included Agentic AI metrics table, find the metric that you want to remove.
2.  Select the remove icon.
3.  Select **Remove** to confirm.


</td></tr></tbody>
</table>
## Result

Evaluation scoring is active for ServiceNow AI systems. Scores appear on the monitoring Overview page as new sessions are evaluated.

## What to do next

To have an added metric contribute to your quality score, add it to a metric template and assign a weight. See [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-metric-templates.md).

To start evaluating a managed ServiceNow AI system, you must turn on evaluation at the asset level. See [Enable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-enable-evaluation.md).

**Parent Topic:**[Configuring monitoring and evaluations in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configuring-aict-evaluations.md)

