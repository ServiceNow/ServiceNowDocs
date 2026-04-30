---
title: Create cryptographic module for Field Encryption
description: Create a Column Level Encryption cryptographic module to define the mechanisms used for cryptographic operations.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Field Encryption, Field Encryption, Encryption]
---

# Create cryptographic module for Field Encryption

Create a Column Level Encryption cryptographic module to define the mechanisms used for cryptographic operations.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager or sn\_kmf\_admin, security\_admin, admin

## About this task

This procedure describes options that are available with Field Encryption with the base system and additional configuration options that become available with Field Encryption Enterprise functionality. Field Encryption Enterprise is available with a paid subscription. Refer to [Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md) for supported features and options available with each offering. See [Activate Field Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Field Encryption Enterprise.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Column Level Encryption Modules** &gt; **New**.

    ![Shows new crypto module form for Field Encryption Enterprise.](../image/pe-cryptomodule.png)

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Module name|Alphanumeric string to be referenced when running scripts.|
    |Crypto spec template|Default template used to create the cryptographic module that contains mappings of many crypto purposes to crypto specifications and recommended algorithms.|
    |Application|The selected application scope.|
    |Name|Encryption module name is prepended with application scope name to avoid conflict with other scoped applications on module creation. For example, if you created a module with the name `my_crypto_module` in the global application scope, the name is saved as `global.my_crypto_module`.|
    |Crypto module lifecycle state|The term lifecycle refers to the creation, use, and deactivation of a cryptographic module. Set to **Draft** initially during configuration. When using the module, set to **Published**. The Default template is automatically set to **Published**.|
    |Parent crypto module|The parent is populated automatically as **column\_level\_encryption**.|

3.  Click **Submit**.

    After submitting successfully, your cryptographic module is listed in the Cryptographic Modules table.

    **Warning:**

    -   **For legacy encryption support users:**

        If you're using the non-enterprise version of Field Encryption, you're limited to five modules. If you've exceeded this limit, you receive the following warning:

        This insertion exceeds the number of published modules limit for Field Encryption  entitled with the Subscription Product. The Enterprise subscription for Field Encryption is required for additional modules. Please reach out to your Account team.

    A default cryptographic specification is created with the crypto purpose set to Symmetric Data Encryption/Decryption and the algorithm as AES 256 CBC. Select the algorithm for updates.

4.  To open the configuration options, click the newly created cryptographic module.

    **Note:** A maximum of five Field Encryption modules are allowed before upgrading to Field Encryption Enterprise. An error message displays and you are prevented from adding additional cryptographic modules. ![Error message for maximum modules created in FEE.](../../encryption/image/cle_limits-modules.png)


## What to do next

[Create a cryptographic specification for Field Encryption](create-crypto-spec-pe.md).

**Parent Topic:**[Using Field Encryption](../../encryption/concept/using-column-level-encryption.md)

