---
title: Instance level keys in the Key Management Framework
description: The Key Management Framework \(KMF\) architecture introduces a key structure built with security in mind. Using a Hardware Security Module \(HSM\), KMF uses envelope encryption to ensure that all platform keys under KMF management are protected through a chain of keys. Customer Data Encryption Keys \(CDEKs\) created by KMF are also included.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Instance level keys in the Key Management Framework

The Key Management Framework \(KMF\) architecture introduces a key structure built with security in mind. Using a Hardware Security Module \(HSM\), KMF uses envelope encryption to ensure that all platform keys under KMF management are protected through a chain of keys. Customer Data Encryption Keys \(CDEKs\) created by KMF are also included.

At the instance level, KMF defines several keys that are used internally for varying cryptographic purposes throughout the ServiceNow AI Platform.

Envelope encryption is the practice of encrypting a key with another key. The following figure provides an example of the envelope encryption. Here, CDEKs are envelope encrypted by the IKEK, which in turn is envelope encrypted by the IRK, which is finally envelope encrypted by the RK. Since the IRK can only be accessed by the HSM, the IKEK must be uploaded for decryption.

This table provides examples of a subset of available customer/app keys that are managed and protected by KMF.

<table id="table_kd1_j5s_1nb"><thead><tr><th>

Key

</th><th>

Location

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Root Key \(RK\)

</td><td>

Hardware Security Model \(HSM\)

</td><td>

Root key used to decrypt the IRK.

</td></tr><tr><td>

Instance Root Key \(IRK\)

</td><td>

HSM

</td><td>

A key unique to your instance that is used to envelope-encrypt several instance internal keys.

</td></tr><tr><td>

Instance HMAC Key \(IHK\)

</td><td>

Instance

</td><td>

Unique per instance, the IHK is used internally for Hash-Based Message Authentication Code \(HMAC\) purposes. The IHK helps to ensure the authenticity and integrity of module keys and is wrapped on either KeySecure or the File Key Store.

</td></tr><tr><td>

Instance Key Encryption Key \(IKEK\)

</td><td>

Instance

</td><td>

The IKEK wraps the module keys and is wrapped on either KeySecure or the File Key Store.

</td></tr><tr><td>

Instance Asymmetric Encryption Key \(IAEK\)

</td><td>

Instance

</td><td>

A key unique to your instance that is used internally for asymmetric encryption purposes.The IAEK is used to transmit confidential messages between an instance during Key Exchange or Instance Data Replication consumer approval.

</td></tr><tr><td>

Instance Signature Key \(ISK\)

</td><td>

Instance

</td><td>

A key unique to your instance that is used internally for signing purposes.

</td></tr><tr><td>

Password2 \(PW2\)

</td><td>

Instance

</td><td>

With KMF, the key for PW2 fields is fully managed by KMF.

</td></tr><tr><td>

Customer Data Encryption Key \(CDEK\)

</td><td>

Instance

</td><td>

Encryption keys created through KMF are envelope-encrypted by the IKEK.

</td></tr><tr><td>

Instance Data Replication \(IDR\) Data Encryption Key \(DEK\)

</td><td>

Instance

</td><td>

Specific encryption keys used for the IDR process.

</td></tr></tbody>
</table>**Parent Topic:**[Key Management Framework Reference](../concept/understanding-kmf.md)

**Related topics**  


[Cryptographic module overview](../concept/crypto-module-overview.md)

[Module access policy overview](../concept/module_access_policy_overview.md)

[Cryptographic specification](../concept/cryptographic-purpose.md)

[Key Management Framework key lifecycle states](key-life-cycle-states.md)

[Roles installed with Key Management Framework](kmf-roles.md#)

[Configure field encryption settings to select key type](../task/configure-field-encryption-settings.md)

[Create a cryptographic module](../task/create-cryptographic-module.md)

[Create a module access policy](../task/create-module-access-policy.md)

[Module access policy visualization](../concept/map-vis-concept.md)

[Module access policy debugger](../concept/map-debugger.md)

[Create a cryptographic module life-cycle policy](../task/create-cryptographic-module-lifecycle-policy.md)

