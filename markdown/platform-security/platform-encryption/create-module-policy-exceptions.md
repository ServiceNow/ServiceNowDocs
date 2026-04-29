---
title: Create module life-cycle policy exceptions
description: Create a module policy exception to change the life-cycle policy of a key only for a specific on one instance.
locale: en-US
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a cryptographic module life-cycle policy, Configuring the Key Management Framework, Key Management Framework, Encryption]
---

# Create module life-cycle policy exceptions

Create a module policy exception to change the life-cycle policy of a key only for a specific on one instance.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager and sn\_kmf.admin

Exceptions apply only to that module and not to the entire instance. For example, an administrator configured symmetric keys to be limited to one year at the instance level. An exception can be made at the module level to be two years.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Cryptographic Modules** **All**.

2.  Select the cryptographic module that will use the policy exceptions.

3.  In the Cryptographic Module table, select the **Module Policy Exceptions** tab.

4.  Select **New**.

5.  Complete the form.

<table id="table_etj_ygn_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Crypto Module

</td><td>

Name of the module selected. This field is read only.

</td></tr><tr><td>

Applies to

</td><td>

Specified key is auto-populated.

</td></tr><tr><td>

Key Type

</td><td>

Key type that the exception policies are related to. **Note:** You may only select a single key type, but multiple exception policies can be created per cryptographic module.

</td></tr><tr><td>

Policy condition

</td><td>

Customizable condition which determines when the policy exception applies.

</td></tr><tr><td>

Result

</td><td>

The result that occurs when the condition in the **Policy Condition** field is met.-   **Reject** rejects usage of the key.
-   **Track** allows the key to be used.


</td></tr></tbody>
</table>6.  Select **Submit** to be returned to the Cryptographic Module table.


**Parent Topic:**[Create a cryptographic module life-cycle policy](create-cryptographic-module-lifecycle-policy.md)

