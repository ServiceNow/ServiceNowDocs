---
title: Configure global metrics for ServiceNow AI systems
description: Choose which metrics to evaluate for ServiceNow AI systems and optionally adjust the shared sample rate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-configure-global-metrics-servicenow.html
release: zurich
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure evaluation scoring for ServiceNow AI systems, Configure, Monitoring and evaluating AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Configure global metrics for ServiceNow AI systems

Choose which metrics to evaluate for ServiceNow AI systems and optionally adjust the shared sample rate.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

After activating evaluation for ServiceNow AI systems, configure the global metrics that AI Control Tower evaluates for every ServiceNow AI system by default and how often they run.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  On the **AI evaluations** sub-tab, select **ServiceNow AI systems**.

3.  Review the quality metrics that are included by default.

    The following quality metrics are evaluated for ServiceNow AI systems by default.

    -   **Overall task completeness**

        Whether the agentic workflow completed its assigned task, including all required steps and proper resolution or escalation.

    -   **Tool calling correctness**

        Whether tool calls used correct parameters, formatting, and expected values.

    For a complete list of available metrics and their descriptions, see [Evaluation metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-evaluation-metrics-reference.md).

4.  In the Evaluation metrics for Agentic AI section, add or remove metrics that you want to evaluate.

    **Important:** Adding more metrics increases the visibility you gain into each session, but also increases assist usage to evaluate it. Select the metrics that give you the insight you need.

<table id="choicetable_add_remove_metrics_sn"><thead><tr><th align="left" id="d192414e180">

Option

</th><th align="left" id="d192414e183">

Description

</th></tr></thead><tbody><tr><td id="d192414e189">

**Add metrics**

</td><td>

1.  Select **+ Add metrics**.
2.  In the Add evaluation metrics panel, find or search for the metric that you want to add.
3.  Select the metric.
4.  Select **Done**.


</td></tr><tr><td id="d192414e219">

**Remove metrics**

</td><td>

1.  Find the metric that you want to remove.
2.  Select the remove icon.
3.  Select **Remove** to confirm.


</td></tr></tbody>
</table>5.  Update the sample rate.

    The sample rate determines what percentage of AI executions are evaluated. ServiceNow AI systems use a single sample rate for all metrics, unlike external AI systems, where each metric has its own rate. The default is 100%. You can enter a lower percentage to evaluate fewer executions.

    1.  Enter the sample rate to use when evaluating ServiceNow AI systems.

    2.  Select **Update**.


## What to do next

To have an added metric contribute to your quality score, add it to a metric template and assign a weight. See [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-metric-templates.md).

To tailor metrics for an individual ServiceNow AI system instead of changing the global configuration, see [Configure asset-specific metrics for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-asset-metrics-servicenow.md).

**Parent Topic:**[Configure evaluation scoring for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-servicenow-ai-systems.md)

**Related topics**  


[Activate evaluation scoring for ServiceNow AI systems]()

[Configure asset-specific metrics for ServiceNow AI systems]()

[Exclude ServiceNow AI systems from a metric]()

