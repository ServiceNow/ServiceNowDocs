---
title: Configure Field Encryption modules
description: Learn how to configure Field Encryption modules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Configure Field Encryption modules

Learn how to configure Field Encryption modules.

## Before you begin

Role required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience**.

2.  Select the module you want to configure. To create a new module, see [Create cryptographic module for Field Encryption](../../key-management-framework/task/create-PE-cryptographic-module.md).

3.  In the Module Overview fill out the fields as shown here.

<table id="table_p4x_3dw_22c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Module name

</td><td>

Displays the module name prepended with the application scope name to avoid conflict with other scoped applications. For example, if you create a module with the name my\_crypto\_module in the global application scope, the name is saved as global.my\_crypto\_module. Choose a name for the module. This name is referenced when running scripts.

</td></tr><tr><td>

Module lifecycle state

</td><td>

The term “lifecycle” refers to the creation, use, and deactivation of a cryptographic module. Set this value to **Draft** initially during configuration. Set it to **Published** for active use.**Note:** The default template is automatically set to **Published**.

</td></tr><tr><td>

Application scope

</td><td>

The application scope for this module. This field is automatically populated with the current application.

</td></tr><tr><td>

Cryptographic purpose

</td><td>

Displays the purpose of the selected algorithm, key, length, and mode. For Field Encryption, this field is read only and has a value of Symmetric Data Encryption/Data.

</td></tr><tr><td>

Crypto Spec Template

</td><td>

Automatically populated with **Default template**. This template is used to create the cryptographic module that contains mappings of many cryptographic purposes to cryptographic specifications and recommended algorithms.

</td></tr><tr><td>

Algorithm

</td><td>

Defines which encryption scheme will be used to encrypt fields associated with the module.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Configure the purpose, algorithm, key length, mode, and origin of your encryption key in [Cryptographic specifications for Field Encryption](configure-fe-crypto-specs.md).

**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

