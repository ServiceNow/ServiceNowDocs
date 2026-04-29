---
title: Using Field Encryption
description: Use Field Encryption to manage access to encrypted data on your instances.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Field Encryption, Encryption]
---

# Using Field Encryption

Use Field Encryption to manage access to encrypted data on your instances.

There are two methods of encrypting field data:

-   Single module - Permits data encryption using a single encryption module in a deterministic method.
-   Multi module - Permits data encryption using multiple encryption modules in a non-deterministic method. Row Conditions is the new and preferred method of applying multiple modules to a field. Row Conditions applies the multi module capability in a deterministic way.

## Field Encryption Experience

The Field Encryption Experience user interface provides a centralized interface for managing Field Encryption modules and configurations. It displays an overview of your encryption configuration, including all modules with their encrypted fields, access policies, and ServiceNow generated keys. You can filter your view and sort displayed data on the Modules and Configurations tabs.

## Modules

Each module tile displays its name, state, and configuration status of the encrypted fields, access policies, and active encryption keys. Selecting the configuration steps allows you to complete the figuration of each. Detailed information can be viewed by selecting the module.![Field Encryption Experience Modules tab](../image/modules-tab.png)

The default module page provides an introductory video that demonstrates how Field Encryption works with keys, access policies, and encrypted fields. Contextual links to resources are provided in the interface for added assistance.

## Configurations

The Configurations tab enables you to find all of your encrypted fields, access policies, and encrypted keys in one place.![Field Encryption Experience Configurations tab](../image/configurations-tab.png)

## What you can do

The Field Encryption Experience provides a guided workflow that enables you to:

-   Create new Field Encryption modules- Initiate configurations for your data security requirements.
-   Add encryption keys- Use guided steps to generate and add encryption keys.
-   Configure encrypted fields- Specify which fields to encrypt through an intuitive selection process.
-   Define Module Access Policies- Control which users and roles can access encrypted data.

## Field Encryption tasks

Use the related links to find information on common Field Encryption tasks.

-   **[Create cryptographic module for Field Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md)**  
Create a Field Encryption cryptographic module to define the mechanisms used for cryptographic operations.
-   **[Using multiple encryption modules](using-multiple-encryption-modules.md)**  
Multiple encryption modules enable data to be encrypted with more than one encryption module. If each module has its own access policy based on a role, for example, users with different roles can encrypt data on the same table but used to help prevent them from viewing each other's encrypted data.
-   **[Create a cryptographic specification for Field Encryption](../../key-management-framework/task/create-crypto-spec-pe.md)**  
After you create a cryptographic module, access the corresponding cryptographic specification to define the algorithm.
-   **[Configure advanced algorithms for Field Encryption Enterprise](../../key-management-framework/task/adv-algorithm-cleent.md)**  
Create a cryptographic specification to define the algorithm for a cryptographic module. Customize the encryption specifications with advanced options that are available for Field Encryption Enterprise.
-   **[Using customer-supplied keys with Field Encryption Enterprise](csk-landing.md)**  
You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.
-   **[Encrypting fields and attachments](field-encryption-key-management.md)**  
Once cryptographic modules are created, a security admin can define the encrypted fields configuration \(EFC\) and opt to encrypt a field or attachment on a table.
-   **[Field Encryption Enterprise examples](../../key-management-framework/concept/kmf-walkthroughs-tutorials.md#)**  
These examples walk you through the encryption of fields and attachments using customer-supplied keys.

**Parent Topic:**[Field Encryption](field-encryption.md)

**Related topics**  


[Create cryptographic module for Field Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md)

[Create a cryptographic specification for Field Encryption](../../key-management-framework/task/create-crypto-spec-pe.md)

[Configure advanced algorithms for Field Encryption Enterprise](../../key-management-framework/task/adv-algorithm-cleent.md)

[Configure properties for customer-supplied keys](customer-supplied-keys.md)

[Encrypting fields and attachments](field-encryption-key-management.md)

[Field Encryption Enterprise examples](../../key-management-framework/concept/kmf-walkthroughs-tutorials.md#)

