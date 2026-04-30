---
title: Create a subflow using Template Integration Gateway
description: Use the Template Integration Gateway as a reference to create the supported subflows for Integration Gateway.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Enterprise Service Management Integrations Framework, Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Create a subflow using Template Integration Gateway

Use the Template Integration Gateway as a reference to create the supported subflows for Integration Gateway.

## Before you begin

Role required: flow\_designer, sn\_hr\_integr\_fw.admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  In **Subflows**, select Template Integration Gateway.

3.  Create a copy of subflow, and provide a suitable name for the flow, click **Copy**.

4.  Delete logs.

5.  Add the logic and assign flow outputs:

    |Field|Description|
    |-----|-----------|
    |Data|Result that is returned.|
    |Provider|Name of the provider.|
    |Status|Type of code number displayed when no results are returned. Code numbers vary based on scenario.|
    |Message|Message associated with status.|


## What to do next

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.
2.  In Subflows, select Integration Gateway.
3.  Create an entry for the above created subflow. For more information, see [Configure Integration Provider Mapping \(Decision table\)](configure-integration-mapping.md).
4.  Click **Test**.

    1.  In Test Subflow, select User, Feature Name, Service Name, and Payload.
    2.  Click **Run Test**.
    Verify if the outputs or results generated are correct. Validate if the correct subflow has been run.


