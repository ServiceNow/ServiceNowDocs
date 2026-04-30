---
title: Key management for Edge Encryption
description: You are responsible for providing and managing the encryption keys used by Edge Encryption.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Edge Encryption, Edge Encryption, Encryption]
---

# Key management for Edge Encryption

You are responsible for providing and managing the encryption keys used by Edge Encryption.

This topic refers to keys for the Edge Encryption product. If you are looking for information on the Key Management Framework, which can be used with Field Encryption, see [Key Management Framework](../../key-management-framework/concept/understanding-kmf.md).

When obtaining and creating encryption keys to support the encryption types used by Edge Encryption, consider the following:

-   Whether to use AES 128-bit or AES 256-bit. You must define a default AES 128-bit encryption key, even if it is not used.
-   Whether to use file system, Java KeyStore, or Enterprise Key Management \(EKM\).
-   When to rotate encryption keys.
-   When and if to use a mass encryption job to re-encrypt data using the new key.

Before removing a key from the proxy configuration files and the keystore, it is critical that you decrypt all data on the instance that uses the key. You can do this by adding a new encryption key and scheduling a mass key rotation job.

## Keystores

Edge Encryption supports the following types of key storage.

-   **File store**

    Keys are stored in a file in a file system that is accessible by the Edge Encryption proxy. Encryption keys stored in a file are not encrypted, so it is your responsibility to protect these files.

-   **Java KeyStore**

    Keys are stored in Java's JCEKS KeyStore. A Java KeyStore is protected by a password, so it is more secure than storing keys in a file in the file store. A single Java KeyStore can store multiple keys, and the keys are identified by a key alias, making it easier to manage multiple keys.

-   **Enterprise Key Management \(EKM\)**

    Keys are stored and retrieved with the SafeNet KeySecure or Unbound Technology key management systems.


The Edge Encryption proxy ships with the Java JCEKS KeyStore file named `keystore.jceks` in the `keystore` directory. This keystore file contains the ServiceNow public key used to validate encryption rules signed by ServiceNow.

**Note:** If using a keystore other than the base system Java JCEKS KeyStore, you must import the ServiceNow public key into your keystore. The public key alias is **servicenow**.

In addition to the encryption keys, the Java JCEKS KeyStore is used to store the RSA key pair for digitally signing the encryption configuration and encryption rules that are stored in the instance, and the digital certificate that the Edge Encryption proxy uses to establish a secure connection with the browsers and any other clients.

-   **[SafeNet key versioning for Edge Encryption](safenet-key-versioning.md)**  
Use SafeNet key versioning to simplify changing keys. Instead of creating an alias for every new key, SafeNet key versioning keeps the same alias and increments the version.

**Parent Topic:**[Exploring Edge Encryption](c_EdgeEncryptionOverview.md)

