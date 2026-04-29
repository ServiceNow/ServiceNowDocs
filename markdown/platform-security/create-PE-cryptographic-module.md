---
title: Create cryptographic module for Field Encryption
description: Create a Field Encryption cryptographic module to define the mechanisms used for cryptographic operations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Field Encryption, Field Encryption, Encryption]
---

# Create cryptographic module for Field Encryption

Create a Field Encryption cryptographic module to define the mechanisms used for cryptographic operations.

## Before you begin

Role required: security\_admin  and sn\_kmf.cryptographic\_manager  or sn\_kmf.admin

## About this task

This procedure describes options that are available with Field Encryption with the base system and additional configuration options that become available with Field Encryption Enterprise functionality. Field Encryption Enterprise is available with a paid subscription. Refer to [Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md) for supported features and options available with each offering. See [Activate Field Encryption](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Field Encryption Enterprise.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Experience** &gt; **Create new module**.

2.  Enter the module name and select the algorithm.

    ![image.fe-create-crypto-module]

3.  Select **Create**.

4.  Click **Submit**.

    After submitting successfully, your cryptographic module is listed in the Field Encryption modules overview.

    **Warning:**

    -   **For legacy encryption support users:**

        If you're using the non-enterprise version of Field Encryption, you're limited to five fields. If you've exceeded this limit, you receive the following warning:

        This insertion exceeds the number of published fields limit for Field Encryption  entitled with the Subscription Product. The Enterprise subscription for Field Encryption is required for additional fields. Please reach out to your Account team.

    A default cryptographic specification is created with the crypto purpose set to Symmetric Data Encryption/Decryption and the algorithm as AES 256 CBC. Select the algorithm for updates.

5.  To open the configuration options, click the newly created cryptographic module.

    **Note:** A maximum of five Field Encryption fields are allowed before upgrading to Field Encryption Enterprise. An error message displays and you are prevented from adding additional cryptographic modules. ![Error message for maximum modules created in FEE.](../../encryption/image/cle_limits-modules.png)


## Result

After submitting successfully, your cryptographic module is listed on the Field Encryption modules overview page of Field Encryption Experience.

**Warning:**

-   **For legacy encryption support users:**

    If you're using the non-enterprise version of Field Encryption, you're limited to five fields. If you've exceeded this limit, you receive the following warning:

    This insertion exceeds the number of published fields limit for Field Encryption  entitled with the Subscription Product. The Enterprise subscription for Field Encryption is required for additional fields. Please reach out to your Account team.


## What to do next

To open the configuration options, click the newly created cryptographic module.

**Note:** A maximum of five Field Encryption fields are allowed before upgrading to Field Encryption Enterprise. A message displays at the top stating the allowance and the number of encrypted fields that you currently have is listed. Once that maximum allowance is met, the **Create new** button is grayed out and you are prevented from adding additional cryptographic modules. ![image.fe-efc-limit]

[Create a cryptographic specification for Field Encryption](create-crypto-spec-pe.md).

**Parent Topic:**[Using Field Encryption](../../encryption/concept/using-column-level-encryption.md)

