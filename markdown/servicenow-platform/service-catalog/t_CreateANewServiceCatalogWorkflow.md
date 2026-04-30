---
title: Create a catalog workflow
description: Create service catalog workflows when the default workflows are not appropriate for a fulfillment process.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Service catalog workflows, Service Catalog request fulfillment, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a catalog workflow

Create service catalog workflows when the default workflows are not appropriate for a fulfillment process.

## Before you begin

Role required: workflow\_creator, workflow\_admin, or admin

## About this task

This example describes the procedure to set up fulfillment for a laptop request.

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**

2.  Click **New Workflow**.

    ![Service catalog workflow form](../image/ServiceCatalogWorkflowForm.png "Service catalog workflow form")

3.  Complete the form with the following information.

<table id="table_wbf_1zt_dq"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

`Laptop Fulfillment`

</td></tr><tr><td>

Table

</td><td>

**Requested Item \[sc\_req\_item\]** Consider the following information:

 -   Workflows on the Service Catalog Requested Item \[sc\_req\_item\] table fulfill the request of a single catalog item. Each requested item triggers its own fulfillment workflow when the item is ordered. Use the Requested Item table to add workflows for requested items.

**Note:** To enable approval-type workflows to operate smoothly, make sure that the appropriate users have the correct role to access necessary tables in all domains.

-   Use caution when using **before query** business rules, as they can restrict access to the requested item record.
-   Workflows on the Request \[sc\_request\] table always run when a service catalog request is submitted, regardless of what item was ordered. These workflows control the entire request process, which can involve delivering several requested items.

Therefore, Request table workflows are not assigned to a specific item from the maintain item form. If you do use the Request table for service catalog requests, add conditions to the workflow to ensure it runs when the correct item is requested.

</td></tr><tr><td>

Expected time

</td><td>

**Days** `7`, **Hours** `00:00:00`. Workflows cannot calculate the end time because not all the activities within the workflow have defined times. Therefore, the **Expected time** on the workflow becomes the **Delivery Time** on the catalog request.**Note:** When both **Expected time** and **Schedule** are filled in, the catalog delivery time is then calculated based on the combination of both. For example, if you put 2 days as **Expected time**, it is calculated as 48 hours. If you then add a schedule that defines a work day as 8 hours, the delivery time becomes 48 / 8 = 6 days. If your schedule excludes weekends, the calculation also add 2 days for the weekend, making the delivery time 8 days.

</td></tr><tr><td>

Schedule

</td><td>

**8–5 weekdays**.

</td></tr><tr><td>

Timezone

</td><td>

**US/Pacific**. The timezone that the schedule applies to.

</td></tr><tr><td>

Description

</td><td>

`A workflow for the fulfillment of laptop requests.`

</td></tr></tbody>
</table>4.  Click **Submit**.

    ![Service catalog workflow form activities](../image/ServiceCatalogWorkflowFormActivities.png "Service catalog workflow form activities")


## What to do next

After initiating a workflow, add workflow activities to it. Workflow activities are listed on the **Core** tab in the right pane.

**Parent Topic:**[Service catalog workflows](../concept/c_ServiceCatalogWorkflowDefinition.md)

