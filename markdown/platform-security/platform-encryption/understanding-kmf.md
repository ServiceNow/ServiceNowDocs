---
title: Key Management Framework Reference
description: The Key Management Framework \(KMF\) API/UX lets you fully customize and manage how cryptographic operations are performed on your ServiceNow instance. The ServiceNow Key Management Framework provides a secure and comprehensive interface for instance-side cryptographic key management services.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Key Management Framework, Encryption]
---

# Key Management Framework Reference

The Key Management Framework \(KMF\) API/UX lets you fully customize and manage how cryptographic operations are performed on your ServiceNow instance. The ServiceNow Key Management Framework provides a secure and comprehensive interface for instance-side cryptographic key management services.

-   **[Key Management Framework key lifecycle states](../reference/key-life-cycle-states.md)**

    KMF supports several cryptographic key life-cycle states through the enforcement of specific allowable actions. For example, only keys that are in the active state can be used fully for their intended cryptographic purpose. The following table provides further detail on the varying key life-cycle states.

-   **[Roles installed with Key Management Framework](../reference/kmf-roles.md#)**

    The Key Management Framework \(KMF\) introduces specific roles for cryptographic module and key management-related configurations.

-   **[Module access policy visualization](map-vis-concept.md)**

    Use module access policy visualization to view all relevant cryptographic module information on a single UI page.

-   **[Module access policy debugger](map-debugger.md)**

    Use the module access policy debugger to review logging information and understand why your users are or aren’t granted access to an encryption context.

-   **[Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md)**

    With key management, Column Level Encryption is upgraded at no additional charge to the highly configurable encryption modules. You also have the option to upgrade to the unlimited-use license. Subscribe to the new encryption entitlement bundle, Platform Encryption, which includes Column Level Encryption Enterprise and Cloud Encryption.


-   **[Cryptographic module overview](crypto-module-overview.md)**  
Cryptographic modules are the centerpiece of \(KMF\). They define the specific cryptographic mechanisms used for cryptographic operations for a given use case.
-   **[Module access policy overview](module_access_policy_overview.md)**  
Module access policies \(MAPs\) are access controls that you apply to your cryptographic modules. Use these access policies to decide which users and scripts can access data encrypted by a cryptographic module.
-   **[Instance level keys in the Key Management Framework](../reference/instance-level-keys.md)**  
The Key Management Framework \(KMF\) architecture introduces a key structure built with security in mind. Using a Hardware Security Module \(HSM\), KMF uses envelope encryption to ensure that all platform keys under KMF management are protected through a chain of keys. Customer Data Encryption Keys \(CDEKs\) created by KMF are also included.
-   **[Cryptographic specification](cryptographic-purpose.md)**  
The Cryptographic specification is the component that defines aspects of your cryptographic module, including its cryptographic purpose and which encryption algorithm to use.
-   **[Key Management Framework key lifecycle states](../reference/key-life-cycle-states.md)**  
KMF supports several cryptographic key lifecycle states through the enforcement of specific allowable actions. For example, only keys that are in the active state can be used fully for their intended cryptographic purpose. The following table provides further detail on the varying key lifecycle states.
-   **[Roles installed with Key Management Framework](../reference/kmf-roles.md#)**  
The Key Management Framework \(KMF\) introduces specific roles for cryptographic module and key management-related configurations.
-   **[Configure field encryption settings to select key type](../task/configure-field-encryption-settings.md)**  
Configure your field encryption settings to use ServiceNow supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform.
-   **[Create a cryptographic module](../task/create-cryptographic-module.md)**  
Create a cryptographic module to define the mechanisms used for cryptographic operations. After you create the module, you create a cryptographic specification, where you define an algorithm for encryption and generates a key.
-   **[Create a module access policy](../task/create-module-access-policy.md)**  
Create module access policies to decide which users and scripts can access data encrypted by a cryptographic module.
-   **[Module access policy visualization](map-vis-concept.md)**  
Use module access policy visualization to view all relevant cryptographic module information on a single UI page.
-   **[Module access policy debugger](map-debugger.md)**  
Use the module access policy debugger to review logging information and understand why your users are or aren’t granted access to an encryption context.
-   **[Create a cryptographic module life-cycle policy](../task/create-cryptographic-module-lifecycle-policy.md)**  
Create a cryptographic module life-cycle policy to place limits on cryptographic modules, such as how long the key is good for. Create policies to safeguard cryptographic modules by limiting their exposure.

**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

