---
title: Add preferred stockrooms to an assignment group
description: Set up preferred stockrooms for work groups so agents can search parts from their preferred stockrooms using the Now Mobile Agent application.
locale: en-US
release: australia
product: Asset Management for Field Service
classification: asset-management-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stockrooms, Inventory and asset management, Configure, Field Service Management]
---

# Add preferred stockrooms to an assignment group

Set up preferred stockrooms for work groups so agents can search parts from their preferred stockrooms using the Now Mobile Agent application.

## Before you begin

The Field Service Advanced Parts Sourcing plugin \(com.snc.fsm\_advanced\_parts\_sourcing\) must be activated. For more information, see [Additional plugins for Field Service Management](../reference/field-service-additional-plugins.md).

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Group Management** &gt; **Work Groups**.

2.  Open a work group for which you want to add preferred stockroom.

3.  In the Preferred Stockroom related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Assignment group|Assignment group to be linked with the preferred stockroom. Groups with the **wm\_work** type are listed.|
    |Stockroom|The preferred stockroom.|
    |Active|Option that sets the preferred stockroom.|
    |Order|Enter the order for the stockroom. The stockroom with lowest order is preferred and automatically sourced|
    |Conditions|Add conditions. For example, if model category is hardware, use the preferred stockroom.|
    |Type|Select the workflow to use the preferred stockroom. You can use the stockroom to source, dropoff, or for both operations.|

5.  Click **Submit**.

    The preferred stockroom is created for the selected assignment group.

6.  Select the **Preferred Stockroom** option in the **Part Search Criteria** property to help Field Service agents search parts from the preferred stockrooms using the Now Mobile Agent application.

    For more information, see [Advanced Part Sourcing components](../reference/advanced-part-souring-components.md)


**Related topics**  


[Setting up Field Service user groups](setting-up-field-service-user-groups.md#)

