---
title: Configure Field Encryption modules
description: Learn how to configure Field Encryption modules.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Configure Field Encryption modules

Learn how to configure Field Encryption modules.

## Before you begin

Role required: KMF Admin or KMF Cryptographic Manager

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Modules**.

2.  Select **New**

3.  In the Module form fill out the fields as shown here.

<table id="table_p4x_3dw_22c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Module name

</td><td>

Choose a name for the module. This name is referenced when running scripts.

</td></tr><tr><td>

Crypto Spec Template

</td><td>

Automatically populated with **Default template**. This template is used to create the cryptographic module that contains mappings of many cryptographic purposes to cryptographic specifications and recommended algorithms.

</td></tr><tr><td>

Application

</td><td>

The application scope for this module. This field is automatically populated with the current application.

</td></tr><tr><td>

Name

</td><td>

This name automatically generated. It is the module name prepended with the application scope name to avoid conflict with other scoped applications. For example, if you create a module with the name `my_crypto_module` in the global application scope, the name is saved as `global.my_crypto_module`.

</td></tr><tr><td>

Crypto Module Lifecycle State

</td><td>

The term “lifecycle” refers to the creation, use, and deactivation of a cryptographic module. Set this value to **Draft** initially during configuration. Set it to **Published** for active use.**Note:** The Default template is automatically set to **Published**.

</td></tr><tr><td>

Parent Crypto Module

</td><td>

For Field Encryption, ensure this value is set to **column\_level\_encryption**.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Configure the purpose, algorithm, key length, mode, and origin of your encryption key in [Cryptographic specifications for Field Encryption](configure-fe-crypto-specs.md).

**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

