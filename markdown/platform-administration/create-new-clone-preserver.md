---
title: Create a clone preserver
description: Create clone preservers to protect data on the target instance from being overwritten.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/create-new-clone-preserver.html
release: australia
topic_type: task
last_updated: "2026-03-12"
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

    The **Name** is a display label for your preserver. Use a descriptive name that identifies the table being preserved \(for example, "Firewall Devices CMDB", "incident Data", "User Preferences"\).

    Use the table's **system name** \(for example, "incident", "change\_request", "cmdb\_ci\_firewall\_device\_palo\_alto"\) to identify the table. Don't use the display label \(for example, "incident", "Change Request", "Firewall Device"\).

    **Note:**

    The data preserver must have a table selected or it can't be submitted.

    For tables with long system names \(more than 30 characters\), the system automatically uses a shortened **storage alias**. For example, the table `cmdb_ci_firewall_device_palo_alto` \(33 characters\) uses the storage alias `cmdb_ci_f6l_device_palo_alto` \(28 characters\). You can use either the original table name or the alias; the preserver will correctly preserve data from the aliased table. This is working as designed. See [Clone: Table name longer than 30 characters not preserved during instance clone \[KB1220478\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1220478) for more information.

6.  Select the **Table** to be preserved.

    From the table drop-down, select the table that you want to preserve. If the table has a long system name, it may display with both the original name and a shortened storage alias.

    **Note:**

    If the table system name exceeds 30 characters, you can use either the original table name or its storage alias. The system will preserve the correct table during the clone operation.

7.  Select the **Theme** check box if the data being preserved is a UI property.

8.  Define the data to be preserved using the **Condition builder**, and select **Save**.

    The success message displays.


