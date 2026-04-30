---
title: Using multiple encryption modules
description: Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but they can still be prevented from viewing each others encrypted data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Using multiple encryption modules

Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but they can still be prevented from viewing each others encrypted data.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager or sn\_kmf.admin

## About this task

**Note:** Only encryption on columns supports multiple modules. Attachment encryption does not. Mass encryption is not available when using the multiple encryption modules method.

You cannot change a field using multiple encryption modules to use a single encryption module.

The field is encrypted by the encryption module of the first user to enter data. Because the encryption module is set on a per record basis, fields in a list can have different encryption modules. Within a single record, the field can be encrypted by only one module.

## Procedure

1.  Create multiple cryptographic modules and an access policy for each one.

    Make sure that you grant different roles to the different cryptographic modules through the access policies.

2.  Navigate to **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations**.

    If you need more information on Encrypted Field Configurations, see [Set encrypted field configurations](../../encryption/task/set-encrypted-field-config.md).

3.  In the **Type** field, you must select **Column**.

    Attachment encryption does not support multiple modules.

4.  Select **Multiple Modules** in the **Method** field.

    ![Multiple Modules selected as the method Encrypted Field Configurations.](../image/select-multi-modules.png)

5.  Select the **Table** and the **Column** in the table that you want to encrypt.

6.  Click **Submit**.


## Result

Newly created data for the specified field is encrypted with the key of the relevant module. When a user with the role specified in module A's access policy writes to the specified table, the data is encrypted with module A's key. Only users with the same role can read the data.

## Example

To encrypt the Short Description column on the Incident table. You would do the following:

1.  Create two cryptographic modules A and B.
2.  For each module, create a module access policy.

    For module A, give users with an HR role access. For module B, give users with a Sales role access.

3.  Create an Encrypted Field Configuration record specifying the Short Description column on the Incident table, and make sure that you select **Multiple Modules** in the **Method** field.
4.  Have two users, one with the HR role \(user A\) and one with the Sales role \(user B\), create an incident with a short description, and then have both users look at the list of incidents.

    The short description for the incident created by the user with the HR role is encrypted by the key for module A. Likewise, the short description for the incident created by the user with the Sales role is encrypted by the key for module B.

    Although all users with the HR and Sales roles have access to incidents, only a user with the HR role can decrypt and view the short description for those incidents created by user A, who had the HR role. Likewise, only users with the Sales role can decrypt and view the short descriptions for those incidents created by the user B, who had the Sales role.


![Shows a diagram of multiple modules.](../image/MultipleModules.png)

**Parent Topic:**[Using Column Level Encryption](../../encryption/concept/using-column-level-encryption.md)

