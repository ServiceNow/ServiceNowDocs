---
title: Rekey ciphertext with Key Exchange
description: Resource Exchange supports rekeying of ciphertext on the Key Target instance that was encrypted with keys from the Key Source instance. Rekey activity is tracked in the key life-cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/rekey-keyexchange.html
release: brazil
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Key Management Framework Resource Exchange, Key Management Framework, Encryption]
---

# Rekey ciphertext with Key Exchange

Resource Exchange supports rekeying of ciphertext on the Key Target instance that was encrypted with keys from the Key Source instance. Rekey activity is tracked in the key life-cycle.

## How rekeying works with Key Exchange

Rekey means re-encrypting data so that it is protected by a new key instead of the key it was originally encrypted with. Ciphertext is data in its encrypted form, which can't be read without the key used to encrypt it. For background on how instances exchange keys, see [Key Management Framework Resource Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/resource-exchange.md).

Administrators who use KMF, including Field Encryption, can use Key Exchange to rekey cryptographic keys between the Key Source instance and the Key Target instance when performing data cloning.

You create the request in the Resource Exchange Request form.

An active key must first be available on the Key Target instance for rekey. Rekey requires an active key.

The system automatically creates and runs an encryption job to rotate and rekey the key from the Key Source instance and re-encrypt the ciphertext.

Use Key Exchange to do the following:

-   Rekey request expiration
    -   Request: The rekey request is created in the Resource Exchange Request form.
    -   Expiration: Set an expiration time frame for rekey.
    -   Outcome: If the request has expired, then the request is rejected and the key is deleted.
-   Automate rekeying ciphertext that was encrypted with keys from the Key Source instance.

    A new cloned crypto key is used to re-encrypt ciphertext on the Key Target instance.

-   The Rekey purpose is set up during the cloning process and is automated as part of the clone.
-   Rekey activity is tracked on the **Modules Key** tab of the cryptographic module. Access the Key life cycle state and Key version for key activity. See [Rotate keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/rotate-cust-supplied-keys.md) for additional information.

Configure a Key Exchange and select the **Enable Rekeying After Key Imported** check box for activation. See [Configure key exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/configure-key-exchange.md) for details.

\[Omitted image "rekey-res-exchange.png"\] Alt text: Select the Enable Rekeying After Key Imported check box.

**Parent Topic:**[Key Management Framework Resource Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/platform-encryption/resource-exchange.md)

