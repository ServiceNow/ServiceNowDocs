---
title: Configure auditing using Audit Management Console
description: Use Audit Management Console module to experience a more enhanced way of defining and configuring the audit capability within your instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-03"
reading_time_minutes: 1
breadcrumb: [Configure, Auditing]
---

# Configure auditing using Audit Management Console

Use Audit Management Console module to experience a more enhanced way of defining and configuring the audit capability within your instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Audit Management Console**.

    A list of all tables in your instance shows up.

    **Note:** By default, the list of tables that has set Audit enabled shows up.

    You can select **Disabled** tab to see the list of tables that has set Audit disabled. You can also select the All tab to see all the tables in your instance with either enabled or disabled Audit option.

2.  Select the table from the list you want to update the auditing configurations.

    The table with its respective columns show up. You can also see the total number of columns in the selected table.

    **Note:** **Columns** and **Retention** are the tabs that show up on the table.

3.  Modify the Audit toggle depending on if you want to enable or disable audit for the selected table.

    **Note:** When Audit is enabled in a table, all the columns and fields within the table are enabled by default.

4.  Select **Edit Audit Status** if you don’t want all the columns to be enabled within an audit enabled table.

    The Select Columns to be Edited modal shows up.

5.  Unselect the columns that you don’t want to be enabled.

    You can also add any column by checking the column from the Available columns list.

6.  Select **Save** to save the latest modifications.

    Select **Clear All** to remove all the columns being enabled. See [Setup your audit retention](setup-audit-retention.md) for more information about audit data retention.


