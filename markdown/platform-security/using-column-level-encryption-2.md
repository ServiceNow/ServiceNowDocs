---
title: Using Column Level Encryption
description: Use Column Level Encryption to manage access to encrypted data on your instances.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2026-01-31"
reading_time_minutes: 2
breadcrumb: [Column Level Encryption, Encryption]
---

# Using Column Level Encryption

Use Column Level Encryption to manage access to encrypted data on your instances.

Use the related links to find information on common Column Level Encryption tasks.

-   **[Create cryptographic module for Column Level Encryption](../../key-management-framework/task/create-PE-cryptographic-module-2.md)**  
Create a Column Level Encryption cryptographic module to define the mechanisms used for cryptographic operations.
-   **[Using multiple encryption modules](../../key-management-framework/task/multiple-module-access-policies.md)**  
Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but they can still be prevented from viewing each others encrypted data.
-   **[Create a cryptographic specification for Column Level Encryption Enterprise](../../key-management-framework/task/create-crypto-spec-pe-2.md)**  
After you create a cryptographic module, access the corresponding cryptographic specification to define the algorithm.
-   **[Configure advanced algorithms for Column Level Encryption Enterprise](../../key-management-framework/task/adv-algorithm-cleent-2.md)**  
Create a cryptographic specification to define the algorithm for a cryptographic module. Customize the encryption specifications with advanced options that are available for Column Level Encryption Enterprise.
-   **[Configure properties for customer-supplied keys](customer-supplied-keys.md)**  
If the Column Level Encryption Enterprise plugin is enabled, you can use system properties to define key padding, ephemeral key pair size, and a key validity period of your customer-supplied keys.
-   **[Encrypting fields and attachments](field-encryption-key-management.md)**  
After you create your cryptographic modules, create encrypted field configurations and specify whether to encrypt a field on a table or encrypt attachments.
-   **[Column Level Encryption examples](../../key-management-framework/concept/kmf-walkthrough-tutorials-2.md)**  
These examples walk you through the encryption of fields and attachments using customer-supplied keys.

**Parent Topic:**[Column Level Encryption](column-level-encryption-landing.md)

**Related topics**  


[Create cryptographic module for Field Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md)

[Using multiple encryption modules](../../key-management-framework/task/multiple-module-access-policies.md)

[Create a cryptographic specification for Column Level Encryption Enterprise](../../key-management-framework/task/create-crypto-spec-pe-2.md)

[Configure advanced algorithms for Column Level Encryption Enterprise](../../key-management-framework/task/adv-algorithm-cleent-2.md)

[Configure properties for customer-supplied keys](customer-supplied-keys.md)

[Encrypting fields and attachments](field-encryption-key-management.md)

[Column Level Encryption examples](../../key-management-framework/concept/kmf-walkthrough-tutorials-2.md)

