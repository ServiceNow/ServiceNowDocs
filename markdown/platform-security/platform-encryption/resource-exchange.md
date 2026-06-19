---
title: Key Management Framework Resource Exchange
description: ServiceNow Resource Exchange is a KMF feature that gives you the capability to exchange resources between instances in a secure manner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/platform-encryption/resource-exchange.html
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Key Management Framework, Encryption]
---

# Key Management Framework Resource Exchange

ServiceNow® Resource Exchange is a KMF feature that gives you the capability to exchange resources between instances in a secure manner.

## Terminology

When using the Resource Exchange, reference the following terminology:

|Name|Description|
|----|-----------|
|Resource Exchange|The process to exchange resources across instances.|
|Key Exchange \(KE\)|The process to exchange keys over instances.|
|Key Source instance \(Key Source\)|The instance that owns the keys.|
|Key Target instance \(Key Target\)|The instance that requests the keys.|

## Overview

Resource Exchange utilizes the KMF cryptographic APIs to provide confidentiality, integrity, authentication, and non-repudiation. Currently, Resource Exchange supports the Key Exchange functionality. See [Key Management Framework Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/kmf-key-exchange-overview.md) for additional information.

-   **[Key Management Framework Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/kmf-key-exchange-overview.md)**  
KMF Key Exchange is a subset function of KMF Resource Exchange. Key Exchange securely transfers encrypted data across multiple instances.
-   **[Configure Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/configure-key-exchange.md)**  
Key Management Framework \(KMF\) generates automatic key exchange requests for supported cryptographic modules during the fresh installation or upgrade of the instance, and manages the data encryption key locally for the instance.
-   **[Rekey ciphertext with Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/rekey-keyexchange.md)**  
Resource Exchange supports rekeying of ciphertext on the target instance that was encrypted with keys from the source. Rekey activity is tracked in the key life-cycle.
-   **[Recurring Key Exchange walkthrough](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/key-exchange-walkthrough.md)**  
Use this walkthrough to set up a recurring key exchange in your instance using and Resource Exchange.

**Parent Topic:**[Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/encryption.md)

