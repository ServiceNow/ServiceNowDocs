---
title: Configure key lifecycle states
description: After you have created a cryptographic specification, you can configure the lifecycle actions for the keys in your instance.
locale: en-US
release: yokohama
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a cryptographic module, Configuring the Key Management Framework, Key Management Framework, Encryption]
---

# Configure key lifecycle states

After you have created a cryptographic specification, you can configure the lifecycle actions for the keys in your instance.

## Before you begin

Role required: sn\_kmf.admin

## Procedure

1.  Navigate to **Key Management** &gt; **Cryptographic Modules** &gt; **All**.

2.  Select the cryptographic module to configure the lifecycle of a key.

3.  Select a key alias on the Crypto Specifications tab.

    ![Shows how to select a key from the lifecycle definition.](../image/key-lifecycle-configuration.jpg)

4.  Select **Next**.

    The Field Lifecycle Template loads. Default Key Lifecycle values are created based on the selected algorithms for the defined cryptographic specification.

5.  Select a Key Lifecycle from the **Applies to** column on the Lifecycle Definition step for the crypto specification.

<table id="table_ocj_j5y_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

Selected key that the lifecycle applies to.

</td></tr><tr><td>

For field

</td><td>

Select the type of control for the key that the lifecycle applies to.![Shows the values in the "For field."](../image/field-lifecycle-for-field.jpg "Key lifecycle management "For field" values")

</td></tr><tr><td>

Type

</td><td>

Select if the valuation for the key lifecycle is a relative value or an absolute value:-   **Relative**: Enter a value that depends on other data entries in the system, such as key generation, activation, and deactivation.
-   **Absolute**: Enter an exact value, such as a date.


</td></tr><tr><td>

Lifecycle default

</td><td>

Read only. Displays a value if set.

</td></tr><tr><td>

Order

</td><td>

Enter the sequence in which to process the key lifecycle state for the crypto specification.

</td></tr><tr><td>

Relative duration type

</td><td>

Duration of the lifecycle: **Years**, **Months**, or **Days**.

</td></tr><tr><td>

Relative duration

</td><td>

Number of years, months, or days the key is valid.

</td></tr><tr><td>

Relative operation

</td><td>

**Before**or **After**.

</td></tr><tr><td>

Relative to

</td><td>

Field the duration is relative to. Displays if a relative duration or operation is selected.![Shows the values of the "Relative to" list.](../image/relative-to-kl-state.jpg)

</td></tr></tbody>
</table>
**Parent Topic:**[Create a cryptographic module](create-cryptographic-module.md)

