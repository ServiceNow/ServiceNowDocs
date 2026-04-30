---
title: Create module lifecycle policy exceptions
description: Create a module policy exception to change the lifecycle policy of a key at the module level for an instance. The exception\(s\) applies only to that module and not to the entire instance. For example, if the administrator configured symmetric keys to be limited to one year at the instance level, an exception can be made at the module level to be two years.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a cryptographic module life-cycle policy, Key Management Framework Reference, Key Management Framework, Encryption]
---

# Create module lifecycle policy exceptions

Create a module policy exception to change the lifecycle policy of a key at the module level for an instance. The exception\(s\) applies only to that module and not to the entire instance. For example, if the administrator configured symmetric keys to be limited to one year at the instance level, an exception can be made at the module level to be two years.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager and sn\_kmf.admin

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Cryptographic Modules** **All**.

2.  Select the cryptographic module that will use the policy exceptions.

3.  In the Cryptographic Module table, select the **Module Policy Exceptions** tab.

4.  Click **New**.

5.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Crypto Module|Read only, name of the module selected.|
    |Applies to|The specified key is auto-populated.|
    |Key Type|Select the key type, as the exception policies are related to a specific key. Multiple exception policies can be created per crypto module.|
    |Policy condition|Choose the qualifying conditions from the drop-down and complete the additional constraint criteria.|
    |New criteria|Select additional policy conditions, as required.|
    |Result|Select to **Reject** to reject usage of the key or **Track** to allow usage of it when the criteria is met.|

6.  Click **Submit** to be returned to the Cryptographic Module table.


**Parent Topic:**[Create a cryptographic module life-cycle policy](create-cryptographic-module-lifecycle-policy.md)

