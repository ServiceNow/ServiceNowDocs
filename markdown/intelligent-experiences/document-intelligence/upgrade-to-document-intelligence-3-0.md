---
title: Upgrade to Document Intelligence 3.0 or later from version 2.4 or earlier
description: Document Intelligence 3.0 or later includes an updated database schema to support its transition from a scoped application to a ServiceNow AI Platform plugin.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Document Intelligence, Enable AI experiences]
---

# Upgrade to Document Intelligence 3.0 or later from version 2.4 or earlier

Document Intelligence 3.0 or later includes an updated database schema to support its transition from a scoped application to a ServiceNow AI Platform plugin.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Upgrade tasks

Review the information in this topic before you upgrade to Document Intelligence \(DocIntel\) 3.0 or later from version 2.4 or earlier.

For more information on installation, see [Install Document Intelligence](../task/install-document-intelligence.md).

## Before the upgrade

<table id="table_mnf_lpg_tsb"><thead><tr><th>

Pre-upgrade task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choose a time to schedule the upgrade

</td><td>

Avoid performing the upgrade during the run time of the nightly task definition \(use case\) upgrade job. Upgrading the application at that time would prevent use cases from upgrading until the run time of the next day.

</td></tr><tr><td>

Update any custom code that points directly to DocIntel database tables

</td><td>

After upgrading to Document Intelligence 3.0 or later from version 2.4 or earlier, DocIntel will use new flow actions. DocIntel will also use ServiceNow AI Platform database tables \(sys\_di\_\) in place of the scoped application tables \(di\_\). All DocIntel data will be migrated automatically to these platform tables.

 **Note:** Document extraction use cases may not be available for use until the migration is complete.

 If you have custom code in your instance that points directly to the scoped application tables \(di\_\), it should be updated, preferably to the platform component using DocIntel APIs.

 If you have custom code using DocIntel 2.4 or earlier flow actions, it should be updated to use 3.0 or later flow actions.

 For the list of tables, see [Components installed with Document Intelligence](installed-with-document-intelligence.md).

</td></tr><tr><td>

Add cross-scope records for integrations

</td><td>

For any integrations with Document Intelligence, add cross-scope records for the new DocIntel database tables.

 **Note:** Ensure that the existing cross-scope records for the old tables are not removed.

 See the Cross-scope records section for the list of records to be added.

 For more detail on cross-scope records, see [Cross-scope privilege record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_CrossScopePrivilegeRecord.md).

</td></tr></tbody>
</table>## During the upgrade

<table id="table_itb_bss_dyb"><thead><tr><th>

Upgrade task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Avoid using the Document Intelligence workspace to extract fields

</td><td>

Wait until a document task is migrated to the sys\_di\_task table before completing it using the Document Intelligence workspace. Completing a task during the upgrade may lead to data loss.

</td></tr></tbody>
</table>## After the upgrade

<table id="table_o1y_wrs_dyb"><thead><tr><th>

Post-upgrade task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test DocIntel integrations and custom workflows

</td><td>

Test your use case integrations to ensure they function with the new database schema.

</td></tr><tr><td>

Check for data loss

</td><td>

Some cases where you can lose data include:

 -   Any action resulting in the attachment deletion in an old di\_task record would result in a missing attachment for the new sys\_di\_task record.
-   Deletion of any new tasks created during the data migration \(that is, during or right after the 3.0 or later upgrade\) would result in permanent deletion as those records might not have entries in di\_task tables.
-   Deletion of an old “process\_task” flow \(or any action resulting in that flow deletion\) would result in an empty flow reference in the new integration setup records.

</td></tr><tr><td>

Post-upgrade migration of legacy use cases imported through update sets

</td><td>

At any time after the completion of the Document Intelligence 3.0 or later upgrade and data migration, you can rerun the migration batch script that ran during the upgrade.

 You may want to run this script if you must migrate any imported use cases requiring migration to the platform tables \(sys\_di\_\).

 1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.
2.  Open the **DocIntel migrate remaining data** scheduled job.
3.  Select the **Active** check box.
4.  Select **Execute Now**.

 **Warning:** Never use the **DocIntel migrate remaining data** batch job to rerun migration after deleting all records from sys\_di tables. You should only use it to migrate missing data from di\_ tables to sys\_di tables.

</td></tr></tbody>
</table>## Cross-scope records

|Source scope|Target scope|Target name|Operation|Target type|Status|
|------------|------------|-----------|---------|-----------|------|
|Scope of integrating BU|global|sys\_di\_task|Read|Table|Allowed|
|Scope of integrating BU|global|sys\_di\_key|Read|Table|Allowed|
|Scope of integrating BU|global|sys\_di\_key\_group|Read|Table|Allowed|
|Scope of integrating BU|global|sys\_di\_ocr\_input|Read|Table|Allowed|
|Scope of integrating BU|global|sys\_di\_pdf\_input|Read|Table|Allowed|
|Scope of integrating BU|global|sys\_di\_prediction\_input|Read|Table|Allowed|
|Scope of integrating BU|global|sys\_di\_training\_input|Read|Table|Allowed|
|Scope of integrating BU|global|sys\_di\_key\_hint|Read|Table|Allowed|

