---
title: Configure the connection to an AD credential store
description: You can create a Password Reset credential store record to configure access to your Active Directory server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Credentials Store for Password Reset for Active Directory, Credential stores for Password Reset, Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the connection to an AD credential store

You can create a Password Reset credential store record to configure access to your Active Directory server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.

## Before you begin

Role required: password\_reset\_admin

## About this task

The Microsoft AD Spoke for Password Reset add-on installs the AD Credential store type. The Password Reset Windows Application supports only **Microsoft AD Credential Store**.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Credential Stores** and select **Sample Microsoft AD Credential Store** to use as a template.

2.  Enter a unique and meaningful **Name** and **Description** and then fill in the form.

<table id="table_e3x_kff_g1b"><tbody><tr><td>

Type

</td><td>

Select **Microsoft AD Credential Store type**. A ServiceNow credential store type is a template that provides the required set of capabilities for a particular type of credential store. Credential stores inherit the functionality of the credential store type.

</td></tr><tr><td>

Auto-generate password

</td><td>

Specify a script include that generates a temporary password for use during the reset process.**Note:** If you select the **Enforce history policy** check box, then you must specify a value for **Auto-generate password** that is compliant with the password policy. There are several options to choose from:

-   An auto-generated password that is compliant with the policy you selected.
-   An auto-generated password that is Crypto-secure.
-   A default auto-generated password.


</td></tr><tr><td>

Enforce history policy

</td><td>

Appears only if you select a **Microsoft AD Credential Store type** or **Local ServiceNow Instance** credential store type. The Microsoft AD Credential Store type supports history check. The **Enforce history policy** option appears only when the **Supports history check** option is selected for the **Microsoft AD Credential Store type**.

For information on configuring the setting for credential store types other than AD, see [Configure the connection to a credential store for the Password Reset processes](t_CreateACredentialStore.md). Select the **Enforce history policy** check box to enforce the history policy \(password reuse\).

History policy \(password reuse\): Active Directory domains can be configured to include a history policy that ensures that users don't reuse passwords. For example, the history policy might be configured to not allow the user to reuse any of the previous 10 passwords when resetting a password. This history policy limit is managed by the password\_history\_limit verification parameter.

</td></tr><tr><td>

Hostname

</td><td>

Specify the URL or IP address of the credential store.

</td></tr><tr><td>

User account lookup

</td><td>

Specify the script include that maps the user ServiceNow platform ID to the user credential store ID. The default script, PwdDefaultUserAccountLookup, returns the user ServiceNow platform user name.

</td></tr><tr><td>

Password rule hint

</td><td>

Specify the text that appears on the password reset page to help the user to create a password that meets all requirements. The **Password rule** script enforces the requirements.**Note:** The Password Reset Windows Application supports newline characters in the hint. Other formatting is not supported \(bold, underline, hyperlink, and so on\).

</td></tr><tr><td>

Password rule

</td><td>

Specify the client script that validates the new password that the user enters. The script is invoked when the user enters a new password and clicks **Password Reset**. You can use the script to enforce password strength/complexity requirements.

</td></tr><tr><td>

Enable Password Strength

</td><td>

Select the check box to:-   Display the text box for the **Strength rule** script so you can update the script.
-   Display the graphical **Password Strength** bar to the user while the user changes or resets the password.
 **Note:** The Password Reset Windows Application does not support Password Strength.

</td></tr><tr><td>

Strength rule

</td><td>

This text box appears only if you select **Enable Password Strength**.Specify the client script that calculates the strength/complexity of the password that the user enters. The script is invoked when the user begins to enter a new password during the reset process.

Default settings:-   Selected for local ServiceNow credential stores
-   Not selected for other credential stores
 **Note:**

-   To guide the user during the reset process, the system displays a graphical bar labeled **Password Strength** under the **New password** field.

![Password strength indicator](../image/password-strength.png)

-   The Password Reset Windows Application does not support Password Strength.


</td></tr></tbody>
</table>3.  Click **Submit**.

4.  On the domain controller, set **Password Aging** \(MIN\_PASSWORD\_AGE\) to zero.

5.  To enforce the history policy that is configured for the AD credential store, follow these steps:

    1.  Open the Password Reset process that is associated with the credential store: **Password Reset** &gt; **Processes**.

    2.  On the **Password Reset Details** tab of the Password Reset Process form, clear the **Auto-generate password** check box and then save the process definition.

6.  To enforce the maximum number of attempts to reset the password, in the Password Reset Credential Store Parameters related list, set the value of the **max\_reset\_attempts** parameter to the number of allowed failed attempts.

    The default value of 0 \(zero\) enables an unlimited number of reset attempts.

    **Note:** The **max\_reset\_attempts** setting applies only to Password Reset processes that use AD credential stores.

7.  Click **Submit**.

8.  Set up the [Microsoft AD v2 spoke](https://www.servicenow.com/docs/access?context=setup-ms-ad-v2&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

9.  [Test the connection to the credential store](test-cxn-to-credential-store.md).


**Parent Topic:**[Credentials Store for Password Reset for Active Directory](../concept/credentials-store-AD.md)

**Related topics**  


[Configure the required strength for passwords](config-pwd-strength-rqmts.md)

