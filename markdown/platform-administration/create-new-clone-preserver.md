---
title: Create a clone preserver
description: Create clone preservers to protect data on the target instance from being overwritten.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-30"
reading_time_minutes: 1
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a clone preserver

Create clone preservers to protect data on the target instance from being overwritten.

## Before you begin

Role required: clone\_admin

Preserving large amounts of data can significantly increase your clone duration. When creating a preserver use conditions to preserve only the data that you need.

The **Preservers** tab displays a list of all of your available data preservers. **Preservers** protect data on the target instance from being overwritten. If you have custom applications, you must also manually preserve your unpublished application content. To create a preserver, do the following.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Select **Definitions** from the secondary navigation bar.

3.  Select the **Preservers** tab.

4.  On the **Preservers** task page, select **New**.

5.  Enter the table label as the **Name** for your preserver.

    **Note:** The data preserver must have a table selected or it can't be submitted.

6.  Select the **Table** to be preserved.

7.  Select the **Theme** check box if the data being preserved is a UI property.

8.  Define the data to be preserved using the **Condition builder**, and select **Save**.

    The success message displays.


