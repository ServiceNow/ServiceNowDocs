---
title: Encrypt data using Row Conditions
description: Encrypt fields with multiple Field Encryption modules using Row Conditions to define the data being encrypted and the associated encryption keys. Row Conditions can also be used to define the users that have access using the condition builder.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using multiple encryption modules, Using Field Encryption, Field Encryption, Encryption]
---

# Encrypt data using Row Conditions

Encrypt fields with multiple Field Encryption modules using Row Conditions to define the data being encrypted and the associated encryption keys. Row Conditions can also be used to define the users that have access using the condition builder.

## Before you begin

Role required: security\_admin  and sn\_kmf.cryptographic\_manager  or sn\_kmf.admin

## About this task

**Note:** The following guidelines apply when using Row Conditions:

-   Row Conditions is only supported on encrypted columns and attachments.
-   Mass encryption isn’t available when using the multiple encryption modules method.
-   You can’t change a field using multiple encryption modules to use a single encryption module.
-   Row Conditions enables data to be encrypted on the main record. Dot-walking isn’t supported in the condition builder.
-   Row Conditions isn’t supported by the following service catalog tables:
    -   Options \[sc\_item\_option\]
    -   Question Answer \[question\_answer\]
    -   Multi Row Question Answer \[sc\_multi\_row\_question\_answer\]

The field is encrypted by the encryption module of the first user to enter data. Because the encryption module is set on a per record basis, fields in a list can have different encryption modules. Within a single record, the field can be encrypted by only one module.

## Procedure

1.  Create multiple cryptographic modules and an access policy for each one.

    Make sure that you grant different roles to the different cryptographic modules through the access policies.

2.  Navigate to **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Experience** &gt; **Create new module**.

    If you need more information on Encrypted Field Configurations, see [Set encrypted field configurations](set-encrypted-field-config.md).

3.  Select the **Table** and the **Column** in the table that you want to encrypt.

4.  Select **Encrypt by default** to encrypt saved records that don’t meet a defined row condition.

    If you select this option, make sure to select the **Crypto Module** to be used as a default encryption module.

    If this box isn’t selected and records that are added don't meet a row condition, they aren’t encrypted.

    For example, a Row Condition can be defined to encrypt records to declare that the "Department" field on the record equals "IT." Then, the records in which the "Department" field doesn’t equal "IT" wouldn’t be encrypted unless **Encrypt by default** is selected. This example utilizes a custom created "Department" Choice field on the sn\_customerservice\_case table, but other custom or default fields, if they are a supported data type of Row Conditions. The **Encrypt by default** option is selected by default. To create a configuration without this option selected, create the EFC from the **Configurations** page.

    ![Encrypt by default and associated Crypto module selected.](../image/fe-encrypt-by-default.png)

5.  Select **Submit**.

6.  Select the newly created Encrypted Field Configuration \(EFC\) from the **Configurations** tab.

7.  Select the **Add Row Conditions** box and **Add Condition**.![Create Row Conditions.](../image/fe-add-rcs.png)

8.  Define Row Conditions by filling out the required fields.

9.  Select **Submit**.


## Result

**Note:** Repeat this process as needed to ensure that the number of Row Conditions meet your required Encryption Crypto Modules \(ECMs\). When selecting Encrypt by default in the ECM setup, a Row Condition must also be established to define the default ECM selected.

Newly created data for the specified field is encrypted with the key for the relevant module. When a user with the role specified in module A's access policy writes to the specified table, the data is encrypted with module A's key. Only users with the same role can read the data.

## Example

This example explains how to encrypt the Short Description field on the Incident table. This example works similarly if you want to encrypt a different field in a table.

For encrypting the Short Description, you would do the following:

1.  Create two Field Encryption modules A and B.
2.  For each module, create a Module Access Policy \(MAP\) and define access as follows:
    1.  Module A – to users with an HR role.
    2.  Module B – to users with a Sales role.
3.  Create an Encrypted Field Configuration \(EFC\) record.
    1.  Navigate to **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations** &gt; **New**.
    2.  Select **Incident** in the Table field.
    3.  Select **Short Description** in the Column field.
    4.  Select the **Encrypt by default** box if you must verify any records that fall outside of the condition builder criteria are still encrypted by the default field encryption module. Not selecting this option would mean that any records that fall outside of the condition builder criteria won’t be encrypted.

        Enter the default crypto module in the related **Crypto module** field.

    5.  Select **Submit**.
4.  Create the Row Conditions.
5.  Run the appropriate encryption job:

    -   Mass Encryption - Run this job when a new Row Condition is created.
    -   Mass Rekeying - Run this job when an existing Row Condition is modified.
    See [Schedule mass encryption, decryption, and rekeying jobs](schedule-mass-jobs.md).

6.  Have a user from Module A and a user from Module B create an incident with a short description. Have both users view the list of incidents.

The short description for the incident created by the user with the HR role is encrypted by the key for module A. The short description for the incident created by the user with the Sales role is encrypted by the key for module B.

All users with the HR and Sales roles have access to incidents. However, only a user with the HR role can decrypt and view the short description for those incidents created by another user with the HR role. Likewise, only users with the Sales role can decrypt and view the short descriptions for those incidents created by the user B, who had the Sales role.

![Diagram displays viewable fields of the Row Condition example.](../image/MMASSET0021135-multi-encryption-square.svg)

## What to do next

Perform one of the following operations:

-   Schedule a **Mass Encryption** job to update the encryption of the condition field.
-   If modifying an existing Row Condition run a **Mass Rekeying** job to encrypt necessary data with the updated encryption module.

See [Schedule mass encryption, decryption, and rekeying jobs](schedule-mass-jobs.md)

**Parent Topic:**[Using multiple encryption modules](../concept/using-multiple-encryption-modules.md)

