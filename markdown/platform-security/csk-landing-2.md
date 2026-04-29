---
title: Using customer supplied keys with Column Level Encryption Enterprise
description: You can use your own customer-supplied key instead of using the ServiceNow system-generated keys.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Using customer supplied keys with Column Level Encryption Enterprise

You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.

**Important:** These topics only apply instances using Column Level Encryption Enterprise, which is only available with the com.glide.now.platform.encryption plugin. See [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption-2.md) for more information on obtaining this plugin.

With Column Level Encryption Enterprise you can use your own keys for encryption. Administrators have the choice to use ServiceNow® supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform.

**Important:** To make use of the customer supplied key option, you must have your own cryptographic key.

Once you have your key, you can being using it on your instances by following these steps.

-   **1. [Configure properties for customer-supplied keys](customer-supplied-keys.md)**

    There are three system properties which define the size, padding algorithm, and validity period of the wrapping RSA key pair. Review these properties and adjust their values if the defaults to not fit your needs.

-   **2. [Wrap your customer-supplied key](../task/wrap-customer-supplied-key.md)**

    Use a cryptographic tool to wrap your key like OpenSSL to wrap the symmetric key to use for encryption with the downloaded public key.

-   **[Configure and upload your customer supplied key](../../key-management-framework/task/upload-customer-supplied-key.md)**

    Upload your wrapped your customer supplied key and configure cryptographic module to begin using your key for encryption on your instance.


-   **[Configure properties for customer-supplied keys](customer-supplied-keys.md)**  
If the Field Encryption Enterprise plugin is enabled, you can use system properties to define key padding, ephemeral key pair size, and a key validity period of your customer-supplied keys.
-   **[Wrap your customer-supplied key](../task/wrap-customer-supplied-key.md)**  
Wrap the symmetric key to use for encryption with the downloaded public key.
-   **[Configure and upload your customer supplied key](../../key-management-framework/task/upload-customer-supplied-key.md)**  
You can use your own customer-supplied key instead of using the ServiceNow® system-generated keys.

**Parent Topic:**[Using Column Level Encryption](using-column-level-encryption-2.md)

