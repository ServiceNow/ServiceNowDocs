---
title: Create a clone preserver
description: Create clone preservers to protect specific data on the target instance from being overwritten during a clone operation. Preservers allow you to retain existing target data while cloning source data for other tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/create-new-clone-preserver.html
release: australia
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 1
keywords: [clone preserver, data preserver, preserve data, clone conditions, target instance]
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a clone preserver

Create clone preservers to protect specific data on the target instance from being overwritten during a clone operation. Preservers allow you to retain existing target data while cloning source data for other tables.

## Before you begin

Role required: `clone_admin`

Preserving large amounts of data can significantly increase your clone duration. When creating a preserver, use conditions to preserve only the data that you need. See [General guidelines for excluding a table from cloning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-exclusions-guidelines.md) for optimization strategies.

**Tip:**

If you have custom applications, you must also manually preserve unpublished application content separately.

## About this task

The **Preservers** tab displays a list of all available data preservers. Each preserver defines a table and optional conditions that protect specified data on the target instance from being overwritten during a clone.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Select **Configuration** from the secondary navigation bar.

3.  On the **Preservers** page, select **New**.

4.  Enter a descriptive label in the **Name** field to identify this preserver.

    Use a descriptive name that clearly identifies the table and its purpose. For example: "Firewall Devices CMDB" or "User Preferences Data". This name appears in the Preservers list for easy identification.

    **Note:** The data preserver must have a table selected before it can be submitted.

5.  Select the **Table** to be preserved.

6.  Select the **Theme** check box if the data being preserved is a UI property.

7.  Define the data to be preserved using the **Condition builder**, and select **Save**.

    The preserver is created and saved. A success message confirms the creation.


## Result

The clone preserver is now active and will protect the specified data from being overwritten during any future clone operations that target this instance.

## What to do next

To view all active preservers, return to the **Preservers** tab. To use this preserver in a clone request, it will be automatically applied based on your clone profile configuration.

