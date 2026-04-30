---
title: Password Reset Credential Store form
description: Description of the fields on the Password Reset Credential Store form.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset Credential Store form

Description of the fields on the Password Reset Credential Store form.

<table id="table_e3x_kff_g1b"><tbody><tr><td>

Type

</td><td>

Type of credential store that you are connecting to. A ServiceNow credential store type is a template that provides the required set of capabilities for a particular kind of credential store. Credential stores inherit the functionality of the credential store type.**Note:** For an AD credential store, skip this procedure and see [Integrate Password Reset with your Active Directory service](../task/t_ConPassResetActiveDir.md). The Password Reset Windows Application supports only AD credential stores.

</td></tr><tr><td>

Auto generate password

</td><td>

Script include that generates a temporary password for use during the reset process.If you select the **Enforce history policy** check box, then you must specify a value for **Auto-generate password** that is compliant with the password policy.

</td></tr><tr><td>

Enforce history policy

</td><td>

Appears only if you select a credential store **Type** of **AD Credential Store** or **Local ServiceNow Instance**. For information on configuring the setting for an AD credential store, see [Configure the connection to an AD credential store](../task/config-ad-credential-store.md). Select the **Enforce history policy** check box to ensure that users do not reuse passwords. For example, you might configure the history policy to not allow the user to reuse any of the previous 10 passwords. Follow this procedure:

 1.  Select the **Enforce history policy** check box.
2.  In the Password Reset Credential Store Parameters related list, create a **password\_history\_limit** parameter.
3.  Set the value of the parameter to the number of previous passwords that cannot be used \(maximum **10**\). The default value of 0 \(zero\) enables use of any previous password.

</td></tr><tr><td>

Child Alias

</td><td>

Child aliases are associated with the base alias. After creating a connection and credential alias, you can create a child alias to configure multiple connections for a password reset credential store. When a password reset request is made, the flow checks whether there are child alias connections at the process level. If the child alias is configured at the credential store level, the flow picks the aliases connections and proceeds with the request.

</td></tr><tr><td>

Enable password policy

</td><td>

See [Enable password policies on your instance](https://www.servicenow.com/docs/access?context=enable-password-policies&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td></tr><tr><td>

Password policy

</td><td>

You can use the default policy or define your own.

</td></tr><tr><td>

Hostname

</td><td>

URL or IP address of the credential store.

</td></tr><tr><td>

User account lookup

</td><td>

Script include that maps the user ServiceNow platform ID to the user credential store ID. A default script, PwdDefaultUserAccountLookup, returns the user ServiceNow platform user name.

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
</table>**Related topics**  


[Configure the connection to a credential store for the Password Reset processes](../task/t_CreateACredentialStore.md)

