---
title: Configure multi-module encrypted field configurations
description: Create an encrypted field configuration that uses more than one encryption module.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Configure multi-module encrypted field configurations

Create an encrypted field configuration that uses more than one encryption module.

## Before you begin

Role required: KMF Admin or KMF Cryptographic Manager, Security Admin

You must have a configured field encryption module with a ServiceNow or customer-supplied key. If you have not yet configured a module, see [Configure Field Encryption modules](configure-fe-modules.md).

## About this task

Use multiple encryption modules for a single encrypted field configuration to encrypt different rows within a column \(or different attachments on the same table\) using different module keys. For example, users with different roles can encrypt data on the same table, but still be prevented from decrypting each others encrypted data.

**Warning:**

Note these limitations on multi-module encrypted field configuration before proceeding:

-   Mass encryption isn’t supported for multi-module encrypted field configurations.
-   You can’t change a field configuration from a multi-module to a single module. Instead, you must deactivate the multi-module field configuration and create a new single module one.
-   Which module key a multi-module field configuration uses is determined by the first user to enter data into a field. Because the field encryption module is set on a per-record basis, fields in a list can be encrypted by different field encryption modules. However, within a single record, the field can be encrypted by only one field encryption module.

## Procedure

1.  Verify that you are in the same application scope as the table you want to encrypt.

2.  Confirm that you have the field encryption modules you want to use created.

    If you have not done so, see [Configure Field Encryption modules](configure-fe-modules.md).

3.  Confirm that each of your modules has a module access policy.

    If you have not done so, see [Configure module access policies for field encryption](maps-for-fe.md).

4.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations**.

5.  Open of create an encrypted field configuration record.

6.  In the **Method** field, select **Multiple Modules**.

7.  Select **Column** or **Attachment** in the **Type** field, depending on your need.

8.  Select a table in the **Table** field, and column in the **Column** field, if applicable.

9.  Select **Submit**.


## Result

After the record is saved, and the **Active** field is enabled, new data created for the specified field is encrypted with the module key of the relevant field encryption module. When a user with the role in module access policy “A” writes to the specified table, the data is encrypted with field encryption modules “A”’s module key. In this case, only users with the same role are able to decrypt that data.

## Encrypting the Short Description column on the Incident table using a multi-module encrypted field configuration

1.  Create two field encryption modules, referred to A and B in this example.
2.  For each field encryption module, create a module access policy \(MAPs A and B\).
    1.  For field encryption module A, give users with an HR role access to Module Access Policy A.
    2.  For field encryption module B, give users with a Sales role access to Module Access Policy B.
3.  Create an encrypted field configuration record specifying the Short Description column on the Incident table, and make sure that you select **Multiple Modules** in the **Method** field.
4.  Have two users:

    -   One with the HR Role related to MAP A and field encryption module A \(User A\)
    -   One with the Sales role related to MAP B and field encryption module B \(User B\)
    create an incident record with a short description value. Have both users look at the list of incidents.

    1.  The short description for the incident record created by User A is encrypted with the key for field encryption module A.
    2.  The short description for the incident record created by User B is encrypted with the key for field encryption module B.
5.  Users with the HR and Sales roles have access to incidents. Only a user with the HR role can decrypt and view the short description for those incidents created by User A \(who had the HR Role\). Only users with the Sales role can decrypt and view the short descriptions for those incidents created by User B \(who has the Sales role\).

![Venn diagram showing a multi-module configuration](../image/map-example.png)

**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

