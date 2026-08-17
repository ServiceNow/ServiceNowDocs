---
title: Enable campaigns
description: Enable campaigns to let data owners and approvers move groups of metrics through collection, review, and approval as a single unit, instead of one at a time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/enable-campaigns.html
release: australia
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [campaigns, enable campaigns, bulk actions, approval mode]
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Enable campaigns

Enable campaigns to let data owners and approvers move groups of metrics through collection, review, and approval as a single unit, instead of one at a time.

## Before you begin

-   When modifying system properties, if a message appears about the application scope, select **here** to be able to edit the record.
-   Role required: sn\_esg.admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Name** field, enter `sn_esg.metric_campaign`, and select it.

3.  In the **Value** field, enter `true`.

4.  Select **Update**.

5.  Enable bulk submission, approval, and rejection of campaign tasks.

    1.  In the Name field, enter `sn_esg.campaign_bulk_action_enabled`, and select it.

    2.  In the **Value** field, enter `true`.

    3.  Select **Update**.

6.  Set the approval mode for campaigns.

    1.  In the Name field, enter `sn_esg.metric_approval`, and select it.

    2.  In the Value field, enter `simple` or `advanced`.

    3.  Select **Update**.


**Parent Topic:**[Configuring GRC: Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configuring-grc-metrics.md)

