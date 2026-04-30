---
title: Create a cryptographic module
description: Create a cryptographic module to define the mechanisms used for cryptographic operations. After you create the module, you create a cryptographic specification, where you define an algorithm for encryption and generates a key.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Create a cryptographic module

Create a cryptographic module to define the mechanisms used for cryptographic operations. After you create the module, you create a cryptographic specification, where you define an algorithm for encryption and generates a key.

## Before you begin

If you're supplying your own keys, go to [Configure and upload your customer supplied key](upload-customer-supplied-key.md).

Role required: sn\_kmf.cryptographic\_manager

## About this task

This procedure describes options that are available with KMF in the ServiceNow platform base system. Column Level Encryption Enterprise functionality is available only when the com.glide.now.platform.encryption plugin is active. See [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Column Level Encryption Enterprise. See [Create cryptographic module for Column Level Encryption](create-PE-cryptographic-module.md).

**Note:** Cryptographic module \[sys\_kmf\_crypto\_module\] records can't be deleted.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Cryptographic Modules** &gt; **Create New**.

2.  On the form, fill in the fields:

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Module name

</td><td>

Alphanumeric string to be referenced when running scripts.

</td></tr><tr><td>

Crypto spec template

</td><td>

Select the **Default** template to use to create the cryptographic module, as it contains mappings of supported algorithms for crypto specifications.

</td></tr><tr><td>

Default module access policy value

</td><td>

-   Rely on system default:
-   Reject
-   Track


</td></tr><tr><td>

Actual module access policy result

</td><td>

Reject or track, based on the default policy value or the value selected during the creation of the module access policy.

</td></tr><tr><td>

Name

</td><td>

Crypto module name prepended with application scope name.

</td></tr><tr><td>

Crypto module life-cycle state

</td><td>

Life cycle refers to the creation, use, and deactivation of a cryptographic module. Set to **Draft** initially during configuration. When using the module, set this field to **Published**. The Default template is automatically set to Published.

</td></tr></tbody>
</table>3.  Select **Submit**.

    **Warning:**

    -   **For legacy encryption support users:**

        If you're using the non-enterprise version of Column Level Encryption, you're limited to five modules. If you've exceeded this limit, you receive the following warning:

        This insertion exceeds the number of published modules limit for Column Level Encryption entitled with the Subscription Product. The Enterprise subscription for Column Level Encryption is required for additional modules. Please reach out to your Account team.

    After submitting successfully, your cryptographic module is listed in the Cryptographic Modules table. The system prepends the name with the scope to avoid conflict with other scoped applications. For example, if you created a module with the name `my_crypto_module` in the global application scope, the name is saved as `global.my_crypto_module`.


## What to do next

[Create a cryptographic specification](create-crypto-spec.md)

.

-   **[Create a cryptographic specification](create-crypto-spec.md)**  
After you create a cryptographic module, create a cryptographic specification to define the module algorithms.
-   **[Configure key lifecycle states](configure-key-lifecycle-states.md)**  
After you have created a cryptographic specification, you can configure the lifecycle actions for the keys in your instance.
-   **[Generate a ServiceNow cryptographic key](generate_sn_key.md)**  
Follow this procedure to upload and configure a ServiceNow cryptographic key to encrypt sensitive data.

**Parent Topic:**[Key Management Framework Reference](../concept/understanding-kmf.md)

**Related topics**  


[Cryptographic module overview](../concept/crypto-module-overview.md)

[Module access policy overview](../concept/module_access_policy_overview.md)

[Instance level keys in the Key Management Framework](../reference/instance-level-keys.md)

[Cryptographic specification](../concept/cryptographic-purpose.md)

[Key Management Framework key lifecycle states](../reference/key-life-cycle-states.md)

[Roles installed with Key Management Framework](../reference/kmf-roles.md#)

[Configure field encryption settings to select key type](configure-field-encryption-settings.md)

[Create a module access policy](create-module-access-policy.md)

[Module access policy visualization](../concept/map-vis-concept.md)

[Module access policy debugger](../concept/map-debugger.md)

[Create a cryptographic module life-cycle policy](create-cryptographic-module-lifecycle-policy.md)

