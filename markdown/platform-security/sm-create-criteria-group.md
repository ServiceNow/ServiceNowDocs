---
title: Create a secret group with criteria
description: Create a secret group with criteria to organize secrets entered in Password2 fields automatically when they share a common criteria, such as table, scope, or application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Secrets Management dashboard, Secrets Management, Platform Security]
---

# Create a secret group with criteria

Create a secret group with criteria to organize secrets entered in Password2 fields automatically when they share a common criteria, such as table, scope, or application.

## Before you begin

Role required: admin, KMF\_admin, sn\_secrets.secret\_manager, and sn\_kmf.cryptographic\_manager

Secrets within this type of secret group must all share common criteria. For groups without this restriction, consider creating a basic secret group. Learn about creating a basic secret group in [Create a basic secret group](sm-create-basic-group.md).

## Procedure

1.  Navigate to **All** &gt; **Secrets Management** &gt; **Secret Groups**.

2.  Select **New**.

3.  At the **What type of Secret Group would you like to create?** prompt, select **Secret Group with Criteria**.

4.  In the **Secret Group** form, fill in the fields.

<table id="table_tgr_xp5_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group Name

</td><td>

Name for the group**Note:** Secret group names can only contain lowercase characters, numbers, and underscores\( \_ \)

</td></tr><tr><td>

Secret Type

</td><td>

Whether the group is **Instance accessible** or **Client accessible.**

</td></tr><tr><td>

Autogen Module

</td><td>

Generates a new cryptographic module for this secret group. This module encrypts and decrypts your data. This field is enabled by default.

</td></tr><tr><td>

Application

</td><td>

Scoped application for this record. This read-only field is automatically populated with the current scope.

</td></tr><tr><td>

Short Description

</td><td>

Description of the group

</td></tr><tr><td>

Criterion Type

</td><td>

The criteria the secrets in this group shares.-   Scope
-   Package
-   Target table
-   Secret column
-   Filter record


</td></tr><tr><td>

Crypto Module

</td><td>

Select the cryptographic module to use with this group. This module encrypts and decrypts your data. This field is only visible when **Autogen Module** isn’t selected. For details on module access policies, see [Module access policy overview](../../key-management-framework/concept/module_access_policy_overview.md) **Note:** You can review the module access policies related to your secret group using the **Manage instance access** button.

</td></tr></tbody>
</table>    **Note:** Depending on your configuration, the **Crypto Module** might use an automatically selected value.

<table id="table_fcy_p5g_2bc"><tbody><tr><td>

When the **Criterion Type** field is set to `Package`, and the **Autogen Module** field is selected:

</td><td>

The **Crypto Module** field is empty and read-only. An existing Password2 submodule is used. If a Password2 submodule isn’t found, the instance level Glide Encrypter module is used.

</td></tr><tr><td>

When the **Criterion Type** field is set to `Package`, and the **Autogen Module** field is deselected: \(The **Autogen Module** field can only be deselected by Enterprise users\)

</td><td>

The **Crypto Module** field is editable, and admins can select a crypto module to use.

</td></tr></tbody>
</table>5.  Select and hold \(or right-click\) the form header and select **Save**.

    **Note:** When created, a secret group is inactive by default.

6.  After saving the record, additional fields might appear based on how you’ve configured your group.

<table id="table_lvc_4r5_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target Scope

</td><td>

Scope shared by the secrets to be assigned to this group. This field is only available when you select `Scope` in the **Criteria Type** field.

</td></tr><tr><td>

Target Package

</td><td>

Package shared by the secrets to be assigned to this group. This field is only available when you select `Package` in the **Criteria Type** field.

</td></tr><tr><td>

Target Table

</td><td>

Table shared by the secrets to be assigned to this group. This field is only available when you select `Table` or `Secret Column` in the **Criteria Type** field.

</td></tr><tr><td>

Application Scope

</td><td>

Application scope of the table selected in the **Target Table** field. This field is only visible when you select `Table`, `Filter Column`, or `Secret Column` in the **Criteria Type** field.

</td></tr><tr><td>

Secret Column

</td><td>

Table column that contains the Password2 secrets you include in this group. The fields available in this list are determined by the table selected in the **Target Table** field.**Note:** If there are no columns on the select table that contain secrets, this field only displays `– None --` as a selection.

</td></tr><tr><td>

Filter Column

</td><td>

The column on the table selected in **Target Table** you want to use as a filter. This field can’t be a Password2 field.

</td></tr><tr><td>

Filter value

</td><td>

Value to filter by, based on the column selected in the **Filter Column** field.

</td></tr></tbody>
</table>
## An instance accessible group containing all email account passwords for an email server

![Group containing all email account passwords for a specific email server](../images/secret-group-example.png)

## What to do next

After creating your group, any new records matching the criteria will be encrypted. To encrypt existing records using this group's cryptographic module, you must run a security job. For details, see [Run Secrets Management security jobs](sm-security-jobs.md).

Client-accessible groups need a customer-provided public key to encrypt your secrets. For steps on uploading this key, see [Upload a public key for Secrets Management](sm-upload-key.md).

**Parent Topic:**[Secrets Management dashboard](../concept/secrets-dashboard.md)

