---
title: Import source types to a target instance
description: Import source types that you've exported separate from the Health Log Analytics data input configuration.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, source types, migration, data input configuration, update set, import]
breadcrumb: [Migrating Health Log Analytics data input configurations between instances, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Import source types to a target instance

Import source types that you've exported separate from the Health Log Analytics data input configuration.

## Before you begin

For an overview of this feature, see [Migrating Health Log Analytics data input configurations between instances](../concept/hla-data-input-migration.md).

Before performing this procedure, export the source types to an update set. For more information, see [Export source types to an update set](hla-source-types-migrate.md).

Role required: admin

## Procedure

1.  On the target instance, import the update set that contains the source types.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  In the Related Links, select **Import Update Set from XML**.

    3.  Select **Choose file** and open the update set XML file from the Downloads folder.

    4.  Select **Upload**.

        The update set is uploaded to the instance and appears in the **Retrieved Update Sets** list in the Loaded state.

2.  Identify and address any errors in the update set.

    1.  In the **Retrieved Update Sets** list, open the update set record.

    2.  Select **Preview Update Set Batch** to detect errors in the update set.

        The **Batch Update Set Preview** dialog indicates failure, which is expected behavior.

    3.  Close the dialog and resolve the errors in the **Update Set Preview Problems** related list.

        You can ignore errors that start with 'Could not find a record in \[table\]' for the following tables:

    4.  Select the errors that you ignored and then select the **Select All** check box.

    5.  From the **Actions on selected rows...** drop-down menu, choose **Accept remote update**.

    6.  In the **Preview Problems for Batch** related list, select all remaining errors and accept the remote update as explained in the earlier steps.

3.  When all errors in the update set have been resolved, select **Commit Update Set Batch**.


## Result

The imported source types appear in the Source Types list.

**Parent Topic:**[Migrating Health Log Analytics data input configurations between instances](../concept/hla-data-input-migration.md)

