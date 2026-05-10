---
title: Index attachments on a table
description: You can enable attachment indexing for a table so text searches can return matches from the record and its file attachments.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Attachments, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Index attachments on a table

You can enable attachment indexing for a table so text searches can return matches from the record and its file attachments.

## Before you begin

Role required: admin

## About this task

By default, attachment indexing is enabled for the Knowledge Base. You can enable attachment indexing for other tables. Enabling attachment indexing causes the platform to reindex the selected table, its parent table, and any children of the parent table. For large tables, such as the Task table, reindexing can take several hours and slows down the system until complete. Reindexing is best performed during non-peak times.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations**.

2.  Edit the record for the table that you want to enable attachment indexing for.

3.  In the Text Index Table Attribute Maps related list, select **New**.

4.  On the Text Index Table Attribute Map form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Table|&lt;table name&gt;|
    |Attribute name|Attachment index|
    |Value|true|

    **Note:** The attachment index attribute only applies to the tables on which you explicitly add it. It does not cascade to child tables. For example, enabling indexing of attachments on the Task table does not enable indexing of attachments on the Incident table. Not all file types are supported for attachment indexing. For a list of supported file types, see [Zing can include attachments in search results](../../search-administration/concept/c_SearchingForAttachments.md).

5.  Select **Submit**.

    A message appears indicating that the attachment index attribute change will not take effect until you reindex the selected table.

6.  Dismiss the reindexing message by selecting **OK**.

7.  On the Text Index Configuration form, select the **Generate Text Index** related link.

8.  In the confirmation window, perform one of these two steps:

    -   To receive an email notification from the system when text indexing for the table is complete, enter your email address and select **OK**.
    -   If you do not want to receive an email notification, select **Do not notify me**, then select **OK**.
    ![Confirmation window for Generate Text Index action.](../image/generate-text-index.png)

9.  Dismiss the confirmation message by selecting **OK**.


## Result

The system begins text indexing for the table. When it is complete, attachments can be searched on that table.

**Parent Topic:**[Administering attachments](../reference/r_AdministeringAttachments.md)

**Parent Topic:**[Zing can include attachments in search results](../../search-administration/concept/c_SearchingForAttachments.md)

