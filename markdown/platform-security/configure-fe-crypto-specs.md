---
title: Cryptographic specifications for Field Encryption
description: Use cryptographic specifications to define the purpose, algorithm, key length, mode, and origin of your encryption key.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Cryptographic specifications for Field Encryption

Use cryptographic specifications to define the purpose, algorithm, key length, mode, and origin of your encryption key.

## Before you begin

Role required: KMF Admin or KMF Cryptographic Manager

## About this task

This procedure shows how to configure generated keys. A data encryption key \(known as a Module Key\) is automatically populated once you have configured the Crypto Specifications.

For customer-supplied key configuration, see [Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Modules**.

2.  In the **Cryptographic Modules** list, open the module record you want to configure.

    **Note:** The names displayed in the list are appended with the scope, for example, `global.[your Field Encryption Module name]`.

3.  In the **Crypto Specifications** related list, open the cryptographic specific record by selecting the name under **Key alias**.

    ![Cryptographic Specifications related list](../image/crypto-spec-list-1.png)

4.  In the Cryptographic Specifications form, fill out the fields as needed.

    **Note:** The fields are divided into sections. Select the **Next** or **Back** buttons to navigate between sections.

<table id="table_xfy_lsd_f2c"><thead><tr><th>

Section

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Algorithm Definition

</td><td>

Crypto module

</td><td>

Displays the name of the selected cryptographic module.

</td></tr><tr><td>

Crypto purpose

</td><td>

The purpose of the selected algorithm, key, length, and mode. For Field Encryption, this field is read only and has a value of **Symmetric Data Encryption/Decryption**.

</td></tr><tr><td>

Algorithm

</td><td>

Select a type of algorithm used to accomplish the cryptographic purpose. The options available are filtered to align to the selected cryptographic purpose.

</td></tr><tr><td rowspan="10">

Lifecycle Definition

</td><td>

Applies to

</td><td>

Displays the selected key that the lifecycle applies to.

</td></tr><tr><td>

For field

</td><td>

Select the type of control for the key that you want to apply for the lifecycle. -   Expiration date
-   Future activation date
-   Future destruction date
-   Future renewal date
-   Future rotation date


</td></tr><tr><td>

Key type

</td><td>

 

</td></tr><tr><td>

Lifecycle default

</td><td>

 

</td></tr><tr><td>

Order

</td><td>

Order in which to process the key lifecycle state for the crypto specification. Lower values execute before higher values.

</td></tr><tr><td>

Relative duration

</td><td>

Number of years, months, or days the key is valid.

</td></tr><tr><td>

Relative duration type

</td><td>

Duration type of the lifecycle. Select from **Years**, **Months**, or **Days**.

</td></tr><tr><td>

Relative operation

</td><td>

Choose **Before** or **After**.

</td></tr><tr><td>

Relative to

</td><td>

Select a field that the duration is relative to.-   Activation date
-   Compromise date
-   Deactivation date
-   Destruction date
-   Expiration date
-   Generation date
-   Last renewal date
-   Last rotated date
-   Revocation date
**Note:** This field works together with the value selected in the **Relative operation** field.

</td></tr><tr><td>

Type

</td><td>

Select if the value for the key lifecycle is relative or absolute.-   **Relative**

Enter a value that depends on other data entries in the system, such as key generation, activation, and deactivation.

-   **Absolute**

Enter an exact value, such as a date.

</td></tr><tr><td rowspan="5">

Key Origin

</td><td>

Crypto module

</td><td>

Displays the Name of the selected cryptographic module.

</td></tr><tr><td>

Origin

</td><td>

Whether the key originated from or is supplied by the customer.-   For starter, select **Servicenow**
-   For Enterprise, select **Servicenow** or **Customer Supplied**


</td></tr><tr><td>

Key alias

</td><td>

Name of the cryptographic module with the scope appended to the front of the name.

</td></tr><tr><td>

Crypto purpose

</td><td>

Displays the purpose of the selected algorithm, key, length, and mode. For Field Encryption, this field is read only and has a value of **Symmetric Data Encryption/Decryption**.

</td></tr><tr><td>

Algorithm

</td><td>

Displays the algorithm used to accomplish the crypto purpose.

</td></tr><tr><td rowspan="7">

Key Creation

</td><td>

Crypto module

</td><td>

Displays the name of the selected cryptographic module.

</td></tr><tr><td>

Key alias

</td><td>

Displays the name of the cryptographic module with the scope appended to the front of the name.

</td></tr><tr><td>

Generate Key

</td><td>

Select this link to generate your data encryption key if you're using a generated key, and not a customer supplied key.

</td></tr><tr><td>

Auto generate key

</td><td>

If you don’t select the **Generate key** link, a data encryption key is automatically generated during the first time data must be encrypted using the cryptographic module.

</td></tr><tr><td>

Crypto purpose

</td><td>

Displays the purpose of the selected algorithm, key, length, and mode. For Field Encryption, this field is read only and has a value of **Symmetric Data Encryption/Decryption**.

</td></tr><tr><td>

Origin

</td><td>

Displays the value that was selected during the **Key Origin** section.

</td></tr><tr><td>

Algorithm

</td><td>

Displays the algorithm used to accomplish the crypto purpose.

</td></tr></tbody>
</table>5.  Select **Go To Crypto Module** to return to your Module record.

    In the Module record, there’s now an entry in the **Module Keys** related list. The **Key alias** field in the **Crypto Specifications** related list is now empty, since the key alias has moved to the new module key.


## What to do next

For information on using a customer supplied key, see [Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md).

**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

