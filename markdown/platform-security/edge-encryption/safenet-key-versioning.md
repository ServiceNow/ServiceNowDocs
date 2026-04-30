---
title: SafeNet key versioning for Edge Encryption
description: Use SafeNet key versioning to simplify changing keys. Instead of creating an alias for every new key, SafeNet key versioning keeps the same alias and increments the version.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Key management for Edge Encryption, Exploring Edge Encryption, Edge Encryption, Encryption]
---

# SafeNet key versioning for Edge Encryption

Use SafeNet key versioning to simplify changing keys. Instead of creating an alias for every new key, SafeNet key versioning keeps the same alias and increments the version.

You must set up key versioning in SafeNet before you can configure SafeNet key versioning on the Edge proxy server.

**Note:** Edge proxies installed before the London release support SafeNet keys, but do not support SafeNet key versioning. If you mistakenly use a versioned key on a Kingston or earlier proxy, when you upgrade to a London or later release, the London or later proxy detects this problem, and to prevent potential data loss the proxy does not start.

You must first schedule a mass key rotation job or a single key rotation job to replace the old SafeNet versioned key with a non-versioned key, and then create a new SafeNet versioned key, if needed. This new versioned key is safe to use with the London or later proxy, and you can restart the proxy.

## Encryption key configuration

If using SafeNet versioned keys, the Change Default Keys section of the Encryption Key Configuration form includes new fields for the **Key version** of the default 128-bit and 256-bit keys. **Key version** fields are grayed out and cannot be edited.

![Change default keys, Key version](../images/safenet-key-versioning.png)

For procedures, see [Configure encryption keys on the instance](../task/t_RotateEncryptionKeys.md).

## Versioned keys

If using SafeNet versioned keys, when you navigate to **Edge Encryption Configuration** &gt; **Encryption Key Configuration** &gt; **All Keys**, versioned keys include the **Key version**.

![Versioned keys, Key version](../images/versioned-keys.png)

A version number does not appear for the initial entries you make in the Change Default Keys section of the Encryption Key Configuration form. When the proxy server requests a key from SafeNet, the system adds a new line for the alias and adds the **Key version**.

In the above example, **AES128key** is listed three times:

-   The first listing, with no **Key version** indicated, is the initial entry.
-   The second listing, with **1** in the **Key version** column, is the first version of the key returned from SafeNet.
-   The third listing, with **2** in the **Key version** column, is the second version of the key returned from SafeNet.
-   As other versions of the key are returned from SafeNet, new lines are added to record the **Key version** now in use.

**Parent Topic:**[Key management for Edge Encryption](c_EncryptionKeyManagement.md)

