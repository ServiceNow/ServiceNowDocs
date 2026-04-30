---
title: Customize the Password Reset Windows Application
description: You can customize the appearance and other aspects of the application.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Customize the Password Reset Windows Application

You can customize the appearance and other aspects of the application.

## Before you begin

Role required: Windows system administrator

## Procedure

1.  Open the Registry Editor on your Windows computer.

2.  Go to **Computer** &gt; **HKEY\_LOCAL\_MACHINE** &gt; **SOFTWARE** &gt; **Microsoft** &gt; **Windows** &gt; **CurrentVersion** &gt; **Authentication** &gt; **Credential Providers** &gt; **0780AF60-65C2-4718-942D-E0C56E89EF9B**.

3.  Modify any of the listed string values:

    **Note:** Registry keys that begin with the text `"proxy"` enable use of a proxy server. See [Configure registry keys on your proxy server](win-proxy-registry-password-reset.md).

<table id="table_iqw_xb5_2r"><thead><tr><th>

File name

</th><th>

Description

</th><th>

Default string

</th></tr></thead><tbody><tr><td>

AppDir

</td><td>

Directory that holds the Password Reset Windows Application application files.

</td><td>

`C:\Program Files\ServiceNow`

</td></tr><tr><td>

AppFormIconFile

</td><td>

Icon that is associated with the Password Reset application.

</td><td>

`C:\Program Files\ServiceNow\bin\ServicenowLogo.png`You can change the icon that's associated with your company. Replace the `ServicenowLogo.png` with your company logo and change the `AppFormIconFile` path in the registry.

</td></tr><tr><td>

AppFormTitle

</td><td>

Displayed name of the application.

</td><td>

Password Reset Windows Application

</td></tr><tr><td>

CheckCertificateRevocationList

</td><td>

By default, before every communication, the Password Reset Windows Application validates that the server certificate has not been revoked by checking the Certificate Revocation List \(CRL\). If the Password Reset Windows Application is slow to load after a user requests reset, you can choose to skip checking the CRL.

</td><td>

Default: "true"

 -   **true**: When a user requests reset, the application first checks the CRL to validate the certificate. The application does not proceed without a valid certificate.
-   **false**: The application starts immediately and does not validate the certificate.


</td></tr><tr><td>

CredentialProviderGUID

</td><td>

GUID of the credential provider that is in use.

</td><td>

”"="\{6f45dc1e-5384-457a-bc13-2cd81b0d28ed\}”

</td></tr><tr><td>

DebugFlag

</td><td>

Write entries in the ServiceNowPwdReset event log.

</td><td>

”0”

</td></tr><tr><td>

PasswordResetLinkName

</td><td>

Text to display for the Password Reset link on the Windows login page.

</td><td>

"Forgot password?"

</td></tr><tr><td>

PasswordResetLinkURL

</td><td>

URL of the Password Reset application on your ServiceNow instance.

</td><td>

https://&lt;YourServerName&gt;/$pwd\_reset.do?sysparm\_url=default

</td></tr><tr><td>

Proxy

</td><td>

Keys that configure proxy settings

</td><td>

Registry keys that begin with the text `"proxy"` enable use of a proxy server. See [Configure registry keys on your proxy server](win-proxy-registry-password-reset.md).

</td></tr><tr><td>

ServiceNowServerVersion

</td><td>

Version of your production instance.

</td><td>

"&lt;YourInstanceVersion&gt;" \(For example, "Kingston"\)

</td></tr><tr><td>

ServiceNowWinAppVersion

</td><td>

Version of the Password Reset Windows Application.

</td><td>

"&lt;YourWindowsAppVersion&gt;" \(For example, "4.5"\)

</td></tr><tr><td>

UserAccountPictureLoc

</td><td>

Image that appears on the Login screen.

</td><td>

`%programdata%\Microsoft\User Account Pictures\user.bmp`

</td></tr><tr><td>

WorkingDir

</td><td>

Directory that holds the library files.

</td><td>

`C:\Program Files\ServiceNow\bin`

</td></tr></tbody>
</table>
**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

