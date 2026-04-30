---
title: Key Management Framework key lifecycle states
description: KMF supports several cryptographic key lifecycle states through the enforcement of specific allowable actions. For example, only keys that are in the active state can be used fully for their intended cryptographic purpose. The following table provides further detail on the varying key lifecycle states.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Key Management Framework key lifecycle states

KMF supports several cryptographic key lifecycle states through the enforcement of specific allowable actions. For example, only keys that are in the active state can be used fully for their intended cryptographic purpose. The following table provides further detail on the varying key lifecycle states.

<table id="table_om3_f15_1nb"><thead><tr><th>

Key lifecycle state or action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

There can be only one active key for a given cryptographic specification in a cryptographic module.

</td></tr><tr><td>

Compromised

</td><td>

Several keys can exist in the compromised state for revocation in a given cryptographic specification in a cryptographic module. Any active or suspended key can be moved to a compromised state. Compromised keys cannot be used to generate new content, such as encrypting or signing, but may still be used to identify the purpose of existing content, such as decryption or verification.

</td></tr><tr><td>

Deactivated

</td><td>

Any active key can be deactivated. There could be several keys in a deactivated state for a given cryptographic specification in a cryptographic module. For example, when the key is rotated, the current active key is deactivated. Deactivated keys cannot be used to generate new content, such as encrypting and signing, but may still be used to identify purposes of existing content, such as decryption or verification.

 **Note:** Compromised and revoked keys are treated as deactivated keys.

</td></tr><tr><td>

Destroyed

</td><td>

When a key is destroyed key material is permanently removed and can no longer be used for any cryptographic purpose. Any deactivated key can be destroyed using lifecycle automation when it has not been used in the configured designated time frame. There could be several keys in a destroyed state for a given cryptographic specification in a cryptographic module.**Warning:** Data associated with a destroyed key can no longer be accessed, therefore extreme caution should be exercised when performing a destroy key action.

</td></tr><tr><td>

Generated

</td><td>

Multiple keys can exist in the generated state for a given cryptographic specification in a cryptographic module. A generated key can be moved to an active state when no active key exists for the given cryptographic specification. The first key generated is automatically be set to active.

 **Note:** If the choice is to generate a new key, then a new key is generated and made active even though there are keys in a generated state for the given cryptographic specification.

</td></tr><tr><td>

Renewed

</td><td>

An active key that has an expiration date can be renewed any number of times to extend the lifecycle period of the key.**Note:** The difference between the activation date and expiration date is calculated and the expiration date is postponed by that duration from the current day.

</td></tr><tr><td>

Resume

</td><td>

The UI action is available on suspended keys to move them back to an active state when no other active key exists for the given cryptographic specification.

</td></tr><tr><td>

Revoked

</td><td>

Any active or suspended key can be moved to the revoked state. Revoked keys cannot be used to generate new content, such as encrypting or signing, but may still be used to identify the purpose of existing content, such as for decryption or verification.

 Several keys in a revoked state may exist for a given cryptographic specification in a cryptographic module.

</td></tr><tr><td>

Rotated

</td><td>

Key rotation results in deactivating the current active key and making another key active. Select the new active key from the following:-   Generation of a new key.
-   Point to an existing imported key. Any active key can be rotated.

</td></tr><tr><td>

Suspended

</td><td>

There could be several keys in the suspended state for a given cryptographic specification in a cryptographic module. When the key is suspended, the key can be resumed and reassigned to an active state when no other active key exists for that cryptographic specification.

</td></tr></tbody>
</table>**Parent Topic:**[Key Management Framework Reference](../concept/understanding-kmf.md)

**Related topics**  


[Cryptographic module overview](../concept/crypto-module-overview.md)

[Module access policy overview](../concept/module_access_policy_overview.md)

[Instance level keys in the Key Management Framework](instance-level-keys.md)

[Cryptographic specification](../concept/cryptographic-purpose.md)

[Roles installed with Key Management Framework](kmf-roles.md#)

[Configure field encryption settings to select key type](../task/configure-field-encryption-settings.md)

[Create a cryptographic module](../task/create-cryptographic-module.md)

[Create a module access policy](../task/create-module-access-policy.md)

[Module access policy visualization](../concept/map-vis-concept.md)

[Module access policy debugger](../concept/map-debugger.md)

[Create a cryptographic module life-cycle policy](../task/create-cryptographic-module-lifecycle-policy.md)

