---
title: Configure field encryption settings to select key type
description: Configure your field encryption settings to use ServiceNow supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform.
locale: en-US
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Key Management Framework, Key Management Framework, Encryption]
---

# Configure field encryption settings to select key type

Configure your field encryption settings to use ServiceNow supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform.

## Before you begin

Customer-supplied keys are only supported with Field Encryption Enterprise.

Role required: sn\_kmf.cryptographic\_manager and security\_admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Settings**.

2.  From the Field Encryption Settings, select either **ServiceNow Generated Keys** or **Customer Supplied Keys** from the **Key Source** list.

    ![](../image/field-encryption-settings-choices.png "Key source selection")

    This option changes the `com.glide.encryption.cle_kmf.key_source` property to either **ServiceNow Generated Keys** or **Customer Supplied Keys**.

3.  Select **Save**.


## What to do next

-   If you’re using your own customer-supplied keys, see [Using customer-supplied keys with Field Encryption Enterprise](../../encryption/concept/csk-landing.md).
-   If you’re using ServiceNow supplied keys, start creating your cryptographic module. See [Create a cryptographic module](create-cryptographic-module.md).

**Parent Topic:**[Configuring the Key Management Framework](../../encryption/concept/configure-kmf.md)

