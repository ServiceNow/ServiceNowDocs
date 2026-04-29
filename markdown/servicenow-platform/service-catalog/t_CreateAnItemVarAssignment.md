---
title: Create an item variable assignment
description: Create an item variable assignment that enables the catalog admin set up a default value mechanism in the order guide context so that the user can focus only on required values.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an order guide variable, Order guides, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an item variable assignment

Create an item variable assignment that enables the catalog admin set up a default value mechanism in the order guide context so that the user can focus only on required values.

## Before you begin

Role required: admin

## About this task

For example, you can set the default storage of an iPhone to 64 GB for Sales, and to 16 kB for Development. This setting is configured in the new hire order guide by using mutually exclusive rules and setting the storage variable accordingly for Sales and Development.

The value for an item variable is determined in the following order:

1.  Item variable assignment
2.  Cascading value \(if no item variable assignment exists\)
3.  Default value defined in the variable definition \(if no cascading value or item variable assignment exists\)

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Order Guides**.

2.  Open an order guide.

3.  Open a rule.

4.  In the **Item Variable Assignments** related list, click **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Item Variable|Name of the Item variable. Select an item variable from the list or create one.|
    |Active|Check box to make the record active.|
    |Assignment Type|Name of the assignment type. Select either Order Guide Variable or Value. When Order Guide Variable is selected, the **Order Guide Variable** field is enabled.|
    |Order Guide Variable|Name of the order guide variable. Select an order guide variable from the list or create one. \(This field is only visible if **Assignment Type** is Order Guide Variable.\)|

6.  Click **Submit**.


## What to do next

Set an item variable value to match an order guide variable value, or an order guide default value, using an item variable assignment.

**Parent Topic:**[Create an order guide variable](../concept/c_CreateVariables.md)

