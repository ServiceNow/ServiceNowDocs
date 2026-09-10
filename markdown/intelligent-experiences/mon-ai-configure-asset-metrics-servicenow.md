---
title: Configure asset-specific metrics for ServiceNow AI systems
description: Add or remove metrics for one or more ServiceNow AI systems, without changing your organization's global metric configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-configure-asset-metrics-servicenow.html
release: australia
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure evaluation scoring for ServiceNow AI systems, Configure, Monitoring and evaluating AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Configure asset-specific metrics for ServiceNow AI systems

Add or remove metrics for one or more ServiceNow AI systems, without changing your organization's global metric configuration.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

**Note:** The AI system must have evaluation enabled. See [Enable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-enable-evaluation.md).

## About this task

You can optionally override which metrics are evaluated for specific ServiceNow AI systems. For details on adding or removing metrics for an AI system from that system's asset record instead, see [Configure metrics evaluated for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-ai-system-metrics.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  On the **AI evaluations** sub-tab, select **ServiceNow AI systems**.

3.  Configure the metrics that you want to evaluate for specific AI systems.

<table id="choicetable_asset_metric_actions"><thead><tr><th align="left" id="d270445e141">

Option

</th><th align="left" id="d270445e144">

Steps

</th></tr></thead><tbody><tr><td id="d270445e150">

**Add one or more AI systems and selected metrics**

</td><td>

1.  In the Asset-specific metrics section, select **Add**.
2.  In the side panel, select one or more AI systems that you want to add a metric for.
3.  Select **Next**.
4.  Select one or more metrics that you want to evaluate for the AI systems that you selected.
5.  Select **Add metrics**.


</td></tr><tr><td id="d270445e186">

**Remove one or more metrics**

</td><td>

1.  In the Asset-specific metrics section, select the check box next to the metric or metrics that you want to remove.
2.  Select **Remove**.
3.  In the confirmation dialog, select **Remove**.


</td></tr></tbody>
</table>
**Parent Topic:**[Configure evaluation scoring for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-servicenow-ai-systems.md)

**Related topics**  


[Activate evaluation scoring for ServiceNow AI systems]()

[Configure global metrics for ServiceNow AI systems]()

[Exclude ServiceNow AI systems from a metric]()

