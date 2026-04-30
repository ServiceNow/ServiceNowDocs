---
title: Create a module access policy
description: Create module access policies to decide which users and scripts can access data encrypted by a cryptographic module.
locale: en-US
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring the Key Management Framework, Key Management Framework, Encryption]
---

# Create a module access policy

Create module access policies to decide which users and scripts can access data encrypted by a cryptographic module.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager or sn\_kmf.admin

## About this task

Field Encryption supports role-based module access policies and additional configuration options become available with \(CLE\_Ent\) functionality.

-   Configure the specific cryptographic operation in module access policies for cryptographic modules that support symmetric operations. For instance, a user can be enabled to encrypt data but not decrypt data.
-   Set a default module access policy value or according to a cryptographic module.
-   Associate script versions where changes to the script are tracked and invalidate the script policy providing better security for script-type module access policies.

CLE\_Ent functionality is available with a paid subscription. Refer to for supported features and options available with each offering. For more information, see Field Encryption Enterprise.

**Note:** The default behavior of the module access policies \(MAPs\) is Reject to help prevent any unauthorized access, unless explicitly declared in MAP records.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Module Access Policies** &gt; **** **All**.

    If you don't create a cryptographic module configured for Symmetric Data Encryption/Decryption, an auto-generated module access policy is created and listed in the table.

2.  Select **New**.

    -   Select **Specify purpose** to choose a **Crypto spec** and set the **Granular operation**.![When selecting the Specify purpose check box, Cryptographic spec fields are available.](../image/map-cryptospec-granularity.png)
    -   With cryptographic specifications for symmetric data encryption/decryption and symmetric wrapping/unwrapping, the **Granular operation** field is available if you select the **Specify purpose** check box.

        ![Granular operation list.](../image/granular-operations.png)

3.  Complete the form.

    Module Access Policies fields

<table id="simpletable_b1d_ytf_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Enter a name for the policy.

</td></tr><tr><td>

Crypto module

</td><td>

Select the search icon \(![Search icon.](../image/IconUI11GlobalTextSearch.png)\) to select a module.

</td></tr><tr><td>

Crypto spec

</td><td>

Select or create cryptographic specification while generating the module access policy. This field becomes available when the **Specify purpose** check box is selected.

</td></tr><tr><td>

Granular operation

</td><td>

Select the cryptographic purpose for the cryptographic specification. The values available depend upon the type of cryptographic specification that is selected.See for details on crypto purposes.

</td></tr><tr><td>

Type

</td><td>

-   **Scope**: Controls access by the application scope.
-   **System user**: Allows access for system users to crypto modules.
-   **Script**: Control access by script. See for more information
-   **Role**: Controls access by user role.
-   **Resource Exchange**: Control access using the Resource Exchange. See for more information.
 **Note:** Only Role type is supported with Field Encryption. All other types are available with Field Encryption Enterprise.

</td></tr><tr><td>

Target Scope

</td><td>

Field is visible as an identifier for the **Scope** type. Refers to the functionality for the policy. Select the applications from the search menu.**Note:** Target scope isn't supported and can only be set with Field Encryption Enterprise

</td></tr><tr><td>

Target Role

</td><td>

Field is visible as an identifier for the **Role** type. Role to which this policy applies.

</td></tr><tr><td>

Script TableTarget Script

</td><td>

These fields appear when you select **Script** as the type.

 Field is visible as an identifier for the **Script** Type. Select a table to which this policy applies. Document to which this policy applies. Select the **Table name** and then the related document for the policy.

 The first time a script calls a cryptographic module, access to the module is denied, and the developer receives an error. This error gives the module owner the ability to grant or refuse access to the module.

</td></tr><tr><td>

Resource Exchange:

 -   Crypto spec
-   Approval type
-   Target instance host


</td><td>

These options appear when you select as the type.

 Resource Exchange is supported by both KMF and by when the parent module is **column\_level\_encryption**.

 Select the crypto specification, One-time or Recurring, and the URL of the target instance. See for more information.

</td></tr><tr><td>

Impersonation

</td><td>

In role-based module access policies, users can access encrypted data using an impersonation session. When users, such as admins, impersonate other users, such impersonation-enabled module access policies are applied.

</td></tr><tr><td>

Specify purpose

</td><td>

Select to toggle the Cryptographic specification field as an available field for the policy.

</td></tr><tr><td>

Active

</td><td>

Select to activate the policy.

</td></tr><tr><td>

Result

</td><td>

Select one of the following: -   **StrictReject** rejects access under all circumstances.
-   **Reject** rejects users with the **Target Role** or **Target Scope** from accessing this cryptographic module unless another policy grants them access.
-   **Track** to permit access and monitor use of the module.


</td></tr></tbody>
</table>4.  Select **Submit**.

    **Warning:**

    -   **For legacy encryption support users:**

        If you're using the non-enterprise version of Field Encryption, you're limited to five modules. If you have exceeded this limit, you receive the following warning:

        This insertion exceeds the number of published modules allowed for Field Encryption entitled with the subscription product. The Enterprise subscription for Field Encryption is required for additional modules. Please reach out to your Account team.

5.  Select the policy name associated with the cryptographic module that you want to examine.

    Using Script type module access policy:

    A module access policy is auto-generated based on the default access setting when the script is run. The module name is preceded with `AutoGen-`. For example, the `Module-TestPolicy` module is listed as `AutoGen-Module-TestPolicy` in the Policy name column.

    The Cryptographic Caller Policy form lists the caller policy that you selected. The Target Scope field specifies the scope of the script attempting to use the module. See for additional information.

    **Note:** A maximum of five module access policies are permitted with Field Encryption. See for configuration options.


**Parent Topic:**[Configuring the Key Management Framework](../../encryption/concept/configure-kmf.md)

