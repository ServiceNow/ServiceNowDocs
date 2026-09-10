---
title: Configure metrics evaluated for an AI system
description: Add or remove metrics for a specific AI system to tailor evaluation coverage without changing your organization's global metric configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-configure-ai-system-metrics.html
release: zurich
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Monitoring an AI system, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Configure metrics evaluated for an AI system

Add or remove metrics for a specific AI system to tailor evaluation coverage without changing your organization's global metric configuration.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can configure metrics only for AI systems they manage.

## About this task

The metrics evaluated for an AI system come from your organization's global metric configuration by default. However, you might apply specific metrics for individual AI systems. For example, to check a customer-facing agent for profanity when profanity isn't part of your global safety configuration, you can add or remove the metric for that system specifically. Changes made here don't affect any other AI system or your global configuration.

## Procedure

1.  Navigate to the **Monitor** tab for the AI system that you want to configure in one of the following ways:

    -   Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory**. Select the AI system asset and then select the **Monitor** tab.
    -   Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor** and select a system name in the **AI systems ranked by score** widget.
    -   Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor** &gt; **Evaluated sessions** and select the AI system name in the **AI system** column.
2.  Configure which metrics to score for this asset.

<table id="choicetable_configure_metrics"><thead><tr><th align="left" id="d243676e160">

Scenario

</th><th align="left" id="d243676e163">

Steps

</th></tr></thead><tbody><tr><td id="d243676e169">

**Configuring for the first time**

</td><td>

1.  In the **Metrics evaluated** card, select **Setup asset specific metrics**.
2.  Find a specific metric using the search box or the **All**, **Quality**, and **Safety** tabs.
3.  Select the check box next to each metric that you want to evaluate for this AI system.


</td></tr><tr><td id="d243676e205">

**Modifying an existing configuration**

</td><td>

1.  In the **Metrics evaluated** card, select the settings icon.
2.  Find a specific metric using the search box or the **All**, **Quality**, and **Safety** tabs.
3.  Select or clear check boxes to add or remove metrics.


</td></tr></tbody>
</table>3.  Select **Save metric**.

    A confirmation message appears summarizing the change, and the **Metrics evaluated** card updates to reflect it. If a metric you're removing is currently used in a published evaluation template or a compliance evaluation, the change isn't saved, and you're shown which templates or evaluations are using it so you can resolve that first.


## What to do next

To change how often a metric is evaluated for this AI system, an AI steward can adjust the sample rate from the evaluation settings. See [Configure global metrics for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-global-metrics-servicenow.md) or [Configure global metrics for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-global-metrics-external.md), depending on the AI system type.

**Parent Topic:**[Monitoring an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-asset-monitor.md)

