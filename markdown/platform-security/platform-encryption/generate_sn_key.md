---
title: Generate a ServiceNow cryptographic key
description: Follow this procedure to upload and configure a ServiceNow cryptographic key to encrypt sensitive data.
locale: en-US
release: yokohama
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a cryptographic module, Configuring the Key Management Framework, Key Management Framework, Encryption]
---

# Generate a ServiceNow cryptographic key

Follow this procedure to upload and configure a ServiceNow cryptographic key to encrypt sensitive data.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## About this task

Cryptographic managers have the choice to use ServiceNow supplied keys or their own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform with Field Encryption Enterprise. For information on CSK, see [Configure properties for customer-supplied keys](../../encryption/concept/customer-supplied-keys.md).

## Procedure

1.  Set field encryption settings to use ServiceNow Generated Keys.

    See [Configure field encryption settings to select key type](configure-field-encryption-settings.md) for details.

2.  Navigate to **Key Management** &gt; **Cryptographic Modules** &gt; **All**.

3.  Select the corresponding cryptographic module to open the Cryptographic Module details page.

4.  Select the row for the key alias entry on the Crypto Specifications tab.

    If a key hasn’t yet been generated, the key alias field is empty.

5.  Select **Next** to navigate to the Key Origin tab of the Crypto Specification components.

    The Lifecycle Definition tab displays along with the Key Lifecycle table and can be reviewed or edited. See [Configure key lifecycle states](configure-key-lifecycle-states.md) for details.

6.  Select **Servicenow** in the Origin field.![Servicenow key origin in the crypto spec.](../image/cryptospec-sn-keyorigin.png)

    This field varies based on the field encryption settings from Step 1 and the algorithm selected. To use an imported key, see [Import the wrapping / unwrapping key pair](../concept/import-key-webservice-1.md#). See [Configure properties for customer-supplied keys](../../encryption/concept/customer-supplied-keys.md) if you’re using your own key.

7.  Enter a friendly name for the Key alias.

8.  Select **Next** to move to the Key Creation tab.

9.  Select **Generate Key**.

    After you generate the key, the Cryptographic Module form reloads displaying the cryptographic specification.

10. Select the **Module Keys** tab to view the keys.

    Secure information for the key is stored on the Module Keys tab along with the number of keys that exist for the cryptographic specification.

    ![Shows the Module Keys tab and the generated keys in the table.](../image/module-keys.png)

11. Select a key to perform key management actions.

    See [Key management actions](../reference/key-management-actions.md) for details.


**Parent Topic:**[Create a cryptographic module](create-cryptographic-module.md)

