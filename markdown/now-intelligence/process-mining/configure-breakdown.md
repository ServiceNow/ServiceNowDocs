---
title: Configure a breakdown definition
description: Add a breakdown to filter records and analyze a process map by categories.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a project using Classic view, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure a breakdown definition

Add a breakdown to filter records and analyze a process map by categories.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

-   [Create a project or template using Project Builder](define-workflow-model.md)
-   [Configure multi-dimensional mining](configure-multidimensional-mining.md)

## About this task

**Note:** You can configure a maximum of 10 breakdown definitions for the parent table configuration and 5 breakdown definitions for any child table configuration. You cannot generate more than 5000 elements for any breakdown definition.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Mining Workspace** and select your project record.

2.  Identify which table you are configuring the breakdown definition, and open the associated table configuration record from the **Table Configurations** tab.

3.  In the **Breakdown Definitions** tab, open a new breakdown definition record by selecting **New**.

4.  On the Breakdown Definition form, fill in the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Field|Select the field on to use for the breakdown.|
    |Display Name|Name to display for this breakdown. If no name is entered, the breakdown displays the value of the **Field** field.|

5.  Select **Add Filter Condition** and further choose conditions for filtering the breakdown.

    **Note:** Filter conditions are only available when a reference field is selected in the **Field** field.

6.  Select **Submit**.


## What to do next

[Mine a project](generate-process-map.md#).

**Parent Topic:**[Create a project using Classic view](create-proj.md)

