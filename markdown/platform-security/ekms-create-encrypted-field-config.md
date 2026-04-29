---
title: Create Encrypted Field Configurations
description: Configure specific fields to be encrypted using your External Key Management Service \(EKMS\) cryptographic module with external Amazon Web Services Key Management System \(AWS KMS\) key wrapping.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 3
breadcrumb: [Configuring External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Create Encrypted Field Configurations

Configure specific fields to be encrypted using your External Key Management Service \(EKMS\) cryptographic module with external Amazon Web Services Key Management System \(AWS KMS\) key wrapping.

## Before you begin

Roles required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

Confirm that you have created a cryptographic module with external key wrapping enabled. See [Configure an external key definition](ekms-configure-external-key-definition.md).

## About this task

An Encrypted Field Configuration \(EFC\) connects a specific table column to your EKMS cryptographic module. EFC creates a secure encryption chain where your data can only be decrypted if both the ServiceNow data encryption key \(DEK\) and your external AWS key are available.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations** &gt; **New**.

2.  Complete the EFC form.

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

Algorithm Encrypted Preserving\[read-only\]

</td><td>

Indicates if the crypto module that you selected is already configured to support non-deterministic encryption. This means that if the same data is encrypted more than once, the encryption is different each time.

</td></tr><tr><td>

Encrypt by default

</td><td>

Select this option to verify records that fall outside of the defined criteria are still encrypted by the default field encryption module. If you don't select this option, any records that fall outside of the condition builder criteria won't be encrypted.

</td></tr><tr><td>

Crypto module

</td><td>

The cryptographic module that the encrypted field configuration applies to.**Note:** Verify that you select the crypto module that has the "External wrap key" flag enabled. Using a module without external wrapping encrypts data with ServiceNow's internal keys instead of your AWS KMS key.

</td></tr><tr><td>

Method

</td><td>

Select **Single Module** to apply this access policy to one cryptographic module. Select **Multiple Modules** to apply this access policy across multiple cryptographic modules.-   **Single Module**

Use this option to encrypt all attachments using a single module. Your users need access to this module, otherwise they aren't able to upload attachments.

-   **Multiple Modules**

Use this option to enable users to choose a module when uploading attachments. Users with access to one or more modules can select a module to use for encryption. Users with no module access can upload unencrypted attachments.

</td></tr></tbody>
</table>3.  Select **Submit**.

    ![Completed EFC form.](../image/ekms-create-efc-ui.png)


## Result

The field's data established by the EFC are encrypted using the Data Encryption Key \(DEK\) that is wrapped by your AWS KMS key.

## What to do next

Next steps:

-   [Configure module access policies to control which user roles can view the encrypted data in clear text](ekms-set-up-maps.md)
-   [Test access with users who have appropriate roles](ekms-test-external-key-definition.md)
-   [Test that users without appropriate roles can't view the encrypted data](ekms-change-status-aws-kms-key.md)

**Warning:** Without configured module access policies, users might be unable to view the encrypted data, or access might be unrestricted depending on your system configuration. Configure access policies immediately after creating encrypted field configurations.

**Parent Topic:**[Configuring External Key Management Service](../concept/ekms-configuring-external-key-management.md)

