---
title: Enable entities for Data Separation
description: Enable Data Separation on select entities as needed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Data Separation, Strategic Portfolio Management]
---

# Enable entities for Data Separation

Enable Data Separation on select entities as needed.

## Before you begin

Role required: sn\_ds.ds\_admin

## About this task

You can enable Data Separation on the following entities and related entities.

-   Entities:
    -   Demand \[dmn\_demand\]
    -   Project \[pm\_project\]
    -   Resource Plan \[resource\_plan\]
    -   Cost Plan \[cost\_plan\]
-   Related entities:
    -   Cost Plan Breakdown \[cost\_plan\_breakdown\]
    -   Project Task \[pm\_project\_task\]

## Procedure

1.  Navigate to **All** &gt; **Data Separation** &gt; **Supported Entities**.

    The list opens the entities supported for Data Separation.

2.  Open each Supported Entity record that you want to enable Data Separation for.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Entity|Name of the entity table.|
    |Enable data separation|Option to enable Data Separation for the entity.|

4.  Select **Update** to save the configuration.

5.  Navigate to **All** &gt; **Data Separation** &gt; **Supported Entities**.

6.  From the Supported Entities list view, select **Sync data separation** to synchronize the entity configuration for Data Separation.

    **Note:** The related Cost Plan Breakdown and Project Task entities can be enabled only if the Cost Plan and Project parent entities are enabled respectively.


## What to do next

Map a user group for Data Separation. For more information, see [Map a user group for Data Separation](map-groups-for-data-separation.md).

**Parent Topic:**[Configuring Data Separation](../concept/configuring-data-separation.md)

