---
title: Run mass encryption or decryption
description: You can run mass encryption on encryption configurations, as well as a mass decryption to decrypt previously encrypted values.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Encrypting fields and attachments, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Run mass encryption or decryption

You can run mass encryption on encryption configurations, as well as a mass decryption to decrypt previously encrypted values.

## Before you begin

Role required: security\_admin

## About this task

You can also create scheduled jobs for mass encryption and decryption. See [Schedule mass encryption, decryption, and rekeying jobs](schedule-mass-jobs.md) for instructions.

Mass encryption and decryption are available only when an encrypted field configuration uses the single cryptographic module. Mass decryption is available for both the single and multiple encryption methods,.

**Note:** You should run mass encryption and decryption only during non-peak hours because the operations are resource and time intensive.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations**.

2.  Open the encrypted field configuration for the field you would like to mass encrypt or decrypt.

3.  Under Related Links, select an available option.

    -   **Schedule Mass Decryption job**
    -   **Schedule Mass Encryption job**
4.  Confirm your selection in the dialog.


## Result

If running a mass encryption, all values are encrypted with the encryption module defined in the encrypted field configuration record. If running a mass decryption, only fields encrypted with an encryption module you have access to are decrypted.

**Parent Topic:**[Encrypting fields and attachments](../concept/field-encryption-key-management.md)

