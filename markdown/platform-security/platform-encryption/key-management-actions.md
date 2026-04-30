---
title: Key management actions
description: One of the core features of KMF is to provide the capability  to manage  keys, such as revoking or rotating keys.  KMF properly secures sensitive data with the most up-to-date encryption materials and life cycle operations.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Key Management Framework, Encryption]
---

# Key management actions

One of the core features of KMF is to provide the capability  to manage  keys, such as revoking or rotating keys.  KMF properly secures sensitive data with the most up-to-date encryption materials and life cycle operations.

The following table provides a summary of the key life cycle operations and management actions. The cryptographic module purpose is applied to the data with the cryptographic module configuration and has no impact on data.

<table id="table_mvb_drb_smb"><thead><tr><th>

Key management action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate key 

</td><td>

Generates  a  new key for the given  cryptographic module. A first generated key is set to `active`. 

</td></tr><tr><td>

Rotate key 

</td><td>

Deactivates  the current  key and  generates a new  one. The  new  module key is set to current  \(active\). 

</td></tr><tr><td>

Revoke key

</td><td>

Marks  the current key  and life cycle state as revoked. The cryptographic module auto-generates a new key on new data and sets the key status to active. Revoked means that the key is no longer used for encryption. However, it can still be used for decryption. You can’t destroy a key.

</td></tr><tr><td>

Suspend key

</td><td>

Marks  the current key as suspended.  Manually  resume the suspended  key or revoke  the suspended key to generate  a new module key before using the cryptographic module again.

</td></tr><tr><td>

Resume key

</td><td>

Marks a suspended key as the active key.

</td></tr><tr><td>

Renew key

</td><td>

Extends the life of the current key. The **Renew** button becomes available under the following circumstances:-   You’re assigned the cryptographic manager role.
-   The life-cycle state is marked to either **Active** or **Renewed**.
-   An expiration date is set in the module life cycle definition.

</td></tr></tbody>
</table>-   **[View and manage keys](../task/view-manage-keys.md)**  
Review the status of any key to determine further key action, such as when to renew, rotate, suspend, deactivate, or destroy a current key.
-   **[Rotate keys](../../encryption/task/rotate-cust-supplied-keys.md)**  
For increased security, you can rotate your cryptographic keys on a pre-determined schedule. Key rotation is when you retire an encryption key and replace that old key by generating a new cryptographic key.

**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

