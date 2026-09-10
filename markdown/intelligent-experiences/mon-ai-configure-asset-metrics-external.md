---
title: Configure asset-specific metrics for external AI systems
description: Add or remove metrics for one or more external AI systems without changing the global metric configuration, and adjust metric sample rates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-configure-asset-metrics-external.html
release: australia
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure evaluation scoring for external AI systems, Configure, Monitoring and evaluating AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Configure asset-specific metrics for external AI systems

Add or remove metrics for one or more external AI systems without changing the global metric configuration, and adjust metric sample rates.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

**Note:** The AI system must have evaluation enabled. See [Enable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-enable-evaluation.md).

## About this task

You can optionally override which metrics are evaluated for specific external AI systems. For details on adding or removing metrics for an AI system from that system's asset record instead, see [Configure metrics evaluated for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-ai-system-metrics.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  On the **AI evaluations** sub-tab, select **External AI systems**.

3.  Configure the metrics that you want to evaluate for specific AI systems.

<table id="choicetable_asset_metric_actions"><thead><tr><th align="left" id="d322728e132">

Option

</th><th align="left" id="d322728e135">

Steps

</th></tr></thead><tbody><tr><td id="d322728e141">

**Add one or more AI systems and selected metrics**

</td><td>

1.  In the Asset-specific metrics section, select **Add**.
2.  In the side panel, select one or more AI systems that you want to add a metric for.
3.  Select **Next**.
4.  Select one or more metrics that you want to evaluate for the AI systems that you selected.
5.  Select **Add metrics**.


</td></tr><tr><td id="d322728e177">

**Remove one or more metrics**

</td><td>

1.  In the Asset-specific metrics section, select the check box next to the metric or metrics that you want to remove.
2.  Select **Remove**.
3.  In the confirmation dialog, select **Remove**.


</td></tr></tbody>
</table>4.  Adjust the sample rate for one or more metrics.

    The sample rate determines what percentage of AI executions a metric evaluates. For external AI systems, each metric has its own sample rate, so you can evaluate the metrics that matter most on more executions and sample the rest to limit processing.

    **Note:** When metrics that contribute to the same quality or safety score use different sample rates, the metric with the higher rate evaluates more executions and can skew that score toward its results.

    1.  In the Asset-specific metrics section, select one or more AI systems that you want to update.

    2.  In the More actions menu, select **Edit sample rate**.

    3.  In the side panel, select the pencil icon for the metric that you want to update.

    4.  Enter the sample rate that you want to use.

    5.  Select **Apply**.

    6.  Update the sample rate for additional metrics in the side panel as needed.

    7.  Select **Save**.


**Parent Topic:**[Configure evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-external-ai-systems.md)

**Related topics**  


[Activate evaluation scoring for external AI systems]()

[Configure global metrics for external AI systems]()

[Exclude external AI systems from a metric]()

