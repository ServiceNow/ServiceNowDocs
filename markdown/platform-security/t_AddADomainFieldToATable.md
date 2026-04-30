---
title: Add a domain field to a table
description: As an administrator, domain-separate a custom table by adding a sys\_domain field to it.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# Add a domain field to a table

As an administrator, domain-separate a custom table by adding a sys\_domain field to it.

## Before you begin

Role required: admin

## About this task

**Note:**

Do not add domains to base system tables.

## Procedure

1.  Navigate to the table's list view.

    For example, type &lt;table name&gt;`.list` in the navigation filter.

2.  Right-click the list header and select **Configure** &gt; **List Layout**.

3.  In the **Create new field** section, enter `sys_domain` as the **Name** and `Domain ID` as the **Type**.

4.  Click **Add**.

5.  Click **Save**.

    **Note:**

    Any other means of creating a field adds a **u\_** prefix to the column name. But with the domain field, the system automatically creates the field without the **u\_** prefix. You can use the following functionality as a shortcut: Whenever you create a **sys\_domain** field, name it **sys\_domain** and leave the field type as is. The system automatically sets the field type to **Domain ID** and the field label to **Domain**, saving you a few clicks.

    Adding domains to base system tables requires prohibitively thorough testing, updates and adding new logic. In addition in many cases, the source code is not accessible to the customer.


