---
title: Key Management Framework
description: Use the Key Management Framework \(KMF\) to generate, exchange, store, use, and replace the cryptographic keys used to encrypt and decrypt sensitive data on your ServiceNow instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Encryption]
---

# Key Management Framework

Use the Key Management Framework \(KMF\) to generate, exchange, store, use, and replace the cryptographic keys used to encrypt and decrypt sensitive data on your ServiceNow instance.

Key Management refers to the activities involved in handling your cryptographic keys and related security parameters during the key's life cycle. Key Management Framework is based on [National Institute of Standards and Technology \(NIST\) 800-57](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-57pt1r5.pdf) guidelines. In accordance with these guidelines, you can use KMF to:

-   Assign dedicated roles for cryptographic management and operations, auditing, and integration.
-   Create cryptographic modules to configure of cryptographic specifications for unique cryptographic purposes and key types.
    -   Symmetric key: encryption and decryption, key wrapping and unwrapping, and authentication
    -   Asymmetric key: digital signature generation and verification, encryption and decryption, key wrapping and unwrapping
-   Manage your key life cycle to generate, rotate, revoke, and suspend keys, including support of several key life cycle states
-   Create module access policies \(MAPs\) to enforce access controls, to grant access only to users and scripts that you choose.
-   Protect your cryptographic keys with the Federal Information Processing Standard \(FIPS\) 140-2-L3 hardware Root of Trust \(RoT\), Public Key Infrastructure \(PKI\), key hierarchy, and envelope encryption.
-   Assign the auditing role to users to can then view auditing information such as key usage statistics.

## Get started

<table id="table_y4x_cxd_nzb" class="nav-card"><tbody><tr><td>

Exploring the Key Management Framework![](../../../reuse/icons/brand-icons/bus-explore.svg)

 Learn about the components of the Key Management Framework, and how to use them to manage how cryptographic operations are performed on your instance.

</td><td>

Configuring the Key Management Framework![](../../../reuse/icons/brand-icons/bus-sdlc.svg)

 Create and maintain Key Management components to customize and manage how cryptographic operations are performed on your ServiceNow instance.

</td><td>

[Key Management Framework Reference![](../../../reuse/icons/brand-icons/bus-case-study.svg)](../../key-management-framework/concept/understanding-kmf.md)

 [Review additional Key Management reference materials](../../key-management-framework/concept/understanding-kmf.md)

</td></tr><tr><td>

 

</td><td>

[Key Management Framework actions![](../../../reuse/icons/brand-icons/bus-optimize-manage.svg)](../../key-management-framework/reference/key-management-actions.md)

 [One of the core features of KMF is to provide the capability  to manage  keys, such as revoking or rotating keys.  KMF properly secures sensitive data with the most up-to-date encryption materials and life cycle operations.](../../key-management-framework/reference/key-management-actions.md)

</td><td>

 

</td></tr></tbody>
</table>## Activation information

The ServiceNow Platform Encryption subscription bundle is a group commercial entitlement that includes Key Management Framework, Field Encryption Enterprise, Cloud Encryption, and Database Encryption.

Field Encryption Enterprise is the unlimited license of Field Encryption. The Field Encryption Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](../reference/encryption-sku.md).

**Note:** KMF doesn’t support domain separation, but can be used with on-premise instances.

-   **[Encryption and Key Management subscription bundle](../reference/encryption-sku.md)**  
With Key Management, Column Level Encryption is upgraded at no additional charge to include highly configurable encryption modules. You can also optionally upgrade to the unlimited-use license. Subscribe to the new encryption entitlement bundle, Platform Encryption, which includes Column Level Encryption Enterprise and Cloud Encryption.
-   **[Key Management Framework Reference](../../key-management-framework/concept/understanding-kmf.md)**  
The Key Management Framework \(KMF\) API/UX lets you fully customize and manage how cryptographic operations are performed on your ServiceNow instance. The ServiceNow Key Management Framework provides a secure and comprehensive interface for instance-side cryptographic key management services.
-   **[Key management actions](../../key-management-framework/reference/key-management-actions.md)**  
One of the core features of KMF is to provide the capability  to manage  keys, such as revoking or rotating keys.  KMF properly secures sensitive data with the most up-to-date encryption materials and life cycle operations.
-   **[Import a key from a web service](../../key-management-framework/concept/import-key-webservice-1.md#)**  
Securely upload an external customer key onto your instance using import a key from a web service \(for example the key REST API\). Both symmetric and asymmetric public keys can be imported into a targeted KMF cryptographic module.
-   **[Key Management Framework Health](../../key-management-framework/task/kmf_diagnostics.md)**  
Access on-demand health status information for the Key Management Framework. Warning and malfunction errors contain a detailed message.
-   **[Prepare your instance for GlideEncrypter deprecation](../../key-management-framework/task/check-3des.md)**  
Use an instance scan script to find and remove GlideEncrypter API calls on your instance. Removing these calls is a necessary step in deprecating 3DES encryption on your instance.
-   **[Deprecate GlideEncrypter usage of 3DES for password2 fields](../../key-management-framework/concept/password2-3des-deprecation.md)**  
Deprecate GlideEncrypter usage of 3DES encryption standard on your instance ensure that your instance uses the more secure Advanced Encryption Standard \(AES\) exclusively for the encryption and decryption of your Password2 data.
-   **[Key Management Framework Resource Exchange](../../key-management-framework/reference/resource-exchange.md)**  
ServiceNow® Resource Exchange is a KMF feature that gives you the capability to exchange resources between instances in a secure manner.
-   **[Infrastructure Security](../../key-management-framework/concept/infrastructure-security.md)**  
Use Infrastructure security tools to create, upload, and manage certificates your instance uses to encrypt traffic from client to server.
-   **[Password2 encryption with the Key Management Framework \(KMF\)](../../key-management-framework/concept/password-2way-encrypted-fields.md)**  
Supported by the Key Management Framework, use the Password2 \(2-way encrypted\) field type to encrypt and decrypt custom fields with segregation of duties, key protection, and life-cycle management. It works in accordance with NIST 800-57 guidelines and provides FIPS 140-2-L3 protection.

**Parent Topic:**[Encryption](../../security/concept/encryption-landing.md)

