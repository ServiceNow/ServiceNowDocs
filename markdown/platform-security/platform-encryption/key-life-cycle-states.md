---
title: Key Management Framework key life-cycle states
description: KMF supports several cryptographic key life-cycle states through the enforcement of specific allowable actions. For example, only keys that are in the active state can be used fully for their intended cryptographic purpose. The following table provides further detail on the varying key life-cycle states.
locale: en-US
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Key Management Framework key life-cycle states

KMF supports several cryptographic key life-cycle states through the enforcement of specific allowable actions. For example, only keys that are in the active state can be used fully for their intended cryptographic purpose. The following table provides further detail on the varying key life-cycle states.

<table id="table_om3_f15_1nb"><thead><tr><th>

Key life-cycle state or action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

The active key is used to generate new content, such as encrypting or signing. There can be only one active key for a given cryptographic specification in a cryptographic module.

</td></tr><tr><td>

Compromised

</td><td>

Compromised keys can’t be used to generate new content, such as encrypting or signing, but may still be used to identify the purpose of existing content, such as decryption or verification.

 Several keys can exist in the compromised state for revocation in a given cryptographic specification in a cryptographic module. Any active or suspended key can be moved to a compromised state.

</td></tr><tr><td>

Deactivated

</td><td>

Any active key can be deactivated. There could be several keys in a deactivated state for a given cryptographic specification in a cryptographic module. For example, when the key is rotated, the current active key is deactivated. Deactivated keys cannot be used to generate new content, such as encrypting and signing, but may still be used to identify purposes of existing content, such as decryption or verification.

 **Note:** Compromised and revoked keys are treated as deactivated keys.

</td></tr><tr><td>

Destroyed

</td><td>

When a key is destroyed key material is permanently removed and can no longer be used for any cryptographic purpose. Any deactivated key can be destroyed using lifecycle automation when it hasn’t been used in the configured designated time frame. There could be several keys in a destroyed state for a given cryptographic specification in a cryptographic module.**Warning:** Data associated with a destroyed key can no longer be accessed, therefore extreme caution should be exercised when performing a destroy key action.

</td></tr><tr><td>

Generated

</td><td>

Multiple keys can exist in the generated state for a given cryptographic specification in a cryptographic module. A generated key can be moved to an active state when no active key exists for the given cryptographic specification. The first key generated is automatically set to active.

 **Note:** If the choice is to generate a new key, then a new key is generated and made active even though there are keys in a generated state for the given cryptographic specification.

</td></tr><tr><td>

Renewed

</td><td>

An active key that has an expiration date can be renewed any number of times to extend the life-cycle period of the key.**Note:** The difference between the activation date and expiration date is calculated and the expiration date is postponed by that duration from the current day.

</td></tr><tr><td>

Resume

</td><td>

The UI action is available on suspended keys to move them back to an active state when no other active key exists for the given cryptographic specification.

</td></tr><tr><td>

Revoked

</td><td>

Any active or suspended key can be moved to the revoked state. Revoked keys can’t be used to generate new content, such as encrypting or signing, but may still be used to identify the purpose of existing content, such as for decryption or verification.

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


[Roles installed with Key Management Framework](kmf-roles.md#)

[Module access policy visualization](../concept/map-vis-concept.md)

[Module access policy debugger](../concept/map-debugger.md)

[Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md)

