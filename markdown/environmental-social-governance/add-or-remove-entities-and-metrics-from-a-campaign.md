---
title: Add or remove entities and metrics from a campaign
description: Add or remove entities and metrics from a campaign to control which records are included in its data collection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/add-or-remove-entities-and-metrics-from-a-campaign.html
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [campaign entities, campaign metrics, campaign scope, add entities to campaign]
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Add or remove entities and metrics from a campaign

Add or remove entities and metrics from a campaign to control which records are included in its data collection.

## Before you begin

-   The campaign must exist. For more information, see [Create a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/create-a-campaign.md).
-   Role required: sn\_grc\_metric.manager

## About this task

Adding an entity to the campaign automatically adds metrics that match the campaign's group, frequency, and calendar. Removing an entity automatically removes its associated metrics from the campaign. This may take a few moments to complete.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace**.

2.  From the left panel, select the **List** icon.

3.  Select **Metrics** &gt; **Campaigns**.

4.  Open the campaign.

5.  Select **Entities** or **Metrics**.

    **Note:** To add a metric back after it's been removed this way, or to exclude a specific metric without removing its entity, use the **Metrics** tab directly.

6.  Add or remove records.

<table id="choicetable_add-remove-campaign-records"><thead><tr><th align="left" id="d40181e152">

Option

</th><th align="left" id="d40181e155">

Action

</th></tr></thead><tbody><tr><td id="d40181e161">

**Add**

</td><td>

Select **Add**, select the records, and select **Add**.

 **Note:** An entity already in another campaign with the same group, frequency, and calendar is not available to select again.

</td></tr><tr><td id="d40181e182">

**Remove**

</td><td>

Select the check box next to each record, and select **Remove**.

 **Note:** When a metric is removed from the campaign, or the campaign is deactivated, the metric's data owner and, in Simple approval mode, its approver revert to the values set on its metric definition.

</td></tr></tbody>
</table>
## Result

Data collection for the campaign includes only the entities and metrics currently added to it.

**Parent Topic:**[Configuring GRC: Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configuring-grc-metrics.md)

