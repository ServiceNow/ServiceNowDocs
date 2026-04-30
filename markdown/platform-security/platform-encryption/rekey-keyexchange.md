---
title: Rekey ciphertext with Key Exchange
description: Resource Exchange supports rekeying of ciphertext on the target instance that was encrypted with keys from the source. Rekey activity is tracked in the key life-cycle.
locale: en-US
release: yokohama
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Rekey ciphertext with Key Exchange

Resource Exchange supports rekeying of ciphertext on the target instance that was encrypted with keys from the source. Rekey activity is tracked in the key life-cycle.

## Overview

Administrators who use KMF for Field Encryption can use Key Exchange to rekey cryptographic keys between production instances when performing data cloning. An active key must first be available on the target instance for rekey, as rekey requires an active key. An encryption job is automatically created and run by the system to rotate and rekey the source key and re-encrypt the ciphertext.

Use Key Exchange to do the following:

-   Set an expiration time frame for rekey.

    If the request has expired, then the request is rejected and the key is deleted.

-   Automate rekeying ciphertext that was encrypted with keys from source instances.

    A new cloned crypto key is used to re-encrypt ciphertext on the target instance.

-   The Rekey purpose is set up during the cloning process and is automated as part of the clone.
-   Rekey activity is tracked on the **Modules Key** tab of the cryptographic module. Access the Key life cycle state and Key version for key activity. See [Rotate keys](../../encryption/task/rotate-cust-supplied-keys.md) for additional information.

Configure a Key Exchange and select the **Enable Rekeying After Key Imported** check box for activation. See [Configure Key Exchange](../task/configure-key-exchange.md) for details.

![Select the Enable Rekeying After Key Imported check box.](../image/rekey-res-exchange.png)

**Parent Topic:**[Key Management Framework Resource Exchange](resource-exchange.md)

