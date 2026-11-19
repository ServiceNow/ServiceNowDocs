---
title: Key Management Framework Key Exchange
description: Key Management Framework \(KMF\) Key Exchange securely transfers cryptographic keys from a source instance to a target instance, most commonly during data cloning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/kmf-key-exchange-overview.html
release: brazil
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 2
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Key Management Framework Key Exchange

Key Management Framework \(KMF\) Key Exchange securely transfers cryptographic keys from a source instance to a target instance, most commonly during data cloning.

## Overview of Key Exchange

Key Exchange transfers keys from one instance to another. It's most commonly used during data cloning and replication. You can also use it after you manually export encrypted data between instances, so you can decrypt that data on the target.

KMF Key Exchange provides a secure way for you to exchange KMF keys between instances. With Key Exchange, crypto module keys are copied over during the data cloning of KMF components. Cryptographic modules, module key specifications, and module access policies are included in the cloning process.

This functionality is included with the Key Management Framework, which is included in the ServiceNow AI Platform Encryption subscription bundle. For details on this product, see [Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/encryption.md).

## Using Key Exchange

Administrators who use KMF, including Field Encryption, can use Key Exchange to transfer keys from one instance to another, most often during data cloning. The administrator or KMF cryptographic manager can perform the following:

-   Exchange all keys to the other instances.
-   Exchange particular keys one time or periodically to the other instance.
-   Send ad hoc requests from the target instance to the key source instance.
-   Exchange keys from source to target for rekeying ciphertext.
    -   Manage the expiration time of the request with the ability to delete keys or reject the key exchange request if the request has expired.
    -   After the request is completed and the key is imported, the used key will be set as expired and timestamped.
    -   Rekey ciphertext on the target instance that was encrypted with keys from the source.

## Supported modes

Key Exchange supports several modes on the encryption module crypto specification level:

|Mode|Description|
|----|-----------|
|Automatic \(no configuration, default behavior\)|All keys are sent over automatically during the data cloning process without additional configuration.|
|Configurable \(one-time configuration setup\)|The administrator configures the keys to be sent over during the data cloning process.|
|Manual \(person in the loop\)|The administrator sends an ad hoc request on the target instance to the source. The request must be approved by an administrator on the key source instance.|
|Rekey \(automated request\)|The administrator selects the option of rekey during the cloning setup process.|

**Parent Topic:**[Key Management Framework Resource Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/resource-exchange.md)

