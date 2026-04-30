---
title: Configure field encryption settings to select key type
description: Configure your field encryption settings to use ServiceNow supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Configure field encryption settings to select key type

Configure your field encryption settings to use ServiceNow supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform.

## Before you begin

Customer-supplied keys are only supported with Column Level Encryption Enterprise.

Role required: sn\_kmf.cryptographic\_manager and security\_admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Settings**.

2.  From the Field Encryption Settings, select either **ServiceNow Generated Keys** or **Customer Supplied Keys** from the **Key Source** list.

    ![](../image/field-encryption-settings-choices.png "Key source selection")

    This option changes the `com.glide.encryption.cle_kmf.key_source` property to either **ServiceNow Generated Keys** or **Customer Supplied Keys**.

3.  Select **Save**.


## What to do next

-   If you’re using your own customer-supplied keys, see [Using customer supplied keys with Column Level Encryption Enterprise](../../encryption/concept/csk-landing.md).
-   If you’re using ServiceNow supplied keys, start creating your cryptographic module. See [Create a cryptographic module](create-cryptographic-module.md).

**Parent Topic:**[Key Management Framework Reference](../concept/understanding-kmf.md)

**Related topics**  


[Cryptographic module overview](../concept/crypto-module-overview.md)

[Module access policy overview](../concept/module_access_policy_overview.md)

[Instance level keys in the Key Management Framework](../reference/instance-level-keys.md)

[Cryptographic specification](../concept/cryptographic-purpose.md)

[Key Management Framework key lifecycle states](../reference/key-life-cycle-states.md)

[Roles installed with Key Management Framework](../reference/kmf-roles.md#)

[Create a cryptographic module](create-cryptographic-module.md)

[Create a module access policy](create-module-access-policy.md)

[Module access policy visualization](../concept/map-vis-concept.md)

[Module access policy debugger](../concept/map-debugger.md)

[Create a cryptographic module life-cycle policy](create-cryptographic-module-lifecycle-policy.md)

