---
title: Configure Field Encryption for your Edge Encrypted fields
description: Before migrating your existing edge encrypted fields to Field Encryption, you must configure field encryption for these fields.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Migrate from Edge Encryption to Field Encryption, Configuring Field Encryption, Field Encryption, Encryption]
---

# Configure Field Encryption for your Edge Encrypted fields

Before migrating your existing edge encrypted fields to Field Encryption, you must configure field encryption for these fields.

## Before you begin

Role required: admin

This process assumes you have existing edge encrypted fields that you want to migrate to Field Encryption.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Cryptographic Modules** &gt; **All** &gt; **.**

2.  In the Cryptographic Modules list, select **New**.

3.  In the form, fill in these fields.

    |Field|Value|
    |-----|-----|
    |Name|Select descriptive name|
    |Crypto spec template|Default template|
    |Crypto module lifecycle state|Published|
    |Parent crypto module|column\_level\_encryption|

4.  Right-click the form header and select **Save**.

5.  In the **Crypto Specifications** related list, open the record on the list.

6.  In the **Crypto Specification** record, select **Next** three times to complete the algorithm definition, lifecycle definition, and key origin sections.

    You don’t need to modify any fields in these sections.

7.  In the **Generate Key** field, select the **Generate Key** link to generate a key.

8.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configuration**.

9.  In the encrypted field configuration list, select **New**.

10. In the form, fill in these fields.

    |Field|Value|
    |-----|-----|
    |Type|Select Column or Attachment, depending on what you want to encrypt.|
    |Crypto module|Select the cryptographic module that you created in earlier steps.|
    |Table|Select the table containing the data that you want encrypted.|
    |Method|Select `Single Module`|
    |Column|Select the column \(field\) on the table that you want to be encrypted.|

    **Note:** The data to encrypt is determined by the Table and Column fields. These fields should be the table and column \(field\) where you’re currently using Edge Encryption.

11. Select **Submit**.

12. Navigate to **All** &gt; **Key Management** &gt; **Module Access Policies** &gt; **All**.

13. Select **New**.

14. In the form, fill in these fields.

    |Field|Value|
    |-----|-----|
    |Policy name|Select descriptive name|
    |Crypto module|Select the cryptographic module that you created in earlier steps.|
    |Type|Select `Role`|
    |Target role|Select a role to be used. This role must be able to encrypt and decrypt data in the column.|
    |Result|Select the desired action.|

15. Select **Submit**.

16. To verify your configuration, navigate to the table you want encrypted with Field Encryption, and open a record.

    For example, to access the User \[sys\_user\] table, enter `sys_user.list` into the navigation filter.

    The field you have selected for encryption in the previous steps now has a lock icon next to the field label.


## Result

You edge encrypted field is ready to be migrated to field encryption. To configure more fields, repeat the preceding steps for each of those fields.

**Parent Topic:**[Migrate from Edge Encryption to Field Encryption](../concept/migrate-ee-to-fe.md)

