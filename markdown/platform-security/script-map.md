---
title: Script access for cryptographic modules
description: Scripts can be run to access a cryptographic module policy for a cryptographic purpose.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Encrypting fields and attachments, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Script access for cryptographic modules

Scripts can be run to access a cryptographic module policy for a cryptographic purpose.

For Key Management Framework, policies can be based scripts. When an access policy is triggered for script access, the backend script can execute the module policy actions from the script.

Cryptographic modules can support one or more encryption purposes, such as Asymmetric Data Decryption and Symmetric Data Decryption. Each cryptographic purpose requires the generation of an encryption key and defined cryptographic purpose.

Consider the following when executing an encryption script request:

-   The referenced cryptographic purpose must be defined in the cryptographic module.
-   An active generated key must exist for the cryptographic module.
-   The Module Access Policy type must be set to **script**.

## Check script version

When creating a module access policy that is set to the script type, there is an option available to validate the integrity of the script version being accessed. Only the assigned version of the script is allowed access to the encryption modules. When the **Check script version** check box is selected in the module access policy, anytime the script is run, the system performs a version comparison. If the script has been changed, the user is notified.

![Shows the check script version checkbox in a module access policy.](../image/check-script-version.png "Check script version check box")

-   **[Configure script access to encrypted data](../task/configure-script-encryption.md)**  
Execute a script to run the cryptographic module policy for a cryptographic purpose. Specific read \(decrypt/unwrap\) or write \(encrypt, wrap\) access can be defined based on the module access policy operation granularity.

**Parent Topic:**[Encrypting fields and attachments](../../encryption/concept/field-encryption-key-management.md)

