---
title: Add multiple search fields for contextual search
description: Add multiple search fields if you want to search from a field other than the short description without using the related search box.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Add multiple search fields for contextual search

Add multiple search fields if you want to search from a field other than the short description without using the related search box.

## Before you begin

Role required: admin

## About this task

Search results for the default search field appear automatically when you open a record. You can configure contextual search to search for results even when there is no text in the default search field. Search results in other associated fields only appear when you have updated content in those fields.

As an example, in the base system the **Short description** field is the default search field for the Incident form, so search results based on the field are displayed automatically. If you configure **Description** as an additional search field, contextual search displays search results for **Description** when you open a record with an empty **Short description**.

**Warning:** Adding large fields can significantly affect contextual search performance. For best results, only add search fields that are restricted to 100 or fewer characters.

**Note:** Search results only appear for Search Fields that are visible on the form.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  Open the table configuration record for which you want to add multiple search fields.

3.  In the Search fields related list, click **New**.

4.  On the form, fill in the fields.

    ![Define a new search field on the Search Field form.](../image/multiple-search-fields.png "Search Field form")

<table id="table_pzx_c3q_dhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field

</td><td>

The search field to be added in the search fields list.**Note:** You can only select a text field.

</td></tr><tr><td>

Application

</td><td>

Application scope of the table configuration. The configuration is available for all applications or for scoped applications.

</td></tr><tr><td>

Order

</td><td>

Order in which the field appears in the search fields list. If there are multiple search fields, this field indicates which searched field is executed first.

</td></tr></tbody>
</table>5.  Click **Submit**.

    The new search field appears in the table configuration record's Search Fields related list.

    ![Search Fields related list showing two search fields.](../image/multiple-search-fields-2.png)


## What to do next

Use the **Default** column to set one search field as the default search field.

**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

