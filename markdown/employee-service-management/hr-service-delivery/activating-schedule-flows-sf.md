---
title: Activating schedule flows
description: Activate the schedule flow that interacts with SuccessFactors to pull worker profile information and tasks into a ServiceNow application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery Integration with SuccessFactors, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Activating schedule flows

Activate the schedule flow that interacts with SuccessFactors to pull worker profile information and tasks into a ServiceNow application.

## Before you begin

Role required: sn\_hr\_sf.admin

## Procedure

1.  Navigate to **Flow Designer** &gt; **Designer**.

2.  Open **Run Trigger SAP SuccessFactors Integrations**.

3.  In the **Trigger** field, specify the time and interval at which you want to automatically run the scheduled flow.

4.  Click **Activate**.

5.  Expand **Call Run SuccessFactors Service Subflow**.

    Once data is pulled into staging tables, transform maps moves data into target tables. For more details, refer to [Use transform maps](../reference/transform-maps-w.md).

    **Note:**

    -   For a partial pull, deselect the **Retrieve all data** check box. Partial pull is not supported for Department and Location. It is only supported for HR profile and Job Profile.
    -   The **Retrieve All Data** check box is not supported for Pull To-Dos. The first pull will always be a full pull based on the configuration parameter **Initial Load Date time**. The subsequent ones are incremental pulls.
    -   Before you run the flow, turn off reporting: **com.snc.process\_flow.reporting.level**.

