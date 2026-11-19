---
title: Key Management Framework Resource Exchange
description: ServiceNow Resource Exchange is a KMF feature that gives you the capability to exchange resources between instances in a secure manner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/resource-exchange.html
release: brazil
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2026-09-10"
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

Resource Exchange utilizes the KMF cryptographic APIs to provide confidentiality, integrity, authentication, and non-repudiation. Currently, Resource Exchange supports the Key Exchange functionality. See [Key Management Framework Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/kmf-key-exchange-overview.md) for additional information.

-   **[Key Management Framework Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/kmf-key-exchange-overview.md)**  
Key Management Framework \(KMF\) Key Exchange securely transfers cryptographic keys from a source instance to a target instance, most commonly during data cloning.
-   **[Configure key exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/configure-key-exchange.md)**  
Key Management Framework \(KMF\) generates automatic key exchange requests for supported cryptographic modules during installation or upgrade. It manages the data encryption key locally for the instance.
-   **[Rekey ciphertext with Key Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/rekey-keyexchange.md)**  
Resource Exchange supports rekeying of ciphertext on the Key Target instance that was encrypted with keys from the Key Source instance. Rekey activity is tracked in the key life-cycle.
-   **[Recurring Key Exchange walkthrough](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/key-exchange-walkthrough.md)**  
Use this walkthrough to set up a recurring key exchange in your instance using Resource Exchange.

**Parent Topic:**[Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/encryption.md)

