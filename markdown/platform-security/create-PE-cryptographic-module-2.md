---
title: Create cryptographic module for Column Level Encryption
description: Create a Column Level Encryption cryptographic module to define the mechanisms used for cryptographic operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/create-PE-cryptographic-module-2.html
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

This procedure describes options that are available with Column Level Encryption with the base system and additional configuration options that become available with Column Level Encryption Enterprise functionality. Column Level Encryption Enterprise is available with a paid subscription. Refer to [Encryption and Key Management subscription bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/encryption-sku.md) for supported features and options available with each offering. See [Activate Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/activate-platform-encryption-2.md) for more information on obtaining Column Level Encryption Enterprise.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Modules** &gt; **New**.

    \[Omitted image "parent-crypto-module.png"\] Alt text: Shows new crypto module form for Column Level Encryption Enterprise.

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

    **Note:** A maximum of five Column Level Encryption fields are allowed before upgrading to Column Level Encryption Enterprise. An error message displays and you are prevented from adding additional cryptographic modules. \[Omitted image "cle\_limits-modules.png"\] Alt text: Error message for maximum modules created in FEE.


## What to do next

[Create a cryptographic specification for Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/create-crypto-spec-pe-2.md).

**Parent Topic:**[Using Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/using-column-level-encryption-2.md)

