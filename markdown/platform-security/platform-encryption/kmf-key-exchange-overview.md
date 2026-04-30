---
title: Key Management Framework Key Exchange
description: KMF Key Exchange is a subset function of KMF Resource Exchange. Key Exchange securely transfers encrypted data across multiple instances.
locale: en-US
release: yokohama
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2025-02-26"
reading_time_minutes: 2
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Key Management Framework Key Exchange

KMF Key Exchange is a subset function of KMF Resource Exchange. Key Exchange securely transfers encrypted data across multiple instances.

## Overview of Key Exchange

Key Exchange securely transfers keys across instances.

KMF Key Exchange provides a secure way for customers to exchange KMF keys between instances. One application use case is the data cloning process. With Key Exchange, crypto module keys are copied over during the data cloning of KMF components. Cryptographic modules, module key specifications, and module access policies are included in the cloning process. Transfer of keys isn’t included.

This functionality is included with the Key Management Framework, which is included in the ServiceNow AI Platform Encryption subscription bundle. For details on this product, see [Key Management Framework](../../encryption/concept/encryption.md).

## Using Key Exchange

Administrators who use KMF for Field Encryption can use Key Exchange to clone the keys between production instances when performing data cloning. In data cloning, the administrator/ KMF cryptographic manager can perform the following:

-   Exchange all keys to the other instances.
-   Exchange particular keys one time or periodically to the other instance.
-   Send on-demand requests from the target instance to the key source instance.
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
|Manual \(person in the loop\)|The administrator sends an on-demand request on the target instance to the source. The request must be approved by an administrator on the key source instance.|
|Rekey \(automated request\)|The administrator selects the option of rekey during the cloning setup process.|

**Parent Topic:**[Key Management Framework Resource Exchange](resource-exchange.md)

