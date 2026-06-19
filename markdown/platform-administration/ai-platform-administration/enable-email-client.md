---
title: Enable the email client for a table
description: Enable the email client for a table so that users can send emails directly from the table record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/enable-email-client.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable the email client for a table

Enable the email client for a table so that users can send emails directly from the table record.

## Before you begin

Role required: admin

## About this task

The email client is enabled by default on the Incident \[incident\] table. You can enable the email client for another table by adding the **email\_client** dictionary attribute to the table.

**Note:** This capability is not inherited by tables that extend the current table. For example, enabling the email client on the Task table does not enable it for the Incident or Problem tables.

## Procedure

1.  Open a record in the table that you want to enable the email client for.

    For example, to enable the email client for the Problem \[problem\] table, navigate to **Problem** &gt; **Open**, and then open any problem record.

2.  On the form, select the menu icon \(\[Omitted image "menu-icon.png"\] Alt text: Menu icon\) and then select **Configure** &gt; **Dictionary**.

3.  On the Dictionary Entries list, open the record of type **Collection**.

    The record does not have any entry for **Column name**.

4.  On the form, in the Related Links section, select **Advanced view**.

5.  In the **Attributes** field, enter `email_client=true`.

    If there are other values in the field, separate the attribute with a comma.

6.  Select **Update**.


**Parent Topic:**[Configure email client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/configuring-email-client.md)

