---
title: Rotate keys
description: For increased security, you can rotate your cryptographic keys on a pre-determined schedule. Key rotation is when you retire an encryption key and replace that old key by generating a new cryptographic key.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/platform-encryption/rotate-cust-supplied-keys.html
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2025-07-31"
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

    \[Omitted image "active-key-selection.png"\] Alt text: Select the active key from the Module Keys tab.

    \[Omitted image "rotatekeys.png"\] Alt text: Lifecycle key form to click Rotate Key.

4.  Select **Rotate Key**.

    The key life-cycle state changes to "Deactivated." The **Last rotated date**, **Deactivation date**, and **Key version** fields update.

5.  Return to **Cryptographic Module** &gt; **** **Module Keys**.

    \[Omitted image "key-rotated.png"\] Alt text: Displays the Module Keys tab with the key lifecycle states updated based on active and deactivated keys.

    There’s an extra module key listed in the table. The newly rotated key becomes "Active" and the last key is "Deactivated."


**Parent Topic:**[Key management actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/key-management-actions.md)

