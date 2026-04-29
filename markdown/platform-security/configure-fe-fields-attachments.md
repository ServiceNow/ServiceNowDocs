---
title: Configure encrypted field configurations for fields or attachments
description: Create an encrypted field configuration to specify which fields are encrypted on a table, and whether that table's attachments are encrypted.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Configure encrypted field configurations for fields or attachments

Create an encrypted field configuration to specify which fields are encrypted on a table, and whether that table's attachments are encrypted.

## Before you begin

Role required: security\_admin and sn\_kmf.cryptographic\_manager or sn\_kmf.admin

You must have a configured field encryption module with a ServiceNow or customer-supplied key. If you have not yet configured a module, see [Configure Field Encryption modules](configure-fe-modules.md).

## Procedure

1.  Ensure that you are in the same application scope as the table you want to encrypt.

2.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience** &gt; **Modules**.

3.  Select **Create new**.

4.  In the **Encrypted Field Configuration** form, fill in the fields as needed.

<table id="table_pnt_42l_f2c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select either **Column** or **Attachment****Note:** Attachment encryption is only available with Field Encryption Enterprise.

</td></tr><tr><td>

Table

</td><td>

Select the table which will have it's fields or attachments encrypted.

</td></tr><tr><td>

Column

</td><td>

If you have chosen **Column** in the **Type** field, select the fields to be encrypted.**Note:** If the field you want to encrypt is not available, it may not be a supported type. The supported field types are:

-   String \(including Full UTF-8\)
-   Date
-   Date/Time
-   URL
-   HTML
-   Journal
-   Translated
-   Email
-   Phone


</td></tr><tr><td>

Active

</td><td>

Whether the configuration is active.**Important:**

When active, your instance is actively encrypting new data in the selected fields or attachments. Users will not have access to this data unless they have permission via an associated Module Access Policy. Do not check if the field is not yet ready to begin encrypting and enforcing Module Access Policies.

To ensure historical data is encrypted after an Encrypted Field Configuration is active, you’ll need to run a Mass Encryption Job on the column. For details, see [Schedule mass encryption, decryption, or rekeying jobs](schedule-mass-jobs.md).

</td></tr><tr><td>

Crypto Module

</td><td>

The field encryption module use by this encrypted field configuration.

</td></tr><tr><td>

Method

</td><td>

Select **Single Module** to ensure all fields or attachments are encrypted by a single field encryption module.

 Select **Multi Module** to allow for different field encryption modules to be used for different rows within a column or different attachments. For details on multi-module configuration, see[Configure multi-module encrypted field configurations](multi-module-fe-config.md).

</td></tr><tr><td>

Algorithm Equality Preserving

</td><td>

Displays whether **Equality Preserving** is enabled in the field encryption module selected in the **Crypto Module** field.

</td></tr></tbody>
</table>5.  Select **Save**.


**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

