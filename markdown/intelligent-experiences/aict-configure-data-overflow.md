---
title: Change the data overflow processing setting
description: Keep all ServiceNow Otto traffic in ServiceNow datacenters by opting out of data overflow processing, or opt back in to restore bursting to Microsoft Azure during traffic spikes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configure-data-overflow.html
release: australia
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring data controls, Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Change the data overflow processing setting

Keep all ServiceNow Otto traffic in ServiceNow datacenters by opting out of data overflow processing, or opt back in to restore bursting to Microsoft Azure during traffic spikes.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or admin

## About this task

Data overflow processing is active by default. Opting out keeps all traffic in ServiceNow datacenters but can cause processing delays or capacity overflow errors during high-traffic periods. You can opt back in at any time.

If multi-instance management is configured, change this setting on the production instance, because it's read-only on sub-prod instances.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **ServiceNow AI**.

2.  Select the **Data controls** tab.

3.  Change the data overflow processing setting for your situation.

<table><thead><tr><th align="left" id="d332834e116">

Scenario

</th><th align="left" id="d332834e119">

Steps

</th></tr></thead><tbody><tr><td id="d332834e125">

**Keep all traffic in ServiceNow datacenters**

</td><td>

1.  On the **Data overflow processing** card, select **Opt out**.
2.  In the confirmation dialog box, select **Opt out**.


</td></tr><tr><td id="d332834e155">

**Restore bursting to Microsoft Azure**

</td><td>

On the **Data overflow processing** card, select **Opt in**.

</td></tr></tbody>
</table>
## Result

The **Data overflow processing** card shows **Inactive** after you opt out, or **Active** after you opt back in.

**Parent Topic:**[Configuring data controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-data-controls.md)

