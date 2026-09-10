---
title: Create a data preserver \(legacy\)
description: Data preservers copy specified data to a target instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/t\_CreateADataPreserver.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create preservers, Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a data preserver \(legacy\)

Data preservers copy specified data to a target instance.

## Before you begin

Database views can't be preserved.

Role required: clone\_admin

## About this task

**Where to perform this task:** You must define data preservers on the **source instance** before initiating a clone. The preserved data is extracted from the source instance and restored on the target instance after the clone completes.

Data preservers retain system settings and themes, such as instance-specific authentication settings from the source instance. Don't use data preservers to transfer large sets of data, such as user groups. If you must preserve table data such as users, groups, and roles, consider exporting the records to a file and importing it after the clone is complete.

**Warning:**

If you attempt to create a preserver on the target instance instead of the source instance, the configuration will not work as intended. No data will be preserved during the clone. Always verify you are working on the source instance before proceeding with these steps.

## Procedure

1.  On the source instance, navigate to **Instance Clone** &gt; **Preserve Data**.

    **Tip:**

    Verify you are on the source instance \(the instance you are cloning FROM, not cloning TO\). You can confirm this by checking the instance name in the top-right corner or in the URL.

    You are now on the Preserve Data configuration page on the source instance.

2.  Select **New**.

3.  Enter a descriptive **Name** for the preserver.

    Use a descriptive name that identifies the table and its purpose. For example, use "User Preferences" for the `sys_user_preference` table or "Firewall Devices CMDB" for a custom table. This name helps you identify the preserver in the list. The data preserver must have a table name or it can't be submitted.

4.  Select the **Table** to be preserved.

    The data preserver must have a table selected or it can’t be submitted.

5.  Select the **Theme** check box if the data being preserved is a UI property.

6.  Define the data to be preserved using the [Condition Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).

    Use conditions to define records to preserve during a clone. For example, to preserve specific system properties, add conditions for each property name to preserve.

    **Note:** The condition to match regular expressions \[match regex\] isn't supported.

7.  Select **Submit**.

    If you want to delete the data preserver later, make sure not to modify or delete the following data preserver records:

    -   Core Instance Properties
    -   Semaphores
    -   Email Accounts

## Result

The data preserver is created on the source instance and will be applied to future clone operations. The preserved data will be retained and restored to the target instance after the clone completes.

## What to do next

After creating data preservers on the source instance, you can now request a clone. See [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md) for information on submitting a clone request. The configured preservers will be automatically applied based on your clone profile.

