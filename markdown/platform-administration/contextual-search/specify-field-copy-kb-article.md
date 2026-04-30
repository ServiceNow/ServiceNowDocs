---
title: Specify field for attached Knowledge article links
description: Specify which field to add a note to when you attach a Knowledge article to a record.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Attach a Knowledge article, Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Specify field for attached Knowledge article links

Specify which field to add a note to when you attach a Knowledge article to a record.

## Before you begin

Role required: admin

## About this task

When you attach a Knowledge article to a record, by default a link to the Knowledge article is added to the **Additional comments \(Customer visible\)** field. You can specify the field for this link based on the table. For example, a Problem record doesn't have the **Additional comments \(Customer visible\)** field on the form, so the **Attach** action is configured to add the note to the **Work notes** field.

You can specify the field either globally or locally. The local field for a table overrides the global default field value.

To specify the global field, navigate to **Knowledge** &gt; **Administration** &gt; **Properties** &gt; **Other Knowledge Properties** and specify the name of the field in the **glide.knowman.attach.fields** property.

You can specify the local field using the following procedure.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  Open the table configuration that you want to change attachment fields for.

3.  Select the Search Action Configurations related list.

    ![Field where a link to the Knowledge article is embedded.](../image/polaris-ui-kb-attach-field.png)

4.  For each search action that you want to change the default field for, perform the following steps:

    1.  Open the search action.

    2.  Select the **Use custom field for attach note** option, if not already selected.

    3.  In the **Attach note field**, enter the name of the field that you want to copy the article information into, such as `comments` or `work_notes`.

        If field is not present on the form, Agent Assist will fallback on `comments` or `description` field depending on what is available.

    4.  Select **Update**.

    **Note:**

    -   If you don't want to add a note to any field, leave the **Attach note field** blank.
    -   If the field you have specified in the **Attach note field** isn't found on the form, then the note isn't added to any field.

## What to do next

Clear the system cache to make sure the changed field specification applies. You can clear the system cache by appending `cache.do` to the instance URL. For example, `https://<instance name>.service-now.com/cache.do`.

**Warning:**

Clearing the system cache can affect overall performance and degrade system response times. Don't run cache flushes during business hours, and don't trigger cache flushes automatically.

**Parent Topic:**[Attach a Knowledge article](t_AttachAnArticle.md)

