---
title: Using Field Encryption
description: Use Field Encryption to manage access to encrypted data on your instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/using-column-level-encryption.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Field Encryption, Encryption]
---

# Using Field Encryption

Use Field Encryption to manage access to encrypted data on your instances.

There are two methods of encrypting field data:

-   Single module - Permits data encryption using a single encryption module in a deterministic method.
-   Multi module - Permits data encryption using multiple encryption modules in a non-deterministic method. Row Conditions is the new and preferred method of applying multiple modules to a field. Row Conditions applies the multi module capability in a deterministic way.

Use the related links to find information on common Field Encryption tasks.

-   **[Create cryptographic module for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/create-PE-cryptographic-module.md)**  
Create a Field Encryption cryptographic module to define the mechanisms used for cryptographic operations.
-   **[Using multiple encryption modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/using-multiple-encryption-modules.md)**  
Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but used to help prevent them from viewing each other's encrypted data.
-   **[Create a cryptographic specification for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/create-crypto-spec-pe.md)**  
After you create a cryptographic module, access the corresponding cryptographic specification to define the algorithm.
-   **[Configure advanced algorithms for Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/adv-algorithm-cleent.md)**  
Create a cryptographic specification to define the algorithm for a cryptographic module. Customize the encryption specifications with advanced options that are available for Field Encryption Enterprise.
-   **[Using customer supplied keys with Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/csk-landing.md)**  
You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.
-   **[Encrypting fields and attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/field-encryption-key-management.md)**  
Once cryptographic modules are created, a security admin can define the encrypted fields configuration \(EFC\) and opt to encrypt a field or attachment on a table.
-   **[Field Encryption Enterprise examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/kmf-walkthroughs-tutorials.md)**  
These examples walk you through the encryption of fields and attachments using customer-supplied keys.

**Parent Topic:**[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/field-encryption.md)

**Related topics**  


[Create cryptographic module for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/create-PE-cryptographic-module.md)

[Create a cryptographic specification for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/create-crypto-spec-pe.md)

[Configure advanced algorithms for Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/adv-algorithm-cleent.md)

[Configure properties for customer-supplied keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/customer-supplied-keys.md)

[Encrypting fields and attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/field-encryption-key-management.md)

[Field Encryption Enterprise examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/kmf-walkthroughs-tutorials.md)

