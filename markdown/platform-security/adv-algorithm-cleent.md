---
title: Configure advanced algorithms for Column Level Encryption Enterprise
description: Create a cryptographic specification to define the algorithm for a cryptographic module. Customize the encryption specifications with advanced options that are available for Column Level Encryption Enterprise.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-10-22"
reading_time_minutes: 2
breadcrumb: [Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Configure advanced algorithms for Column Level Encryption Enterprise

Create a cryptographic specification to define the algorithm for a cryptographic module. Customize the encryption specifications with advanced options that are available for Column Level Encryption Enterprise.

## Before you begin

Role required: admin

## Procedure

1.  On the **Crypto Specifications \(\#\)** tab, click **New**.

    ![Crypto Specifications tab.](../image/new-crypto-spec.png)

2.  On the form, fill in the fields.

<table id="table_ff2_jwq_fqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Crypto module

</td><td>

Name of the selected cryptographic module populates.

</td></tr><tr><td>

Crypto purpose

</td><td>

The value is **Symmetric Data Encryption/Decryption** for Column Level Encryption Enterprise.

</td></tr><tr><td>

Algorithm

</td><td>

The value is **AES** for Column Level Encryption Enterprise.

</td></tr><tr><td>

Operation mode

</td><td>

The value is **CBC** for Column Level Encryption Enterprise.

</td></tr><tr><td>

Size

</td><td>

Possible values are **256** and **128**.

**Note:** 256-bit size is most secure for encryption and is used for Symmetric Data Encryption/Decryption for Column Level Encryption Enterprise.

</td></tr><tr><td>

Equality preserving

</td><td>

Option to enable deterministic encryption.

 **Note:** Selecting this option means that the encrypted value of a field should be the same when the field value remains the same.

 Option to enable **Symmetric Data Encryption/Decryption** with **AES** in **Cipher Block Chaining \(CBC\)** mode.

</td></tr><tr><td>

Integrity

</td><td>

Option to provide Integrity in GCM operation and does not apply for Column Level Encryption Enterprise functionality.

</td></tr></tbody>
</table>3.  Click **Submit**.

    The following example shows AES CBC-256 encryption. When Column Level Encryption Enterprise is active and the parent module is column\_level\_encryption, only Symmetric Data Encryption/Decryption AES CBC-256 applies as the crypto purpose. See [Cryptographic specification](../concept/cryptographic-purpose.md) for details.

    ![Shows the AES-CBC-256 encryption configuration options.](../image/algorithm-definition.png)


## What to do next

Perform one of the following operations:

-   Select an entry in the Key Lifecycle table to define key lifecycle behavior. See [Configure key lifecycle states](configure-key-lifecycle-states.md) for details to complete the lifecycle definition for the key.
-   Select **Next** to create a cryptographic key. See one of the following tasks for key generation:
    -   [Generate a ServiceNow cryptographic key](generate_sn_key.md).
    -   [Configure properties for customer-supplied keys](../../encryption/concept/customer-supplied-keys.md).
    -   [Import the wrapping / unwrapping key pair](../concept/import-key-webservice-1.md#).

**Parent Topic:**[Using Column Level Encryption](../../encryption/concept/using-column-level-encryption.md)

