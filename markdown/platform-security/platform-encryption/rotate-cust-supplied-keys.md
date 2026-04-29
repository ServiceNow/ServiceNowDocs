---
title: Rotate keys
description: For increased security, you can rotate your cryptographic keys on a pre-determined schedule. Key rotation is when you retire an encryption key and replace that old key by generating a new cryptographic key.
locale: en-US
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Key management actions, Key Management Framework, Encryption]
---

# Rotate keys

For increased security, you can rotate your cryptographic keys on a pre-determined schedule. Key rotation is when you retire an encryption key and replace that old key by generating a new cryptographic key.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## About this task

Encryption modules, unlike encryption contexts, support a rekey of records for re-encryption with a new key. The following demonstrates how to perform a key rotation operation manually on a cryptographic module.

## Procedure

1.  Navigate to **Key Management** &gt; **Cryptographic Modules** &gt; **All**.

2.  Select the cryptographic module for key rotation.

3.  On the **Module Keys** tab, select the Active key.

    ![Select the active key from the Module Keys tab.](../../key-management-framework/image/active-key-selection.png "Select the active key")

    ![Lifecycle key form to click Rotate Key.](../../key-management-framework/image/rotatekeys.png)

4.  Select **Rotate Key**.

    The key life-cycle state changes to "Deactivated." The **Last rotated date**, **Deactivation date**, and **Key version** fields update.

5.  Return to **Cryptographic Module** &gt; **** **Module Keys**.

    ![Displays the Module Keys tab with the key lifecycle states updated based on active and deactivated keys.](../../key-management-framework/image/key-rotated.png)

    There’s an extra module key listed in the table. The newly rotated key becomes "Active" and the last key is "Deactivated."


**Parent Topic:**[Key management actions](../../key-management-framework/reference/key-management-actions.md)

