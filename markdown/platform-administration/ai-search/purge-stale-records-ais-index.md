---
title: Purge stale records from the AI Search index
description: Execute a scheduled job to delete stale records from the AI Search index.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indexed source retention policies and filter conditions, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Purge stale records from the AI Search index

Execute a scheduled job to delete stale records from the AI Search index.

## Before you begin

Role required: admin

**Note:** If the **glide.script\_processor.admin** system property's value has been changed from the default value, you need the role specified by that property value. For details on this property value and its effects, see Restrict access to background script.

## About this task

If either of these conditions is satisfied for a record in the AI Search index, AI Search marks the record as stale.

-   The time since the record's last update exceeds the age limit from its indexed source's retention policy
-   The record no longer satisfies the filter conditions defined for its indexed source

AI Search automatically purges stale records from the index daily. Administrators can purge records manually by running a background script.

For more information on running background scripts, see Scripts - Background module.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

    **Note:** If the **glide.script\_processor.admin** system property's value is set to security\_admin, you must elevate to that privileged role to access this module. For more information on elevating privileges, see Elevated privilege roles.

2.  In the **Run script \(JavaScript executed on server\)** text field, enter one of the following background scripts.

    -   To purge stale records indexed from a specific table, enter this script, replacing `TABLE_NAME` with the name of your chosen table:

        ```
        new sn_ais.IndexEvent().purgeFilteredDocuments('TABLE_NAME');
        ```

        For example, to purge all stale records indexed from the Knowledge Table indexed source, replace `TABLE_NAME` with `kb_knowledge` in the script.

    -   To purge all stale records in the index, regardless of which table they were indexed from, enter this script:

        ```
        new sn_ais.IndexEvent().purgeFilteredDocuments();
        ```

3.  Select **Run script**.

    The script creates an event that the index handler processes, so the script completes without blocking on completion of the purge job.


## Result

The background script executes, deleting stale records from the AI Search index.

**Parent Topic:**[Indexed source retention policies and filter conditions](../concept/retention-policies-conditions-ais.md)

