---
title: Configuring the Key Management Framework
description: Create and maintain Key Management components to customize and manage how cryptographic operations are performed on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/configure-kmf.html
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Key Management Framework, Encryption]
---

# Configuring the Key Management Framework

Create and maintain Key Management components to customize and manage how cryptographic operations are performed on your ServiceNow instance.

-   **[Assign Key Management Framework roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/assign-kmf-roles.md)**  
Administrators with the security\_admin role can assign Key Management Framework \(KMF\) admins, who in turn can assign other Key Management Framework roles.
-   **[Configure field encryption settings to select key type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/configure-field-encryption-settings.md)**  
Configure your field encryption settings to use ServiceNow supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform.
-   **[Create a cryptographic module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/create-cryptographic-module.md)**  
Create a cryptographic module to define the mechanisms used for cryptographic operations. After you create the module, you create a cryptographic specification, where you define an algorithm for encryption and generates a key.
-   **[Create a module access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/create-module-access-policy.md)**  
Create module access policies to decide which users and scripts can access data encrypted by a cryptographic module.
-   **[Create a cryptographic module life-cycle policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/create-cryptographic-module-lifecycle-policy.md)**  
Create a cryptographic module life-cycle policy to place limits on cryptographic modules, such as how long the key is good for. Create policies to safeguard cryptographic modules by limiting their exposure.

**Parent Topic:**[Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/encryption.md)

