---
title: Create cryptographic module for Column Level Encryption
description: Create a Column Level Encryption cryptographic module to define the mechanisms used for cryptographic operations.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-02-01"
reading_time_minutes: 2
breadcrumb: [Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Create cryptographic module for Column Level Encryption

Create a Column Level Encryption cryptographic module to define the mechanisms used for cryptographic operations.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager or sn\_kmf\_admin, security\_admin, admin

## About this task

This procedure describes options that are available with Column Level Encryption with the base system and additional configuration options that become available with Column Level Encryption Enterprise functionality. Column Level Encryption Enterprise is available with a paid subscription. Refer to [Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md) for supported features and options available with each offering. See [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption-2.md) for more information on obtaining Column Level Encryption Enterprise.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Modules** &gt; **New**.

    ![Shows new crypto module form for Column Level Encryption Enterprise.](../../encryption/image/parent-crypto-module.png)

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

        If you're using the non-enterprise version of Column Level Encryption, you're limited to five fields. If you've exceeded this limit, you receive the following warning:

        This insertion exceeds the number of published fields limit for Column Level Encryption  entitled with the Subscription Product. The Enterprise subscription for Column Level Encryption is required for additional ields. Please reach out to your Account team.

    A default cryptographic specification is created with the crypto purpose set to Symmetric Data Encryption/Decryption and the algorithm as AES 256 CBC. Select the algorithm for updates.

4.  To open the configuration options, click the newly created cryptographic module.

    **Note:** A maximum of five Column Level Encryption fields are allowed before upgrading to Column Level Encryption Enterprise. An error message displays and you are prevented from adding additional cryptographic modules. ![Error message for maximum modules created in FEE.](../../encryption/image/cle_limits-modules.png)


## What to do next

[Create a cryptographic specification for Column Level Encryption](create-crypto-spec-pe-2.md).

**Parent Topic:**[Using Column Level Encryption](../../encryption/concept/using-column-level-encryption-2.md)

