---
title: Use an EXE file from the command line
description: As an alternative to command-line installation, you can use a wizard.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Install Password Reset Windows Application, Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use an EXE file from the command line

As an alternative to command-line installation, you can use a wizard.

## Before you begin

Role required: security\_admin elevated privilege

Privilege required: Windows local administrator

## Procedure

1.  Ensure that the user with the ServiceNow security\_admin role configures the security properties.

    For more information about the security properties, see [Configure security settings for the Password Reset Windows Application](../reference/win-security-properties-password-reset.md)

2.  Copy the following command into a text editor as one line with no breaks.

    ```
    PasswordResetWinAppInstall.exe /VERYSILENT /PasswordResetLinkURL https://<YourServerName>/$pwd_reset.do?sysparm_url=default /PasswordResetLinkName "Forgot password?"
    ```

3.  Add arguments and replace the default parameter values with the correct values for your organization.

    |Argument|Example|Description|
    |--------|-------|-----------|
    |`/Log`|`/Log=c:\temp\PwdResetInstallLog.log`|Optional. To generate a log file, you must first create the directory that the file is written to. In this example, you would create the `c:\temp`directory before running the installation.|
    |`/NORESTART`|`/NORESTART`|Optional. Include `/NORESTART` to prompt the user to restart the computer after installation.|

<table id="table_dw5_znz_wbb"><thead><tr><th>

Parameter

</th><th>

Default

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PasswordResetLinkURL

</td><td>

`https://<YourServerName>/$pwd_reset.do?sysparm_url=default`

</td><td>

URL of the page that users access when resetting a password.Be sure to substitute your ServiceNow server name and the URL suffix for the desired Password Reset process.

</td></tr><tr><td>

PasswordResetLinkName

</td><td>

`"Forgot password?"`

</td><td>

Text to display for the Password Reset link on the Windows login page. Update the text as needed. You must enclose the text in double-quote characters as shown. To ensure that the correct characters are used, do not copy/paste the example text. Instead, type the characters at the command line.

</td></tr><tr><td>

CredentialProviderGUID

</td><td>

 

</td><td>

Most installations do not need to specify this parameter value. Provide this value only if you use a customized credential provider and can provide a valid credential provider GUID.

</td></tr></tbody>
</table>4.  Navigate to the directory that holds the `PasswordResetWinAppInstall.exe` file.

5.  Run the updated command at the command line.

6.  After installation and depending on the setting for the `/NORESTART` argument, you might need to restart the computer.

    See [Install Password Reset Windows Application using a wizard](win-install-pwr-wizard.md).


**Parent Topic:**[Install Password Reset Windows Application](../concept/win-install-password-reset.md)

