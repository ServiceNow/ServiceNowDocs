---
title: Encrypting fields and attachments
description: Once cryptographic modules are created, a security admin can define the encrypted fields configuration \(EFC\) and opt to encrypt a field or attachment on a table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/field-encryption-key-management.html
release: zurich
topic_type: concept
last_updated: "2025-09-03"
reading_time_minutes: 2
breadcrumb: [Using Field Encryption, Field Encryption, Encryption]
---

# Encrypting fields and attachments

Once cryptographic modules are created, a security admin can define the encrypted fields configuration \(EFC\) and opt to encrypt a field or attachment on a table.

## How to encrypt fields

**Note:** Encrypted fields aren’t audited by design. This behavior isn’t configurable.

1.  Specify the key source: ServiceNow generated keys or your customer-supplied keys \(bring your own key\) in **System Security** &gt; **Field Encryption Settings**.
2.  After specifying the key source, create a cryptographic module or use an existing cryptographic module. Start with [Create a cryptographic module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/create-cryptographic-module.md) for instructions.

    **Note:** If you use customer-supplied keys, follow the directions in [Create cryptographic module for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/create-PE-cryptographic-module.md) and [Configure properties for customer-supplied keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/customer-supplied-keys.md).

3.  Create an encrypted field configuration to define where the encryption is applied. Here, you specify the target table and choose whether to encrypt a column or attachments within the table. See [Set encrypted field configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/set-encrypted-field-config.md) to get started.

**Note:** See [Field Encryption Enterprise examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/kmf-walkthroughs-tutorials.md) that illustrates how to encrypt fields and attachments using customer-supplied keys.

-   **[Set encrypted field configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/set-encrypted-field-config.md)**  
Configure which table columns or attachments that the system encrypts using a preconfigured cryptographic module.
-   **[Script access for cryptographic modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/script-map.md)**  
Scripts can be run to access a cryptographic module policy for a cryptographic purpose.
-   **[Schedule mass encryption, decryption, and rekeying jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/schedule-mass-jobs.md)**  
Schedule encryption, decryption, and rekeying jobs to run at a time that is best for your instance.
-   **[Run mass encryption or decryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/mass-enc-dec.md)**  
You can run mass encryption on encryption configurations, as well as a mass decryption to decrypt previously encrypted values.
-   **[Upload attachments for encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/upload-attachments-for-encryption.md)**  
Protect sensitive files by encrypting record attachments using Field Encryption and Row Conditions.

**Parent Topic:**[Using Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/using-column-level-encryption.md)

**Parent Topic:**[Using Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/using-column-level-encryption-2.md)

