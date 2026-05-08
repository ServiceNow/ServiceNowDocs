---
title: Encrypting fields and attachments
description: Once cryptographic modules are created, a security admin can define the encrypted fields configuration \(EFC\) and opt to encrypt a field or attachment on a table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Field Encryption, Field Encryption, Encryption]
---

# Encrypting fields and attachments

Once cryptographic modules are created, a security admin can define the encrypted fields configuration \(EFC\) and opt to encrypt a field or attachment on a table.

## How to encrypt fields

**Note:** Encrypted fields aren’t audited by design. This behavior isn’t configurable.

1.  Specify the key source: ServiceNow generated keys or your customer-supplied keys \(bring your own key\) in **System Security** &gt; **Field Encryption Settings**.
2.  After specifying the key source, create a cryptographic module or use an existing cryptographic module. Start with [Create a cryptographic module](../../key-management-framework/task/create-cryptographic-module.md) for instructions.

    **Note:** If you use customer-supplied keys, follow the directions in [Create cryptographic module for Field Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md) and [Configure properties for customer-supplied keys](customer-supplied-keys.md).

3.  Create an encrypted field configuration to define where the encryption is applied. Here, you specify the target table and choose whether to encrypt a column or attachments within the table. See [Set encrypted field configurations](../task/set-encrypted-field-config.md) to get started.

**Note:** See [Field Encryption Enterprise examples](../../key-management-framework/concept/kmf-walkthroughs-tutorials.md#) that illustrates how to encrypt fields and attachments using customer-supplied keys.

-   **[Set encrypted field configurations](../task/set-encrypted-field-config.md)**  
Configure which table columns or attachments that the system encrypts using a preconfigured cryptographic module.
-   **[Script access for cryptographic modules](../../key-management-framework/concept/script-map.md)**  
Scripts can be run to access a cryptographic module policy for a cryptographic purpose.
-   **[Schedule mass encryption, decryption, and rekeying jobs](../task/schedule-mass-jobs.md)**  
Schedule encryption, decryption, and rekeying jobs to run at a time that is best for your instance.
-   **[Run mass encryption or decryption](../task/mass-enc-dec.md)**  
You can run mass encryption on encryption configurations, as well as a mass decryption to decrypt previously encrypted values.
-   **[Upload attachments for encryption](../task/upload-attachments-for-encryption.md)**  
Protect sensitive files by encrypting record attachments using Field Encryption and Row Conditions.
-   **[Module access policies for inbound email attachment encryption](fe-maps-inbound-email-attachment-encryption.md)**  
Encrypting inbound email attachments associated with matched records requires one or more module access policies \(MAPs\).

**Parent Topic:**[Using Field Encryption](using-column-level-encryption.md)

**Parent Topic:**[Using Column Level Encryption](using-column-level-encryption-2.md)

