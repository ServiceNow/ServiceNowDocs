---
title: Create a cryptographic specification
description: After you create a cryptographic module, create a cryptographic specification to define the module algorithms.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a cryptographic module, Key Management Framework Reference, Key Management Framework, Encryption]
---

# Create a cryptographic specification

After you create a cryptographic module, create a cryptographic specification to define the module algorithms.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## Procedure

1.  Navigate to **Key Management** &gt; **Cryptographic Modules** &gt; **All**.

2.  Select the cryptographic module for definition to open the configuration options.

3.  On the **Crypto Specifications** tab, click **New**.

    ![Crypto Specifications tab.](../image/new-crypto-spec.png)

4.  Complete the Algorithm Definition form.

    See [Cryptographic specification](../concept/cryptographic-purpose.md) for details.

    ![Definition form for the key algorithm.](../image/algorithm-definition.png)

    The algorithm definition screen opens. Select options for the key generation. Repeat this step to generate multiple keys for the selected crypto module.

<table id="table_bbk_5v4_kqb"><thead><tr><th>

Field

</th><th>

 

</th></tr></thead><tbody><tr><td>

Crypto module

</td><td>

Read only. Name of the selected cryptographic module displays.

</td></tr><tr><td>

Crypto purpose

</td><td>

Select the purpose of this module. For example, you might use it for data encryption, signature generation, or key wrapping. The available algorithms adjust based on the selected crypto purpose. See [Cryptographic specification](../concept/cryptographic-purpose.md) for details.

</td></tr><tr><td>

Algorithm

</td><td>

Type of algorithm used to accomplish the crypto purpose. The algorithm also controls the key origin. Adjusts automatically based on the selected crypto purpose. [Cryptographic specification](../concept/cryptographic-purpose.md) for details.

</td></tr><tr><td>

Operation mode

</td><td>

This field may display based on the selected crypto purpose.

</td></tr><tr><td>

Size

</td><td>

Select the bit size.

</td></tr><tr><td>

Hash

</td><td>

This field becomes available based on the algorithm selected.

</td></tr><tr><td>

Equality preserving

</td><td>

Enables non-deterministic encryption.

 This option appears when you select **Symmetric Data Encryption/Decryption** with **AES** and in **Cipher Block Chaining \(CBC\)** mode.

 Selecting this option means that if the same data is encrypted again the encoded data is the same each time. Non-deterministic encryption does not support filtering a list of encrypted data using equality comparison operators.

</td></tr><tr><td>

Integrity

</td><td>

GCM operation mode provides Integrity.

</td></tr></tbody>
</table>5.  Click **Next**.

    The crypto specification is listed on the Key Lifecycle table based on the algorithms selected.


## What to do next

Perform one of the following operations:

-   Select an entry in the Key Lifecycle table to define key lifecycle behavior. See [Configure key lifecycle states](configure-key-lifecycle-states.md) for details to complete the lifecycle definition for the key.
-   Click **Next** to create a cryptographic key. See one of the following tasks for key generation:
    -   [Generate a ServiceNow cryptographic key](generate_sn_key.md).
    -   [Configure properties for customer-supplied keys](../../encryption/concept/customer-supplied-keys.md).
    -   [Import the wrapping / unwrapping key pair](../concept/import-key-webservice-1.md#).

**Parent Topic:**[Create a cryptographic module](create-cryptographic-module.md)

