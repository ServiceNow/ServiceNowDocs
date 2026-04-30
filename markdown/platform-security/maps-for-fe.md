---
title: Configure module access policies for field encryption
description: Create a module access policy to control which users, scripts, or system processes can encrypt or decrypt data encrypted by a field encryption module.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-31"
reading_time_minutes: 4
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Configure module access policies for field encryption

Create a module access policy to control which users, scripts, or system processes can encrypt or decrypt data encrypted by a field encryption module.

## Before you begin

Role required: KMF Admin or KMF Cryptographic Manager, Security Admin

You must have a published field encryption module to use this process. If you have not done so, see [Configure Field Encryption modules](configure-fe-modules.md).

## About this task

Module access policies \(MAPs\) are the access controls you apply to your field encryption modules to define which users, scripts, or system processes can encrypt or decrypt data. Configure MAPs for users \(via roles\), scripts, or processes running in the “system” context. Without a MAP, users, scripts, or system processes aren’t able to encrypt or decrypt data, which can result in end-to-end workflow processes not working correctly.

MAPs are separate from access control lists \(ACL\), but can be used in combination with them. See [Exploring Field Encryption](../concept/exploring-fe.md) for more information about the purpose behind MAPs.

For Field Encryption Enterprise, review to plan for which users, scripts, or system processes need a MAP.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Module Access Policies** &gt; **All**.

2.  Select **New**.

3.  In the Module Access Policy form, fill in the fields as needed.

<table id="table_wyr_rgm_f2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy Name

</td><td>

Name of your MAP

</td></tr><tr><td>

Crypto Module

</td><td>

Select the field encryption module to be governed by this MAP.

</td></tr><tr><td>

Crypto Spec

</td><td>

Optional. Select or create a new Cryptographic Specification for this MAP.This field appears only when the **Specify Purpose** field is enabled.

</td></tr><tr><td>

Type

</td><td>

Decide who or what should have access to this MAP to encrypt or decrypt data.-   **Scope**

Anything within the specified Application Scope has access to this MAP.

-   **Role**

Only users with the specific role can access this MAP.

-   **Script**

Ensure a specified script can access this MAP.

-   **System Access**

Allows processes running in “System Context” access to this MAP.

-   **Resource Exchange**

Allows for the Resource Exchange feature access to this MAP.

For more information on how these different types of MAP work, see [Exploring Field Encryption](../concept/exploring-fe.md).

</td></tr><tr><td>

Target Scope

</td><td>

Select a scope to that this MAP applies to. This field appears only if the **Type** field is set to **Scope**.

</td></tr><tr><td>

Specify Purpose

</td><td>

Optional. Enable to display the **Crypto Spec** field on the form. Enable this option to configure granular operations, such as some users being able to encrypt, but not decrypt.

</td></tr><tr><td>

Granular Operation

</td><td>

Optional. Select the cryptographic purpose for the Crypto Spec. The values available depend upon the type of Crypto Spec that is selected. For example, you can specify that this MAP only allows users to encrypt, but not decrypt, or the opposite, or both.

This field appears only if there’s a value in the **Crypto Spec** field.

-   If a user has encrypt access, but not decrypt access, the field displays in edit mode and the data entered displays as asterisks.
-   If a user has decrypt access, but not encrypt access, the field displays the decrypted data in read-only mode.
-   If a user has encrypt and decrypt access, both read and write functionality are available for the encrypted field.


</td></tr><tr><td>

Target Role

</td><td>

Select which role should have access to this MAP.This field appears only when the **Type** field is set to **Role**

</td></tr><tr><td>

Script Table

</td><td>

Select which type of script applies to this MAP:-   Access Control
-   Activity Designer
-   Business Rule
-   Inbound Email Action
-   Record Producer
-   Scheduled Script Execution
-   Script Include
-   UI Action
-   Widget
-   Workflow Activity
This field appears only if the **Type** field is set to **Script**.

</td></tr><tr><td>

Target Script

</td><td>

Choose the specific script of the type table selected in the **Script Table** field that should have access to this MAP.This field appears only if the **Type** field is set to **Script**.

</td></tr><tr><td>

Check Script Version

</td><td>

When selected, the system checks the version of the script that is run with the version specified in the **Target Script** field. If the versions are different, the admin is notified.This field appears only if the **Type** field is set to **Script**.

</td></tr><tr><td>

Approval Type

</td><td>

Select either **One Time** or **Recurring**:-   **One Time**

Allows for the symmetric data encryption key in the associated field encryption module to be securely shared to the target instance one time.

-   **Recurring**

Allows for the symmetric data encryption key in the associated field encryption module to be securely shared to the target instance on a recurring basis.

This field appears only if the **Type** field is set to **Resource Exchange**.

</td></tr><tr><td>

Target Instance Host

</td><td>

Enter the URL for the target instance that the symmetric data encryption key in the associated field encryption module is being sent to.This field appears only if the **Type** field is set to **Resource Exchange**.

</td></tr><tr><td>

Impersonation

</td><td>

When enabled, a user impersonating another user gains any MAP permissions from both users. If disabled, a user impersonating another user only has any MAP permissions that were granted to them from before the impersonation.

</td></tr><tr><td>

Active

</td><td>

Enable to activate this MAP.

</td></tr><tr><td>

Result

</td><td>

Select one of the following:-   **Track**

Permits access and monitors use of the MAP.

-   **Reject**

Rejects access unless a different MAP grants access.

-   **StrictReject**

Rejects access under all circumstances, even if a different MAP grants access.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

