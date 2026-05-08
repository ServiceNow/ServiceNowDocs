---
title: Troubleshoot import set performance
description: Review these performance issues to troubleshoot and improve the performance of your import set jobs.Running business rules during transform may cause the transform to take longer than expected, or cause the instance to slow down.Using multiple GlideRecord queries or large loops may slow down transform scripts.Repeatedly importing data that has not changed leads to many skipped rows.Coalescing on non-indexed fields with a large amount of data may cause transforms to slow down.Running imports simultaneously may cause excessive load on the database.Failing to clean import set tables may lead to those tables becoming cluttered and slow.Changing the table schema, such as by importing a new column locks the import set table.Importing a very large data set takes longer than importing multiple smaller data sets.Importing a high volume of data with many references to resolve might take longer than expected or cause the database to slow down.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Import sets, Imports, Workflow Data Fabric]
---

# Troubleshoot import set performance

Review these performance issues to troubleshoot and improve the performance of your import set jobs.

**Parent Topic:**[Import sets](../../import-sets/reference/import-sets-landing-page.md)

## Running business rules during transform

Running business rules during transform may cause the transform to take longer than expected, or cause the instance to slow down.

**Becomes an issue**: When importing a very large amount of data. For example, importing all data from an old system.

**Symptoms**:The transform takes much longer than expected. Also, the entire instance may be slow during that time.

**How to avoid this**: Do not run items like business rules, workflows, approval engines, and so on during a transform unless you want all insert and update business rules, notifications, and workflows to run. For example, when importing all data from an old system, you may not want notifications to run. To disable these items from running and to cease auditing and field normalization within the transform map for that import, deselect the **Run business rules** check box.

![](../image/TransformMapCheckbox.png "Transform Map Checkbox")

**Note:** Consider using an onComplete transform script to run business logic such as calculations at the end of an import rather than on each record as business rules do.

## Slow transform scripts

Using multiple GlideRecord queries or large loops may slow down transform scripts.

Becomes an issue: When the transform scripts are using multiple GlideRecord queries or looping through large collections of objects for each row. This issue may appear when the transform script is not efficient. In most cases, script goals can be accomplished using built-in functionality within the Import Set application. For example, you can script case-sensitive coalesce instead of writing scripts that use GlideRecord queries. GlideRecord queries typically slow down the import.

Symptoms: The transform takes much longer than would be expected. Depending on the script, the entire instance may be slow during that time.

How to avoid this: Use base system functionality whenever possible instead of writing custom scripts and if you do write scripts, avoid writing complicated scripts that use GlideRecord queries.

## Importing data that has not changed

Repeatedly importing data that has not changed leads to many skipped rows.

Becomes an issue: When you are importing data from a table that is very large and most of the records are not getting updated on a regular basis.

Symptoms: The import set takes longer than expected. Under **System Import Sets** &gt; **Progress**, expect to see an import with a Total count that is very high with a Skipped count that is also very high - this is found under the Message column. Indicating that most of the records imported had not actually changed. These records did not need to be imported.

How to avoid this: If you are running a JDBC import, use the last run datetime option in your import set [Data Source](../../import-sets/concept/c_DataSources.md). For a type of File import, be sure that whatever is generating your files is only adding data that is new, or has been changed.

## Coalescing on non-indexed fields

Coalescing on non-indexed fields with a large amount of data may cause transforms to slow down.

Becomes an issue: When matching on fields that are not indexed, this causes the transform stage of an import to run slowly. However, it only becomes an issue if there is a large enough amount of data. In extreme cases, this causes performance issues with the database due to added load.

Symptoms: Time spent in the transform stage of the import is large relative to the time taken to load the data. Expect to see high transform times.

How to avoid this: If possible, you should coalesce on a field that unique and already indexed. To determine if a field is already indexed, navigate to **System Definition** &gt; **Tables &amp; Columns** and find the table. In the list of columns for that table, an indexed column has a blue icon with an i next to it if indexed. For assistance indexing a field contact ServiceNow Technical Support.

## Running imports simultaneously

Running imports simultaneously may cause excessive load on the database.

Becomes an issue: When importing large amounts of data puts an additional load on the database. For example, importing 500,000 users and importing 200,000 configuration items at the same time. This can have a significant performance impact on all queries on the system due to the increased load on the database. This issue is especially severe when two imports are importing to the same table. In such a case, there is a possible contention issue for the table. Additionally, depending on which table is involved in processing, this can severely degrade performance of the import and the instance.

Symptoms: Multiple simultaneous imports running slowly combined with load on the database. You see large numbers of inserts and updates along; and if there is enough load or contention, high IO Wait times.

How to avoid this: Stagger your imports so they do not overlap.

## Large import set tables

Failing to clean import set tables may lead to those tables becoming cluttered and slow.

Becomes an issue: When the Import Set Deleter job is not running.

Symptoms: This is a size issue. If the import sets are not cleaned on a regular basis \(a cleanup is recommended after seven days worth of data\) the table fills causing imports to stop.

How to avoid this: Verify the Import Set Deleter job is running. If it is not currently running, contact Customer Service and Support as they will truncate all import set tables before enabling this job.

## Altering table schema during import

Changing the table schema, such as by importing a new column locks the import set table.

Becomes an issue: Any time a new column is imported, the entire import set table is locked during that schema change and depending on the size of the table, can take between five and ten minutes. During that time, no data can be selected or inserted. If that table is not used often, this may not cause any problems. However, if that table is frequently used, for example the LDAP import table, issues may arise.

Symptoms: The symptoms of this problem may vary. In our example of the LDAP import table, any transactions requiring a query of the LDAP import table will have to wait until the schema change has completed.

How to avoid this: Truncate the import table before importing with a new column.

## Importing very large data sets

Importing a very large data set takes longer than importing multiple smaller data sets.

Becomes an issue: When very large data sets are imported in a single job.

Symptoms: The import job takes a long time to complete.

How to avoid this: Break a very large data set into multiple, smaller jobs for faster results. Consider import sets under 100,000 records as a guideline. For example, importing 10 sets of 100,000 records completes faster than one import of 1 million records even though the total data imported is the same.

## Large data imports with many reference fields

Importing a high volume of data with many references to resolve might take longer than expected or cause the database to slow down.

Becomes an issue: When using a transform map for high-volume data imports with many reference fields.

Symptoms: The transform takes much longer than expected. While importing, the entire database slows down.

How to avoid this: Use secondary storage to look up references. Secondary storage uses a secondary database for reference resolution. It enables some read queries to be redirected to the secondary database, reducing the load on the primary database.

To enable secondary storage:

-   Activate the Secondary Database Pools \[com.glide.secondary\_db\_pools\] plugin. For more information, see Request a plugin.
-   Confirm that the import\_reference\_resoultion category in the Secondary Database Categories \[sys\_db\_category\] table has been configured and enabled. When you request the plugin, ServiceNow support configures this category for you.

After the plugin is activated and your secondary storage category has been configured and enabled, there will be a **Use Secondary Storage for References** check box on the form to [Create a transform map](../../../script/server-scripting/task/t_CreateATransformMap.md). Use this check box to enable or disable secondary storage.

When using secondary storage, set the **Choice action** field in the field map to **ignore** or **reject**. Setting the **Choice action** to **create** may cause multiple copies of a record to be created because the reference resolution doesn't detect newly created records immediately. For more information about choice actions, see [Create a field map](../../../script/server-scripting/task/t_CreatingAFieldMap.md).

A secondary database is always slightly out of date compared to the primary database. If your import requires completely up-to-date data, don't use secondary storage.

