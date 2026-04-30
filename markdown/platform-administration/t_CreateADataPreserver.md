---
title: Create a data preserver \(legacy\)
description: Data preservers copy specified data to a target instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-25"
reading_time_minutes: 1
breadcrumb: [Add preservers, Configure, Instance Clone, Configure core features, Administer]
---

# Create a data preserver \(legacy\)

Data preservers copy specified data to a target instance.

## Before you begin

Role required: clone\_admin

-   Database views can't be preserved.
-   If preservers aren't configured, a clone can't be requested.

## About this task

Data preservers retain system settings and themes, such as instance-specific authentication settings from the source instance. Don't use data preservers to transfer large sets of data, such as user groups. If you must preserve table data such as users, groups, and roles, consider exporting the records to a file and importing it after the clone is complete.

For information on how data preservers interact with exclusions see [Clarifying exclusions and preservers combinations](../concept/clone-exclusions-preservers-cleanupscripts.md#section_ahk_kxg_bgc).

## Procedure

1.  On the source instance, navigate to **Instance Clone** &gt; **Preserve Data**.

2.  Select **New**.

3.  Enter a **Name** for the preserver.

    For example, add the table label such as user preference for the `sys_user_preference` table. The data preserver must have a table name or it can’t be submitted.

4.  Select the **Table** to be preserved.

    The data preserver must have a table selected or it can’t be submitted.

5.  Select the **Theme** check box if the data being preserved is a UI property.

6.  Define the data to be preserved using the [Condition Builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    Use conditions to define records to preserve during a clone. For example, to preserve specific system properties, add conditions for each property name to preserve.

    **Note:** The condition to match regular expressions \[match regex\] isn't supported.

7.  Select **Submit**.

    If you want to delete the data preserver later, make sure not to modify or delete the following data preserver records:

    -   Core Instance Properties
    -   Semaphores
    -   Email Accounts

