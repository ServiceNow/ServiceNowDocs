---
title: Set up Module Access Policies
description: Configure module access policies in External Key Management Service \(EKMS\) to control who can view encrypted data in clear text.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 2
breadcrumb: [Configuring External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Set up Module Access Policies

Configure module access policies in External Key Management Service \(EKMS\) to control who can view encrypted data in clear text.

## Before you begin

Role required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

Confirm that you have:

-   [Created a cryptographic module with external key wrapping enabled](ekms-configure-external-key-definition.md)
-   [Created an Encrypted Field Configuration](ekms-create-encrypted-field-config.md)

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience** &gt; **Configurations** &gt; **Access Policies**.

    **Note:** For additional information, refer to [Configure module access policies for Field Encryption](../../key-management-framework/task/create-module-access-policy.md).

2.  Select **Create New**.

3.  Select **Configure**.

4.  Complete the Module Access Policy \(MAP\) form.

<table id="table_w2n_qfy_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Enter a name for the policy.

</td></tr><tr><td>

Type

</td><td>

Decide who or what should have access to this MAP to encrypt or decrypt data.-   Scope- Anything within the specified Application Scope has access to this MAP.
-   Role- Only users with the specific role can access this MAP.
-   Script- Ensure a specified script can access this MAP.
-   System Access- Allows processes running in “System Context” access to this MAP.
-   Resource Exchange- Allows for the Resource Exchange feature access to this MAP.
For more information on how these different types of MAP work, see [Exploring Field Encryption](../concept/exploring-fe.md).

</td></tr><tr><td>

Target scope

</td><td>

Field is visible as an identifier for the Scope type. Refers to the functionality of the policy. Select the applications from the search menu.

</td></tr><tr><td>

Specify purpose

</td><td>

Optional.  Enable  to  display  the  Crypto  Spec  field  on  the  form.  Enable this option to configure granular operations, such as some users being able to encrypt, but not decrypt. 

</td></tr><tr><td>

Application

</td><td>

The  Application scope  is  auto-populated  by  your  current scope. 

</td></tr><tr><td>

Active

</td><td>

Select to activate the policy.

</td></tr><tr><td>

Result

</td><td>

Select one of the following:-   **StrictReject** rejects access under all circumstances.
-   **Reject** rejects users with the **Target Role** or **Target Scope** from accessing this cryptographic module unless another policy grants them access.
-   **Track** to permit access and monitor use of the module.


</td></tr></tbody>
</table>    ![Example of completed MAP form.](../image/ekms-create-map-track-ui.png)


## Result

The Module Access Policy for the script is available in the system.

Next steps:

-   [Test an external key definition](ekms-test-external-key-definition.md)
-   [Learn how to change the status of an AWS KMS Key](ekms-change-status-aws-kms-key.md)

**Parent Topic:**[Configuring External Key Management Service](../concept/ekms-configuring-external-key-management.md)

