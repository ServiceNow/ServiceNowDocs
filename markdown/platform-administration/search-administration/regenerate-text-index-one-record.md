---
title: Regenerate the text index for a single record
description: Update the text search index for a single record. Use this approach to quickly verify whether text indexing is the cause of a search issue without rebuilding the full text index for an entire table.
locale: en-US
release: zurich
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Regenerate a text index for a table, Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer]
---

# Regenerate the text index for a single record

Update the text search index for a single record. Use this approach to quickly verify whether text indexing is the cause of a search issue without rebuilding the full text index for an entire table.

## Before you begin

Identify the following:

-   A search term that doesn't return the expected results
-   A record containing the identified search term that isn't returned when searching for the term
-   The table that includes the identified record

The identified table must already be configured for indexing and searching. For details on this configuration process, see [Configure a table for indexing and searching](configure-single-table-for-indexing.md#).

Role required: admin

**Note:** If the **glide.script\_processor.admin** system property's value has been changed from the default value, you need the role specified by that property value. For details on this property value and its effects, see [Restrict access to background script \[Updated in Security Center 1.3 and 2.0\]](https://www.servicenow.com/docs/access?context=sc-restrict-access-to-background-script&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## About this task

This reindexing method rebuilds the text search index for a single record. It takes less time than rebuilding the text index for all records in a table.

You can use this method to quickly determine whether text indexing is the cause of a search issue. Doing so avoids the delay associated with rebuilding the entire table's text search index.

## Procedure

1.  Copy the sys\_id for the identified record by selecting **Copy sys\_id** from its context menu.

2.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

    **Note:** If the **glide.script\_processor.admin** system property's value is set to security\_admin, you must elevate to that privileged role to access this module. For more information on elevating privileges, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

3.  In the **Run script \(JavaScript executed on server\)** text field, enter the following script, replacing `TABLE_NAME` with the name of the table containing the identified record and `SYS_ID` with the record's sys\_id that you copied in step [1](regenerate-text-index-one-record.md#copy-sys-id-step):

    ```
    var gr = new GlideRecord('TABLE_NAME');
    gr.get('SYS_ID');
    gs.eventQueue("text_index", gr, '[TABLE_NAME]','update','text_index');
    ```

4.  Select **Run script**.

    The script creates a text\_index update event for the specified table in the text\_index queue.

5.  Navigate to **All** &gt; **System Policy** &gt; **Events** &gt; **Event Log** and wait for the new text\_index update event's state to change to **processed**.

    To find the new event, you can apply a **\[Name\]\[contains\]\[text\_index\]** filter and sort the Event list view by **Created** date/time in descending \(z to a\) order.


## Result

The system updates the text index for the specified record in the specified table.

## What to do next

Repeat your sample search. If this search returns the identified record, you may want to update the text index for the entire table that contains that record. For details, see [Regenerate a text index for a table](t_RegenerateATextIndexForATable.md).

**Parent Topic:**[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

