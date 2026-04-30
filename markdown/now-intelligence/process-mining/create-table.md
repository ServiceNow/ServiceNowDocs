---
title: Create an audit table
description: Create an audit table to store data. Audit table is a staging table that is created with the required columns to populate the external data.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with external datasets, Using Process Mining, Process Mining, Platform Analytics]
---

# Create an audit table

Create an audit table to store data. Audit table is a staging table that is created with the required columns to populate the external data.

## Before you begin

Role required: sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the External data integration icon \( ![External data integration icon](../image/ext-dataset-modules.png)\).

3.  Select **Create dataset**.

    The **Create an external dataset** tab opens.

4.  Provide a name for your dataset.

    ![Create a dataset](../image/ext-dataset1.png)

    **Note:** The dataset name must be unique. Ensure to have a user-friendly name that clarifies the type of data and the source for ease of use later.

5.  Select **Create dataset.**

    The next screen displays a list of columns for the audit table with their descriptions and examples.

6.  Select **Next**.

    ![List of columns for the audit table](../image/ext-dataset2.png)

    The next screen enables you to add custom columns for the table. If you need more columns than what is already provided, you can do it here.

    |Column title|Description|
    |------------|-----------|
    |Case ID|Refers to a unique identifier that is assigned to each record to distinguish between different records.|
    |Event value|Refers to an action or activity that occurs within a process, and captures information about what happened.|
    |Timestamp|Captures the date and time when an event occurred.|
    |User|\(Optional\) Refers to the person who performed the action.|
    |Event type|\(Optional\) Refers to the specific kind of activity that is being recorded in an event log. Event types are often used to group together similar types of events in a single column.|

7.  Select **Next**.


**Parent Topic:**[Working with external datasets](../concept/external-dataset.md)

