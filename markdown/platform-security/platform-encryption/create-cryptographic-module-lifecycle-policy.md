---
title: Create a cryptographic module life-cycle policy
description: Create a cryptographic module life-cycle policy to place limits on cryptographic modules, such as how long the key is good for. Create policies to safeguard cryptographic modules by limiting their exposure.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Create a cryptographic module life-cycle policy

Create a cryptographic module life-cycle policy to place limits on cryptographic modules, such as how long the key is good for. Create policies to safeguard cryptographic modules by limiting their exposure.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## About this task

A cryptographic module life-cycle policy is an instance-level policy. The more exposure that a cryptographic key has, the more likely it can be compromised. Safeguard keys by limiting how long the keys can be used and who can use them.

The following features govern cryptographic modules:

-   Instance policies set boundaries for the instance. For example, if you specify in an instance policy that the expiration date should never be more than two years after the activation date, you can’t use the life-cycle rules to set an expiration date five years after the activation date.

-   Instance life-cycle templates enable you to set different policies for different keys. Templates offer default life-cycle rules for cryptographic modules so that they don't have to be re-created for every module. For example, you can set different expiration dates for symmetric data encryption keys than for public key wrapping keys.

-   Life-cycle rules affect the keys directly. For example, if you specify in the life-cycle rules that the expiration date should be two years after the activation date, keys will expire two years after the activation date.


## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Lifecycle Policies** &gt; **Instance Policies**.

2.  Select **New**.

3.  Complete the form.

    Cryptographic Life-cycle Policies fields

    |Field|Description|
    |-----|-----------|
    |Applies to|Read only. The key that the life cycle applies to.|
    |Active|Select to activate the policy.|
    |Policy condition|Conditional statements that specify when to activate, renew, deactivate, and destroy the cryptographic module.|
    |Result|**Reject** to revoke access to the cryptographic module, or **Track** to permit access and monitor use of the cryptographic module.|


## What to do next

If you want to add exceptions to this life-cycle policy at the module level, see [Create module lifecycle policy exceptions](create-module-policy-exceptions.md).

-   **[Create module lifecycle policy exceptions](create-module-policy-exceptions.md)**  
Create a module policy exception to change the lifecycle policy of a key at the module level for an instance. The exception\(s\) applies only to that module and not to the entire instance. For example, if the administrator configured symmetric keys to be limited to one year at the instance level, an exception can be made at the module level to be two years.

**Parent Topic:**[Key Management Framework Reference](../concept/understanding-kmf.md)

**Related topics**  


[Cryptographic module overview](../concept/crypto-module-overview.md)

[Module access policy overview](../concept/module_access_policy_overview.md)

[Instance level keys in the Key Management Framework](../reference/instance-level-keys.md)

[Cryptographic specification](../concept/cryptographic-purpose.md)

[Key Management Framework key lifecycle states](../reference/key-life-cycle-states.md)

[Roles installed with Key Management Framework](../reference/kmf-roles.md#)

[Configure field encryption settings to select key type](configure-field-encryption-settings.md)

[Create a cryptographic module](create-cryptographic-module.md)

[Create a module access policy](create-module-access-policy.md)

[Module access policy visualization](../concept/map-vis-concept.md)

[Module access policy debugger](../concept/map-debugger.md)

