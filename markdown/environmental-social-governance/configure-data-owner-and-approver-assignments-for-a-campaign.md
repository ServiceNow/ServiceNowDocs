---
title: Configure data owner and approver assignments for a campaign
description: Assign a data owner and one or more levels of approvers to a campaign, so the right users receive metric data tasks and approve them in sequence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/configure-data-owner-and-approver-assignments-for-a-campaign.html
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [data owner, approvers, approval levels, campaign owners]
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Configure data owner and approver assignments for a campaign

Assign a data owner and one or more levels of approvers to a campaign, so the right users receive metric data tasks and approve them in sequence.

## Before you begin

-   The campaign must exist. For more information, see [Create a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/create-a-campaign.md).
-   Role required: sn\_grc\_metric.manager

## About this task

The approval levels you configure apply regardless of the campaign's approval mode, up to 10 levels. When the approval mode is set to Advanced, submitting a metric data task also generates records in the GRC: Approver Configurator application. Use Approver Configurator for more complex approval rules, according to per-rule anyone-or-all logic, which isn't available when adding approvers on this page.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace**.

2.  From the left panel, select the **List** icon.

3.  Select **Metrics** &gt; **Campaigns**.

4.  Open the campaign.

5.  Select **Owners**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Owner type|Type of data owner assigned to the campaign.|
    |Data owner|User or group that receives all metric data tasks for the campaign.|

7.  Select **Save**.

8.  Select **Approvers**.

    **Note:** For more information, select **Approver configuration** from the **Approvers** tab.

9.  In the **Users** or **User groups** field for **Level 1**, select one or more approvers.

10. Add another approval level.

    Select **Add level**, and select approvers for that level.

11. Sync the approvers with a matching approver configuration.

    Select **Sync from approver configuration**.

12. If the campaign is already published, confirm the change when prompted.

13. Select **Confirm approvers**.


## Result

The data owner receives all metric data tasks for the campaign. Approvers approve each level in sequence before the campaign cycle can move to the next stage.

**Parent Topic:**[Configuring GRC: Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configuring-grc-metrics.md)

