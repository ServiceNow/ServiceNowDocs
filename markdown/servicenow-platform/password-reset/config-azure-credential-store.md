---
title: Configure the connection to the Microsoft Entra ID Credential Store
description: Create a Password Reset credential store record to configure access to your Microsoft Entra ID server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see and other settings.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Credential Store for Password Reset for Microsoft Entra ID, Credential stores for Password Reset, Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the connection to the Microsoft Entra ID Credential Store

Create a Password Reset credential store record to configure access to your Microsoft Entra ID server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see and other settings.

## Before you begin

Role required: none

## About this task

The Microsoft Entra ID Integration for Password Reset installs the Microsoft Entra ID Credential Store type. The Microsoft Entra ID application supports only the **Microsoft Entra ID Credential Store**.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Credential Stores** and select **Sample Microsoft Credential Store** that you can use out of the box or as a template.

2.  Enter a unique **Name** and **Description** and then complete the form.

<table id="table_e3x_kff_g1b"><tbody><tr><td>

Type

</td><td>

Select **Sample Microsoft Entra ID Credential Store**. A ServiceNow credential store type is a template that provides the required set of capabilities for a particular type of credential store. Credential stores inherit the functionality of the credential store type.

</td></tr><tr><td>

Auto generate password

</td><td>

Specify a script include that generates a temporary password for use during the reset process.

</td></tr><tr><td>

Hostname

</td><td>

Specify the domain name of the Entra ID application in this column.

</td></tr><tr><td>

User account lookup

</td><td>

Specify the script include that maps the user ServiceNow platform ID to the user credential store ID. The default script, PwdDefaultUserAccountLookup, returns the user ServiceNow platform user name.

</td></tr><tr><td>

Password rule hint

</td><td>

Specify the text that appears on the password reset page to help the user to create a password that meets all requirements. The **Password rule** script enforces the requirements.

</td></tr><tr><td>

Password rule

</td><td>

Specify the client script that validates the new password entered by the user. The script is invoked when the user enters a new password and selects **Password Reset**.

</td></tr><tr><td>

Enable Password Strength

</td><td>

Select the check box to:-   Display the text box for the **Strength rule** script so you can update the script.
-   Display the graphical **Password Strength** bar to the user while the user changes or resets the password.


</td></tr><tr><td>

Strength rule

</td><td>

This text box appears only if you select **Enable Password Strength**.Specify the client script that calculates the strength/complexity of the password that the user enters. The script is invoked when the user begins to enter a new password during the reset process.

Default settings:-   Selected for local ServiceNow credential stores
-   Not selected for other credential stores
 **Note:**

To guide the user during the reset process, the system displays a graphical bar labeled **Password Strength** under the **New password** field.

</td></tr><tr><td>

Enable password policy

</td><td>

Check this option to select either a default password policy or one you created yourself previously.

</td></tr></tbody>
</table>3.  Click **Submit**.

    Password Reset Credential store record to access your Microsoft Entra ID server is configured.

    **Note:**

    -   The **Enable Password Policy** option was added in the Quebec release. Checking the option displays your password policy choices right from your instance. To learn more, see [Enable password policies on your instance](https://www.servicenow.com/docs/access?context=enable-password-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US).
    -   Since the Microsoft Entra ID doesn't support the history policy, the **Enforce history policy** option is hidden.

**Parent Topic:**[Credential Store for Password Reset for Microsoft Entra ID](../concept/credentials-store-micro-ad.md)

