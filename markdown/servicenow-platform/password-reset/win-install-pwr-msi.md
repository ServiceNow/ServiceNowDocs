---
title: Use an MSI file from the command line
description: Use the MSI file to install the Password Reset Windows Application on multiple computers over a network. As an alternative to MSI installation, you can also install from the command line.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Install Password Reset Windows Application, Installing and configuring Password Reset Windows Application, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use an MSI file from the command line

Use the MSI file to install the Password Reset Windows Application on multiple computers over a network. As an alternative to MSI installation, you can also install from the command line.

## Before you begin

Role required: Windows local administrator

## Procedure

1.  Ensure that the user with the ServiceNow security\_admin role configures the security properties.

    For more information about security properties, see [Configure security settings for the Password Reset Windows Application](../reference/win-security-properties-password-reset.md).

2.  Copy the following command into a text editor as one line with no breaks.

    ```
    msiexec.exe /i PasswordResetWinAppInstall.msi /quiet WRAPPED_ARGUMENTS="/SUPPRESSMSGBOXES /VERYSILENT /NORESTART /PasswordResetLinkURL https://<YourServerName>/$pwd_reset.do?sysparm_url=default /PasswordResetLinkName ""Forgot password?"""
    ```

3.  Add arguments and replace the default parameter values with the correct values for your organization.

<table id="table_jy2_z4z_wbb"><thead><tr><th>

Argument

</th><th>

Example

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`/Log`

</td><td>

`/Log=c:\temp\PwdResetInstallLog.log`

</td><td>

Optional. To generate a log file, you must first create the directory that the file is written to. In this example, you would create the `c:\temp`directory before running the installation.

</td></tr><tr><td>

`/NORESTART`

</td><td>

`/NORESTART`

</td><td>

Optional. By default, MSI installations restart the computers. Include `/NORESTART` not to restart the computers after installation.You might want to communicate with end users that they must restart their computer to enable the Password Reset Windows Application.

</td></tr></tbody>
</table><table id="table_yfb_cpz_wbb"><thead><tr><th>

Parameter

</th><th>

Default value to replace

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

`""Forgot password?""`

</td><td>

Text to display for the Password Reset link on the Windows login page. You must enclose the text in two double-quote characters as shown. To ensure that the correct characters are used, do not copy/paste the example text. Instead, type the characters at the command line.

</td></tr><tr><td>

Optional: CredentialProviderGUID

</td><td>

 

</td><td>

Most installations do not need to specify this parameter value. Provide this value only if you use a customized credential provider and can provide a valid credential provider GUID.

</td></tr></tbody>
</table>4.  Navigate to the directory that holds the `PasswordResetWinAppInstall.msi` file.

5.  Run the updated command at the command line.

6.  After installation and depending on the setting for the `/NORESTART` argument, you might need to restart computers.

    See [Install Password Reset Windows Application using a wizard](win-install-pwr-wizard.md) and [Install the Password Reset Windows Application using an EXE file from the command line](win-install-pwr-exe.md).


**Parent Topic:**[Install Password Reset Windows Application](../concept/win-install-password-reset.md)

