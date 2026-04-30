---
title: View declined cryptographic module usage requests
description: View cryptographic modules that rejected encryption requests made by scripts because of unsupported encryption mechanisms.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure script access to encrypted data, Script access for cryptographic modules, Encrypting fields and attachments, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# View declined cryptographic module usage requests

View cryptographic modules that rejected encryption requests made by scripts because of unsupported encryption mechanisms.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## About this task

Cryptographic modules can support one or more encryption purposes, such as Asymmetric Data Decryption and Symmetric Data Decryption. Encrypted data can only be accessed based on the module access policy. If a script tries to use a cryptographic module for a purpose not defined in the module, the script cannot access to the encrypted data.

In the following example, a cryptographic purpose was assigned to a cryptographic module, but a key was never generated for it.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Module Key Policies** &gt; **** **Module Key Rejections**.

    A list of cryptographic modules that rejected requests displays along with the encryption key used in the corresponding script.

    ![Crypto modules that rejected requests.](../image/policyrejection.png "Module Key Rejections")

    **Note:** If a different script attempts to use the same cryptographic module using the same key type, the value for **Last enforced** updates. Another row does not generate.

    In this example, at 2020-02-10\_15:55:17, the first module rejected a request because module1's key is compromised. At 2020-02-10\_07:24:05, the second module rejected a request because the second module's key is suspended.

    To grant scripts permission to use the encryption module the next time they run, create a module access policy for script encryption. For more information, refer to [Configure script access to encrypted data](configure-script-encryption.md).


**Parent Topic:**[Configure script access to encrypted data](configure-script-encryption.md)

