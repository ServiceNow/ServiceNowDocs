---
title: Module access policy overview
description: Module access policies \(MAPs\) are access controls that you apply to your cryptographic modules. Use these access policies to decide which users and scripts can access data encrypted by a cryptographic module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/module\_access\_policy\_overview.html
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring the Key Management Framework, Key Management Framework, Encryption]
---

# Module access policy overview

Module access policies \(MAPs\) are access controls that you apply to your cryptographic modules. Use these access policies to decide which users and scripts can access data encrypted by a cryptographic module.

## Module access policies

**Note:** A subscription is required to utilize the Field Encryption Enterprise functionality. See [Activate Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/activate-platform-encryption.md) for more information on Field Encryption Enterprise.

Module access policies are introduced with the Key Management Framework \(KMF\) in the base system.

Module access policies expand on the role-based designations that were provided with the encryption modules. Module access policies can be based on the following:

-   Basic \(scope\)
-   Role
-   System user
-   Script
-   Resource Exchange

    **Note:** See [Key Management Framework Resource Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/resource-exchange.md) for details.


In a cryptographic module, you must configure the correct module access policies to permit access to encrypted data. Without a module access policy associated with a cryptographic module, encrypted data isn’t visible to users and associated fields and columns in lists display as empty.

In this example, the absence of a module access policy on the encrypted Short Description field hides the content from all users accessing the Incident table. With a module access policy in place, only users with a specific role are able to see the encrypted data.

\[Omitted image "encryption-field-configuration-example.png"\] Alt text: Data with and without module access policies.

**Note:** The data in the column also appears empty to users without the correct role specified in the module access policy.

Refer to [Create a module access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/create-module-access-policy.md) for setup.

## Autogen policies

Autogen policies are automatically system generated based on the default module access policy defined for the given cryptographic module. If there are no granular level policies defined when the system or a script tries to access the given cryptographic module, these global policies are generated and applied.

**Important:**

Autogen policy rules aren’t applied for scheduled jobs types, or field encryption modules \(modules where the parent module is Field Encryption\).

**Parent Topic:**[Exploring the Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/explore-kmf.md)

