---
title: Export a Health Log Analytics data input configuration
description: Export the configuration of a Health Log Analytics data input with or without the related source types to an update set. You can then import the update set to the target environment.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, data input, source types, migration, configuration, update set, export, settings, mapping]
breadcrumb: [Migrating a data input configuration, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Export a Health Log Analytics data input configuration

Export the configuration of a Health Log Analytics data input with or without the related source types to an update set. You can then import the update set to the target environment.

## Before you begin

For an overview of this feature, see [Migrating a Health Log Analytics data input configuration between instances](../concept/hla-data-input-migration.md).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  In the Data Inputs list, select the data input that you want to export.

3.  Export the data input to an update set.

    **Note:** The exported configuration doesn't include the service instance configured for the data input.

    1.  From the **Actions on selected rows** drop-down menu, choose **Export Data Input**.

        ![Export Data Input option on the Actions on selected rows drop-down menu.](../image/hla-export-data-input1.png)

    2.  In the **Export Data Input** dialog, do one of the following:

        ![Export Data Input dialog.](../image/hla-export-data-input2.png)

        -   Leave the check box selected to include the source types that are associated with the data input in the update set.

            When the box is selected, the update set will include the following source type-related tables:

            -   sn\_occ\_source\_type
            -   sn\_occ\_source\_type\_structure
            -   sn\_occ\_sources
            -   sn\_occ\_timestamp\_formats
            -   sn\_occ\_lexical\_keywords
            -   sn\_occ\_log\_correlator
            -   sn\_occ\_log\_source\_retention
            -   sn\_occ\_quick\_replacements
            -   sn\_occ\_reconstructors
            -   sn\_occ\_replacements
        -   Clear the box to export the data input without the associated source types. For example, if you want to reuse the data input configuration, but configure the source types from scratch.

            When the box is clear, the update set will not include the source type-related tables.

        **Note:** You can export source types separately. For more information, see [Export source types to an update set in Health Log Analytics](hla-source-types-migrate.md).

    3.  Select **Continue**.

    The data input, with or without the source types, is exported to an update set.

    **Note:** An update set can act as the parent for multiple child update sets.

4.  Select **Download update set** to download the update set to the instance.

    The update set is downloaded as an XML file.


## What to do next

Import the update set to the required ServiceNow instance. For more information, see [Import a Health Log Analytics data input to a target instance](hla-data-input-import.md).

**Parent Topic:**[Migrating a Health Log Analytics data input configuration between instances](../concept/hla-data-input-migration.md)

