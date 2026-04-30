---
title: Use a wizard
description: As an alternative to wizard installation, you can run commands directly at the command line.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Install Password Reset Windows Application, Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use a wizard

As an alternative to wizard installation, you can run commands directly at the command line.

## Before you begin

Role required: Windows local administrator

## Procedure

1.  Ensure that the user with the ServiceNow security\_admin role configures the security properties.

    For more information about the security properties, see [Configure security settings for the Password Reset Windows Application](../reference/win-security-properties-password-reset.md).

2.  Right-click the `PasswordResetWinAppInstall.exe` installation file that you downloaded and select **Run as administrator**.

3.  On the **Configure Password Reset Web page and credential provider** page, configure the following settings and then click **Next**:

<table id="table_iwg_3pz_wbb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

URL of the Password Reset page

</td><td>

URL of the page on your ServiceNow instance that users access when resetting a password. Be sure to substitute your ServiceNow server name and the URL suffix for the desired Password Reset process.

</td><td>

`https://<YourServerName>/$pwd_reset.do?sysparm_url=default`

</td></tr><tr><td>

Text to display for the Password Reset link

</td><td>

Text to display for the Password Reset link on the Windows login page. Update the text as needed.

</td><td>

`Forgot password?`

</td></tr><tr><td>

GUID of the credential provider

</td><td>

Most installations do not need to specify this parameter value. Provide this value only if you use a customized credential provider and can provide a valid credential provider GUID.

</td><td>

\[Accept the default.\]

</td></tr></tbody>
</table>4.  For the remaining pages, perform the following actions:

    |Page title|Action|
    |----------|------|
    |License Agreement|Select **I accept the agreement**.|
    |Select Destination Location|Accept the default installation location.|
    |Select Start Menu Folder|Accept the default "ServiceNow".|
    |Ready to Install|Click **Install**.|

5.  Restart the computer.

    See [Use an EXE file from the command line](win-install-pwr-exe.md).


**Parent Topic:**[Install Password Reset Windows Application](../concept/win-install-password-reset.md)

