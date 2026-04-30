---
title: Configure alert rules
description: Configure an alert rule in the Crisis map so that you can define when a feed is displayed as an alert on the dashboard. You can also specify the conditions under which an alert is no longer valid and dismiss it from the dashboard.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup for Crisis map, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure alert rules

Configure an alert rule in the Crisis map so that you can define when a feed is displayed as an alert on the dashboard. You can also specify the conditions under which an alert is no longer valid and dismiss it from the dashboard.

## Before you begin

Role required: sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Threat and Alert Data Feeds** &gt; **Administration** &gt; **Alert Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information on the Alert Rules form, see [Alert Rules form](../reference/alert-rules-form.md).

4.  Add the name, description, order, and category for the alert rule.

5.  In the **Create Condition** tab, define the conditions for the alert rule.

    You can create conditions to address impacted resources or optimize specific impact areas.

    The example shows an alert rule for a specific category and severity.

    ![Category and severity.](../image/alert-rule-example.png)

6.  In the **Dismiss Condition** tab, define the conditions for the alert rule.

    You can dismiss conditions when a feed is deleted or resources are not impacted. The example shows how to dismiss a condition in an alert rule.

    ![Dismiss a condition.](../image/alert-rule-dismiss.png)

7.  Select **Submit**.


## Result

The alert rule is displayed in the **Alert Rules** record page.

-   **[Alert Rules form](../reference/alert-rules-form.md)**  
Use the Alert Rules form in BCM UIB Workspace to add details about the alert rules.

**Parent Topic:**[Setup for Crisis map](../concept/crisis-map-admin-tasks.md)

