---
title: Set encrypted field configurations
description: Configure which table columns or attachments that the system encrypts using a preconfigured cryptographic module.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Encrypting fields and attachments, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Set encrypted field configurations

Configure which table columns or attachments that the system encrypts using a preconfigured cryptographic module.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager and security\_admin or elevate role to security admin.

## About this task

Make sure you are in the correct application scope so you can see the tables in that scope.

Only users with access to the cryptographic module used in this configuration can read the data in the encrypted table column or access the attachment.

-   If a user has write access but not read access, the field displays in edit mode and the data entered displays as asterisks.
-   If a user has read access but not write access, the field displays the decrypted data in read-only mode.
-   If a user has all access, both read/write functionality is available on the encrypted field.

See [Create a cryptographic module](../../key-management-framework/task/create-cryptographic-module.md) or [Create cryptographic module for Column Level Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md) to begin.

**Important:**

After encrypting a column, any new data inserted into the column is encrypted automatically. However, data that existed in the column before the encryption was active is not automatically encrypted.

In order to encrypt data that existed before the column was encrypted, you must run a separate mass encryption job. Learn more about mass encryption in [Run mass encryption or decryption](mass-enc-dec.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations** &gt; **New**.

2.  Select **New**.

3.  Complete the form.

<table id="table_kfg_lzv_bkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

**Column** to encrypt a table column or **Attachment** to encrypt all of a table's attachments.

 Types of data encrypted are:

 -   String text \(Full UTF-8\)
-   Attachments
-   Date, Date/Time:

**Note:** You can create encrypted field configurations to encrypt existing Date and Date/Time fields. You can add a new encryption configuration to a parent table only. You can’t add a new encryption configuration to a child table.

-   URL
-   Column Level Encryption Enterprise also supports the following field types:
    -   HTML
    -   Journal
    -   Translated


</td></tr><tr><td>

Table

</td><td>

Table whose fields or attachments are to be encrypted.

</td></tr><tr><td>

Column

</td><td>

Column \(field\) to be encrypted if you selected **column** as the type.

</td></tr><tr><td>

Active

</td><td>

Select to mark the configuration active. Deselect if the configuration isn’t yet in use.

</td></tr><tr><td>

Crypto module

</td><td>

The cryptographic module that the encrypted field configuration applies to.

</td></tr><tr><td>

Method

</td><td>

Select **Single Module** to set the field configuration across one module. Select **Multiple Modules** for role-based access that spans across more than one cryptographic module.-   **Single Module**

Use this option to encrypt all attachments using a single module. Your users need access to this module, otherwise they aren't able to upload attachments.

-   **Multiple Modules**

Use this option to allow users to choose a module when uploading attachments. Users with access to at least one module can select a module to use for encryption. Users with no module access can upload unencrypted attachments.

</td></tr><tr><td>

Algorithm Encrypted Preserving\[read-only\]

</td><td>

Indicates if the crypto module that you selected is already configured to support non-deterministic encryption. This means that if the same data is encrypted more than once, the encryption is different each time.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Encrypting fields and attachments](../concept/field-encryption-key-management.md)

