---
title: Monitor capacity subscription calculations in Subscription Management
description: View how a capacity total is calculated to keep your subscription in compliance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Monitoring capacity subscriptions, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Monitor capacity subscription calculations in Subscription Management

View how a capacity total is calculated to keep your subscription in compliance.

## Before you begin

Role required: admin or usage\_admin

## Procedure

1.  Navigate to Subscription Management in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management** &gt; **Subscriptions**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **All Subscriptions**.
2.  In the list of all your product subscriptions, select a capacity subscription.

3.  On the subscription details page, preview the Capacity Definition record by selecting the record ID next to the **Capacity Definition** field.

4.  Depending on the definition type, review the following details to view how usage is calculated.

    |Type|Description|
    |----|-----------|
    |**Table query**|View the **Table Name**, **Query**, **Aggregation Type**, and **Aggregation Column**. View how the count is calculated by examining the SQL query.|
    |**Scripted definition**|View how usage is calculated by examining the contents of the **Script** field.|

5.  Select **Open Record** to view the full Capacity Definition record details.

6.  Select **Execute** to run the query or script immediately and view the latest results.

    **Note:** Executing a script or table query in a Capacity Definition record does not count toward the execution total that is monitored by the system.

    The total time required to execute and the latest count are displayed. The count from prior executions is displayed in the Previous Executions related list.

7.  If the capacity subscription is out of compliance, adjust the number of allocated resources or increase the capacity subscription.


**Parent Topic:**[Monitoring capacity subscriptions](../concept/monitoring-capacity-subscriptions.md)

