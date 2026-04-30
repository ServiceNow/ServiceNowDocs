---
title: Reindex a table without impacting text search results
description: Rebuild text search indexes without adversely impacting search results. You can continue to perform text searches on a table while the index regeneration takes place.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Regenerate a text index for a table, Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Reindex a table without impacting text search results

Rebuild text search indexes without adversely impacting search results. You can continue to perform text searches on a table while the index regeneration takes place.

## Before you begin

The table that you want to rebuild the index for must already be configured for indexing and searching. For details on this configuration process, see [Configure a table for indexing and searching](configure-single-table-for-indexing.md#).

Role required: admin

**Note:** If the **glide.script\_processor.admin** system property's value has been changed from the default value, you need the role specified by that property value. For details on this property value and its effects, see [Restrict access to background script \[Updated in Security Center 1.3 and 2.0\]](https://www.servicenow.com/docs/access?context=sc-restrict-access-to-background-script&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## About this task

This reindexing method doesn't purge the entire text search index before the rebuild takes place. It rebuilds the text search table index one record at a time, and reindexes the target table hierarchy only. For example, if you select the sc\_cat\_item table, only the sc\_cat\_item table is reindexed.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

    **Note:** If the **glide.script\_processor.admin** system property's value is set to security\_admin, you must elevate to that privileged role to access this module. For more information on elevating privileges, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

2.  In the **Run script \(JavaScript executed on server\)** text field, enter the following background script, being sure to enclose both arguments in quotes as shown:

    ```
    new GlideTextIndexEvent ( ).indexUpdate('TABLE_NAME', 'EMAIL_ADDRESS');
    ```

    Where:

    -   `TABLE_NAME` is the name of the table you want to reindex.

        **Note:** Only the specified table and its child tables are reindexed.

    -   `EMAIL_ADDRESS` is the address to which an email notification should be sent when the table reindex completes. Type `null` for no email notification.
    For example, to regenerate the kb\_knowledge table text search index, and specify that no email notification is required after the rebuild completes, create the following background script:

    ```
    new GlideTextIndexEvent ( ).indexUpdate('kb_knowledge', 'null');
    ```

    The script creates an event that the index handler processes, so the script completes without blocking on completion of the reindexing job.

3.  Select **Run script**.


## Result

The system reindexes the text search for the specified table. For large tables, such as sys\_metadata, reindexing can take a couple of hours, but you can still perform text searches on the table while the script is running.

**Parent Topic:**[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

