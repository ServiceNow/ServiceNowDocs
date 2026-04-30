---
title: Using Column Level Encryption
description: Use Column Level Encryption to manage access to encrypted data on your instances.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Column Level Encryption, Encryption]
---

# Using Column Level Encryption

Use Column Level Encryption to manage access to encrypted data on your instances.

Use the related links to find information on common Column Level Encryption tasks.

-   **[Create cryptographic module for Column Level Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md)**  
Create a Column Level Encryption cryptographic module to define the mechanisms used for cryptographic operations.
-   **[Using multiple encryption modules](../../key-management-framework/task/multiple-module-access-policies.md)**  
Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but they can still be prevented from viewing each others encrypted data.
-   **[Create a cryptographic specification for Column Level Encryption](../../key-management-framework/task/create-crypto-spec-pe.md)**  
After you create a cryptographic module, access the corresponding cryptographic specification to define the algorithm.
-   **[Configure advanced algorithms for Column Level Encryption Enterprise](../../key-management-framework/task/adv-algorithm-cleent.md)**  
Create a cryptographic specification to define the algorithm for a cryptographic module. Customize the encryption specifications with advanced options that are available for Column Level Encryption Enterprise.
-   **[Using customer supplied keys with Column Level Encryption Enterprise](csk-landing.md)**  
You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.
-   **[Encrypting fields and attachments](field-encryption-key-management.md)**  
After you create your cryptographic modules, create encrypted field configurations and specify whether to encrypt a field on a table or encrypt attachments.
-   **[Column Level Encryption Enterprise examples](../../key-management-framework/concept/kmf-walkthroughs-tutorials.md#)**  
These examples walk you through the encryption of fields and attachments using customer-supplied keys.

**Parent Topic:**[Column Level Encryption](column-level-encryption-landing.md)

**Related topics**  


[Create cryptographic module for Column Level Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md)

[Using multiple encryption modules](../../key-management-framework/task/multiple-module-access-policies.md)

[Create a cryptographic specification for Column Level Encryption](../../key-management-framework/task/create-crypto-spec-pe.md)

[Configure advanced algorithms for Column Level Encryption Enterprise](../../key-management-framework/task/adv-algorithm-cleent.md)

[Configure properties for customer-supplied keys](customer-supplied-keys.md)

[Encrypting fields and attachments](field-encryption-key-management.md)

[Column Level Encryption Enterprise examples](../../key-management-framework/concept/kmf-walkthroughs-tutorials.md#)

