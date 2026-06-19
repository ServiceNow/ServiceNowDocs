---
title: Create a cryptographic specification for Column Level Encryption
description: After you create a cryptographic module, access the corresponding cryptographic specification to define the algorithm.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/create-crypto-spec-pe-2.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: task
last_updated: "2026-02-01"
reading_time_minutes: 1
breadcrumb: [Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Create a cryptographic specification for Column Level Encryption

After you create a cryptographic module, access the corresponding cryptographic specification to define the algorithm.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager or sn\_kmf\_admin and security\_admin or admin

## About this task

This procedure describes options that are available with Column Level Encryption with the base system and additional configuration options that become available with Column Level Encryption Enterprise functionality. Column Level Encryption Enterprise functionality is available with a paid subscription. Refer to [Encryption and Key Management subscription bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/encryption-sku.md) for supported features and options available with each offering. See [Activate Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/activate-platform-encryption-2.md) for more information on obtaining Column Level Encryption Enterprise.

A cryptographic specification will be created by the system when you create a cryptographic module for Column Level Encryption Enterprise.

## Procedure

1.  Navigate to **System Security** &gt; **Field Encryption Modules** &gt; **All**.

2.  Select the cryptographic module to open the configuration options.

    Cryptographic module information is displayed at the top of the screen. A Symmetric Data Encryption/Decryption crypto specification is auto-created with an AES 256 CBC algorithm.

3.  Select the crypto specification from the table to open the Algorithm Definition.

    For Column Level Encryption Enterprise see [Configure advanced algorithms for Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/adv-algorithm-cleent-2.md).

4.  Click **Next** to access the Key Lifecycle.


## What to do next

Perform one of the following operations:

-   Select an entry in the Key Lifecycle table to define key lifecycle behavior. See [Configure key lifecycle states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/configure-key-lifecycle-states.md) for details to complete the lifecycle definition for the key.
-   Click **Next** to create a cryptographic key. For details on this process, see [Generate a ServiceNow cryptographic key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/generate_sn_key.md).

**Parent Topic:**[Using Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/using-column-level-encryption-2.md)

