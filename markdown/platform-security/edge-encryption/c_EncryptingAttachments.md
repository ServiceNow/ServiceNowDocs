---
title: Encrypt attachments using standard encryption
description: You can encrypt attachments for specific tables.Select the tables whose attachments are to be encrypted and identify the encryption type.You can schedule a job to find and encrypt any unencrypted attachments for a specified table, using the default encryption key configured for the table.You can schedule a job to decrypt any encrypted attachments for a specified table, to store clear attachments in the instance.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Encrypt attachments using standard encryption

You can encrypt attachments for specific tables.

All attachments to a table use the same encryption type. Encrypted attachments are not searched when performing a text search. Only the standard encryption types are allowed for attachments. The order preserving or equality preserving encryption types are not allowed.

For a session bypassing the Edge Encryption proxy:

-   On a record with attachment encryption activated:
    -   The user can see that there are attachments and the attachment names.
    -   The user cannot add new attachments.
-   On a record without attachment encryption activated:
    -   The user can open and download existing attachments.
    -   The user can add new attachments.

For a session using the encryption proxy, the user can open and download existing attachments and add new attachments.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

## Configure attachment encryption

Select the tables whose attachments are to be encrypted and identify the encryption type.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Edge Encryption Configurations** &gt; **Create New**.

2.  Fill in the fields on the form, as appropriate.

<table id="table_nb5_jkf_4r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select a table whose attachments are to be encrypted.

</td></tr><tr><td>

Type

</td><td>

Whether to encrypt a table column or attachments for the table. Select **Attachment**.

</td></tr><tr><td>

Column

</td><td>

The table field to be encrypted.This field appears when the **Type** is **Column**, and not when **Type** is **Attachment**.

</td></tr><tr><td>

Encryption type

</td><td>

The encryption type to use. For attachments, only Standard AES128 and Standard AES256 are allowed.

</td></tr></tbody>
</table>3.  Click **Submit**.


### What to do next

After the encryption record has been added, you can create an attachment encryption job to encrypt existing attachments. If you do not run an attachment encryption job, the system encrypts new attachments when you attach them.

**Note:** If you mark the `edge_encryption_clear_attachment_allowed attribute` as **True** in the table's Collection Dictionary entry, unencrypted attachments are added to a table using Edge Encryption to encrypt attachments. If enabling this attribute, you should setup an 'Attachment Encryption Job so that any unencrypted attachments added will be encrypted.

## Schedule an attachment encryption job

You can schedule a job to find and encrypt any unencrypted attachments for a specified table, using the default encryption key configured for the table.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **Edge Encryption Configuration** &gt; **Encryption Configurations** &gt; **All**.

2.  Click the table you want to schedule an encryption job for.

3.  Under **Related Links**, click **Schedule Mass Encryption Job**.

    The **Scheduled Encryption Job** form is shown with all fields populated. The bottom of the form shows records for previous job executions.

4.  Fill in the fields on the form, as appropriate.

    |Field|Value|
    |-----|-----|
    |Name|Enter a descriptive name.|
    |Active|Clear this check box if you want to deactivate this job.|
    |Job Type|Select **Attachment Encryption**.|
    |Table|Select a table.|
    |Run|Select the period between job executions.|
    |Starting|Enter the date and time to run the job for the first time.|

5.  Click the menu icon in the form header and select **Save**.

6.  To see an estimated count of records to be updated, click **Estimate Record Count**.

7.  To run the job immediately, click **Execute Now**.


## Schedule an attachment decryption job

You can schedule a job to decrypt any encrypted attachments for a specified table, to store clear attachments in the instance.

### Before you begin

**Note:** You must mark the encryption record for the table as inactive \(clear the **Active** box\) before the decryption job runs, otherwise, nothing happens.

Role required: security\_admin

### Procedure

1.  Navigate to **Edge Encryption Configuration** &gt; **Encryption Configurations** &gt; **All**.

2.  Click the table with the attachments that you want to decrypt.

3.  Under **Related Links**, click **Schedule Mass Attachment Decryption Job**.

    The **Scheduled Encryption Job** form is shown with all fields populated. The bottom of the form shows records for previous job executions.

4.  Fill in the fields on the form, as appropriate.

    |Field|Value|
    |-----|-----|
    |Name|Enter a descriptive name.|
    |Job Type|Select **Attachment Decryption**.|
    |Active|Clear the check mark if you want to deactivate this job.|
    |Table|Select a table.|
    |Run|Select the period between job executions.|
    |Starting|Enter the date and time to run the job for the first time.|

5.  Click the menu icon in the form header and select **Save**.

6.  To see an estimated count of records to be updated, click **Estimate Record Count**.

7.  To run the job immediately, click **Execute Now**.


