---
title: View and manage keys
description: Review the status of any key to determine further key action, such as when to renew, rotate, suspend, deactivate, or destroy a current key.
locale: en-US
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Key management actions, Key Management Framework, Encryption]
---

# View and manage keys

Review the status of any key to determine further key action, such as when to renew, rotate, suspend, deactivate, or destroy a current key.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Cryptographic Modules** &gt; **** **All**.

2.  Select a cryptographic module.

    The Cryptographic Module &lt;module-name&gt; form appears.

3.  On the Module Keys tab, select the key alias to review the key status on the life cycle &lt;key name&gt; form.

4.  Review the form, as all fields are read-only.

    |Field|Description|
    |-----|-----------|
    |Generation date|Displays the date when the key was generated.|
    |Activation date|Displays the date when the key was activated.|
    |Last renewal date|Displays the date when the key was last renewed.|
    |Last rotated date|Displays the date when the key was last rotated.|
    |Deactivation date|Displays the date when the key was deactivated.|
    |Destruction date|Displays the date when the key was destroyed.|
    |Key life-cycle state|Displays the key life-cycle state.|
    |Future activation date|Displays the future key activation date.|
    |Future renewal date|Displays the future key renewal date.|
    |Future rotation date|Displays the future date for key rotation.|
    |Future destruction date|Displays the future date when the key is destroyed.|
    |Expiration date|Displays the date when the key expires.|

5.  To perform an action on the key, select one of the following to take effect immediately:

    **Note:** These actions can only be performed for custom Cryptographic Modules, not for base system Cryptographic Modules.

    -   **Revoke Key**: Select to deactivate the key and generate a new key. Enter the reason why you’re revoking the key.
    -   **Rotate Key**: Select to deactivate the current key and to generate a new key in its place. The new key is listed in the Module Key table and the Key Version number increments by 1. See for details.

    -   **Suspend Key**: Select to deactivate the current key.
    -   **Resume Key**: Select to mark a suspended key as the active key. This option is only available after the active key has been suspended.

**Parent Topic:**[Key management actions](../reference/key-management-actions.md)

