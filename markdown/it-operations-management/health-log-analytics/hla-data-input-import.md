---
title: Import a Health Log Analytics data input to a target instance
description: Import a data input configuration that you've exported from another instance as an update set.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [ServiceNow, Health Log Analytics, HLA, data input, source types, migration, configuration, update set, import, settings, mapping]
breadcrumb: [Migrating a data input configuration, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Import a Health Log Analytics data input to a target instance

Import a data input configuration that you've exported from another instance as an update set.

## Before you begin

For an overview of this feature, see [Migrating a Health Log Analytics data input configuration between instances](../concept/hla-data-input-migration.md).

Before performing this procedure, export the data input to an update set. For more information, see [Export a Health Log Analytics data input configuration](hla-data-input-migrate.md).

Role required: admin

## Procedure

1.  On the target instance, import the update set that contains the data input configuration.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  In the Related Links, select **Import Update Set from XML**.

    3.  Select **Choose file** and open the update set XML file from the Downloads folder.

    4.  Select **Upload**.

        The update set is uploaded to the instance and appears in the **Retrieved Update Sets** list in the Loaded state.

2.  Identify and address errors in the update set.

    1.  In the **Retrieved Update Sets** list, open the update set record.

    2.  Select **Preview Update Set Batch** to detect errors.

        The **Batch Update Set Preview** dialog indicates failure, which is expected behavior.

    3.  Close the dialog and resolve the errors in the **Update Set Preview Problems** related list.

        For more information, see [Preview a remote update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_PreviewARemoteUpdateSet.md).

        You can ignore errors that start with 'Could not find a record in \[table\]' for the following tables:

        -   aws\_credentials
        -   azure\_sas\_credentials
        -   azure\_service\_principal
        -   basic\_auth\_credentials
        -   cmdb\_ci\_service\_auto - Service instance
        -   ecc\_agent - MID
        -   ecc\_agent\_cluster - MID Server Cluster
        -   kafka\_ssl\_credentials
        -   sn\_occ\_data\_input\_preprocess\_example
        -   sn\_occ\_data\_input\_preprocess\_example\_row
        -   sn\_occ\_gcp\_credentials
        -   sn\_occ\_mapper\_example
        -   sn\_occ\_source\_type\_examples
        -   sn\_occ\_source\_type\_structure\_data
    4.  Select the errors that you ignored and then select the **Select All** check box.

    5.  From the **Actions on selected rows...** drop-down menu, choose **Accept remote update**.

    6.  In the **Preview Problems for Batch** related list, select all remaining errors and accept the remote update as explained in the earlier steps.

3.  When all errors in the update set have been resolved, select **Commit Update Set Batch**.

    The imported data input appears on the Data Inputs list. The import includes mapping settings and all other relevant configuration.

4.  In the imported data input, configure the following.

    -   The MID Server to which the logs stream.
    -   Credentials.

        **Note:** Whether you need to configure credentials depends on the data input that you've imported. For example, you must configure Amazon Web Services \(AWS\) credentials for Amazon CloudWatch and Amazon S3 data inputs.

    -   \(Optional\) The service instance to which to bind the log data.
    For more information, see the configuration documentation for the relevant data input: [Set up data inputs in Health Log Analytics manually](hla-data-input-setup-manual.md).


## Result

You can begin using the data input for streaming and processing log data.

**Parent Topic:**[Migrating a Health Log Analytics data input configuration between instances](../concept/hla-data-input-migration.md)

