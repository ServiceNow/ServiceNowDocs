---
title: Encrypting fields and attachments
description: After you create your cryptographic modules, create encrypted field configurations and specify whether to encrypt a field on a table or encrypt attachments.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Encrypting fields and attachments

After you create your cryptographic modules, create encrypted field configurations and specify whether to encrypt a field on a table or encrypt attachments.

## How to encrypt fields

**Note:** Encrypted fields are not audited by design. This behavior is not configurable.

1.  Specify the key source: system-generated keys or your customer supplied keys \(bring your own key\) in **System Security** &gt; **Field Encryption Settings**.
2.  After you specify the key source, create a new cryptographic module or use an existing cryptographic module. Start with [Create a cryptographic module](../../key-management-framework/task/create-cryptographic-module.md) for instructions.

    **Note:** If you use customer-supplied keys, follow the directions in [Create cryptographic module for Column Level Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md) and [Configure properties for customer-supplied keys](customer-supplied-keys.md).

3.  Create an encrypted field configuration, which is where you specify the table on which the encryption is performed and either the column in the table or the attachments in the table to encrypt. See [Set encrypted field configurations](../task/set-encrypted-field-config.md) to get started.

**Note:** See [Column Level Encryption Enterprise examples](../../key-management-framework/concept/kmf-walkthroughs-tutorials.md#) that illustrates how to encrypt fields and attachments using customer-supplied keys.

-   **[Set encrypted field configurations](../task/set-encrypted-field-config.md)**  
Configure which table columns or attachments that the system encrypts using a preconfigured cryptographic module.
-   **[Script access for cryptographic modules](../../key-management-framework/concept/script-map.md)**  
Scripts can be run to access a cryptographic module policy for a cryptographic purpose.
-   **[Schedule mass encryption, decryption, and rekeying jobs](../task/schedule-mass-jobs.md)**  
Schedule encryption, decryption, and rekeying jobs to run at a time that is best for your instance.
-   **[Run mass encryption or decryption](../task/mass-enc-dec.md)**  
You can run mass encryption on encryption configurations, as well as a mass decryption to decrypt previously encrypted values.

**Parent Topic:**[Using Column Level Encryption](using-column-level-encryption.md)

