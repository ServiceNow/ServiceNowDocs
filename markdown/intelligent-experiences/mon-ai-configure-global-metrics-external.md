---
title: Configure global metrics for external AI systems
description: Choose which metrics evaluate all your external AI systems by default, exclude an individual system from a specific metric, and adjust how often each metric runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-configure-global-metrics-external.html
release: australia
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure evaluation scoring for external AI systems, Configure, Monitoring and evaluating AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Configure global metrics for external AI systems

Choose which metrics evaluate all your external AI systems by default, exclude an individual system from a specific metric, and adjust how often each metric runs.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

Global metric configuration determines which metrics evaluate every external AI system by default and how often each one runs.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  On the **AI evaluations** sub-tab, select **External AI systems**.

3.  Review the quality and safety metrics that are included by default.

    The following quality and safety metrics are evaluated for external AI systems with a 5% sample rate by default.

    -   **Task completion**

        Whether the agent decision path and output satisfy the user's request.

    -   **Answer relevancy**

        Whether the response addresses the query and remains on topic.

    -   **Secrets detection**

        Whether the response contains leaked credentials, API keys, or other sensitive secrets.

    -   **Instruction adherence**

        How closely the response follows the given instructions.

    For a complete list of available metrics and their descriptions, see [Evaluation metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-evaluation-metrics-reference.md).

4.  In the Evaluation metrics for Agentic AI section, add or remove metrics that you want to evaluate.

    **Important:** Adding more metrics increases the visibility you gain into each session, but also increases the processing performed to evaluate it. Select the metrics that give you the insight you need.

<table id="choicetable_add_remove_metrics_ext"><thead><tr><th align="left" id="d71104e180">

Option

</th><th align="left" id="d71104e183">

Description

</th></tr></thead><tbody><tr><td id="d71104e189">

**Add metrics**

</td><td>

1.  Select **+ Add metrics**.
2.  In the Add evaluation metrics panel, find or search for the metric that you want to add.
3.  Select the metric.
4.  Select **Done**.


</td></tr><tr><td id="d71104e219">

**Remove metrics**

</td><td>

1.  Find the metric that you want to remove.
2.  Select the remove icon.
3.  Select **Remove** to confirm.


</td></tr></tbody>
</table>5.  Adjust the sample rate for one or more included metrics.

    The sample rate determines what percentage of AI executions a metric evaluates. For external AI systems, each metric has its own sample rate, so you can evaluate the metrics that matter most on more executions and sample the rest to limit processing.

    **Note:** When metrics that contribute to the same quality or safety score use different sample rates, the metric with the higher rate evaluates more executions and can skew that score toward its results.

    1.  In the Evaluation metrics for Agentic AI section, select the edit icon next to the sample rate that you want to update.

    2.  Enter the new sample rate.

    3.  Select **Apply**.


## What to do next

To have a metric contribute to your quality or safety scores, add it to a metric template and assign a weight. See [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-metric-templates.md).

To tailor metrics for an individual external AI system instead of changing the global configuration, see [Configure asset-specific metrics for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-asset-metrics-external.md).

**Parent Topic:**[Configure evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-external-ai-systems.md)

**Related topics**  


[Activate evaluation scoring for external AI systems]()

[Configure asset-specific metrics for external AI systems]()

[Exclude external AI systems from a metric]()

