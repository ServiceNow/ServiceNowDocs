---
title: Encrypt data using the Multiple Modules feature
description: Encrypt data with more than one encryption module permitting the user to determine which keys are used for specific rows within the encrypted data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using multiple encryption modules, Using Field Encryption, Field Encryption, Encryption]
---

# Encrypt data using the Multiple Modules feature

Encrypt data with more than one encryption module permitting the user to determine which keys are used for specific rows within the encrypted data.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager or sn\_kmf.admin

## About this task

The Multiple Modules option is considered non-deterministic and isn’t the preferred method because the user determines which key to use for a given record. The ability to use multiple modules for a column is being replaced by Row Conditions. See [Using multiple encryption modules](../../encryption/concept/using-multiple-encryption-modules.md). This non-deterministic implementation is still supported because it was created first and is still in use, but it’s preferred to use Row Conditions for any new multiple modules use cases.

**Note:** Only encryption on columns supports multiple modules. Attachment encryption doesn’t. Mass encryption isn’t available when using the multiple encryption modules method.

You can’t change a field using multiple encryption modules to use a single encryption module.

The field is encrypted by the encryption module of the first user to enter data. Because the encryption module is set on a per record basis, fields in a list can have different encryption modules. Within a single record, the field can be encrypted by only one module.

## Procedure

1.  Create multiple Field Encryption modules and a Module Access Policy \(MAP\) for each one.

    Make sure that you grant different roles to the different cryptographic modules through the access policies.

2.  Navigate to **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations** &gt; **New**.

    If you need more information on Encrypted Field Configurations, see [Set encrypted field configurations](../../encryption/task/set-encrypted-field-config.md).

3.  In the **Type** field, you must select **Column**.

    Attachment encryption doesn’t support multiple modules.

4.  Select **Multiple Modules** in the **Method** field.

    ![Multiple Modules selected as the method Encrypted Field Configurations.](../../encryption/image/EFC-multi-modules.png)

5.  Select the **Table** and the **Column** in the table that you want to encrypt.

6.  Select **Submit**.


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

**Parent Topic:**[Using multiple encryption modules](../../encryption/concept/using-multiple-encryption-modules.md)

**Parent Topic:**[Using Column Level Encryption](../../encryption/concept/using-column-level-encryption-2.md)

