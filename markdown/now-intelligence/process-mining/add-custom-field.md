---
title: Add custom fields to the audit table
description: The custom fields form as breakdown filters when viewing the process graph. Without custom fields, there won't be any breakdown filters.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with external datasets, Using Process Mining, Process Mining, Platform Analytics]
---

# Add custom fields to the audit table

The custom fields form as breakdown filters when viewing the process graph. Without custom fields, there won't be any breakdown filters.

## Before you begin

Role required: sn\_process\_optimization\_admin

## Procedure

1.  On the **Add additional fields** page, select **Add a custom field**.

    **Note:** You can add a maximum of 10 custom fields.

2.  Provide a name, and select the type.

    The type has the following options:

    -   **String**: For the size, the maximum length permitted is 4000 characters. The default value is 80.
    -   **Boolean**
    -   **Datetime**
    -   **Date**
    -   **Decimal**: For the size, the maximum length permitted is 20 characters. The default value is 15.
    -   **Integer**: For the size, the maximum length permitted is 20 characters. The default value is 15.
    -   **Reference**: If you select **Reference**, you must then select a reference table and a reference field. This will enable you to configure the source and target fields when doing a multi-dimensional mining using external dataset.
3.  Select **Next**.

    The next screen displays all the columns for the audit table that you’re creating.

4.  Select **Go back to add or remove additional details** if you want to change the custom fields.

    After making the change, select **Next**.

5.  After validating the list of columns, select **Create import table**.

    **Note:** This screen provides you with the name of the table that is created. You’ll need this table name in the next steps while importing data.

    ![Import external dataset](../image/ext-dataset3.png)

    The audit table is ready. You’re now set to import data into the table.


**Parent Topic:**[Working with external datasets](../concept/external-dataset.md)

