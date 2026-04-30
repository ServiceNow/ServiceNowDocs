---
title: Create a custom healthcare case type
description: Create a custom healthcare case type for EMR Help.
locale: en-US
release: xanadu
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure healthcare case types for EMR Help, Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create a custom healthcare case type

Create a custom healthcare case type for EMR Help.

## Before you begin

Role required: admin.

Set your scope to Healthcare and Life Sciences Service Management Core.

## About this task

Video showing how to create a custom healthcare case type.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Click **New**.

3.  Fill in the following fields:

    -   Label: The label for your healthcare case type. For example, EMR Case
    -   Name: The table name for your healthcare case type. For example, sn\_hcls\_emr\_case
    -   Extends table: Healthcare case
4.  In the Controls tab, set Auto-number to **true**.

5.  In the Application Access tab, fill in the fields as follows:

    -   Can read: True
    -   Can create: True
    -   Can update: True
    -   Can delete: True
    -   Allow configuration: True
6.  Right click in the header and select **Save** to save your updates.

7.  Click on the Additional Actions icon in the top left and click **Configure** &gt; **Dictionary**.

8.  In the Dictionary Entries list view, locate the dictionary entry for the caste type you created by entering as follows into the corresponding column search fields:

    1.  Table: sn\_hcls\_emr\_case
    2.  Type: collection
9.  Open sn\_hcls\_emr\_case.

10. Set **Audit** to true.

11. Click **Update**.


## Result

You now have a new case type extended from the abstract case type Healthcare case. For more information on the abstract Healthcare case type, see [Healthcare case table](../reference/hcls-case-table.md).

## What to do next

[Configure the record producer for your healthcare case type](configure-the-record-producer-for-your-hcls-case-type.md).

