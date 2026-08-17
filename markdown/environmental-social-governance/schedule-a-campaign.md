---
title: Schedule a campaign
description: Set the schedule for a campaign to control when data collection starts, when the next cycle begins, and when submissions are due.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/schedule-a-campaign.html
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [campaign schedule, first run date, next run date, due date offset]
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Schedule a campaign

Set the schedule for a campaign to control when data collection starts, when the next cycle begins, and when submissions are due.

## Before you begin

-   The campaign must exist. For more information, see [Create a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/create-a-campaign.md).
-   Role required: sn\_grc\_metric.manager

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace**.

2.  From the left panel, select the **List** icon.

3.  Select **Metrics** &gt; **Campaigns**.

4.  Open the campaign.

5.  Select **Details**.

6.  On the **Schedule** section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |First run date|Date the first data collection cycle begins. Set during campaign creation. Locks once the campaign is published.|
    |Due date offset|Number of days after the period end date when data submission is due.|
    |Next run date|Date the next data collection cycle begins. Editable; changing this affects when future cycles are generated.|
    |Additional comments|Optional comments about the campaign schedule.|

7.  Select **Save**.


## Result

Each campaign cycle generated for the campaign uses these schedule settings. Changes to **Due date offset** apply to cycles generated after the change.

**Parent Topic:**[Configuring GRC: Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configuring-grc-metrics.md)

