---
title: Set up Microsoft Active Directory for Password Reset
description: Enable connections to Active Directory \(AD\) by activating the Password Reset Windows App and Microsoft AD for Password Reset available in the ServiceNow Store.Request the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin that enables connections to the Active Directory \(AD\) credential store types. No other components are installed.The Password Reset Windows Application enables a user, who forgets the password or is locked out of a Windows computer, to reset the password directly from the Windows login screen.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Set up, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up Microsoft Active Directory for Password Reset

Enable connections to Active Directory \(AD\) by activating the Password Reset Windows App and Microsoft AD for Password Reset available in the ServiceNow Store.

## Request the Password Reset Windows App plugin

Request the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin that enables connections to the Active Directory \(AD\) credential store types. No other components are installed.

### Before you begin

Role required: password\_reset\_admin

### About this task

There are two ways to request a plugin:

-   Access the Now Support Service Catalog directly by selecting **All** &gt; **Service Catalog** &gt; **Activate Plugin** on Now Support. For more information about the list of plugins, see [List of Plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   Access the Now Support Service Catalog through the All Applications page on your instance by following these steps.

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  On the All Applications page, select **Request Plugin** to open the Request form on HI.

    ![Request Plugin button on the All Applications page.](../../../reuse/images/request-plugin.png)

3.  On Now Support, select the redirect link to access the Now Support Service Portal Service Catalog.

    ![HI redirect to Service Catalog..](../../../reuse/images/hi-redirect.png)

4.  Select your instance.

5.  Select **Actions &gt; Activate Plugin**.

6.  On the form, fill in the fields.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

Target Instance

</td><td>

Instance on which to activate the plugin.

</td></tr><tr><td>

Plugin Name

</td><td>

Name of the plugin to activate.

</td></tr><tr id="date-time"><td>

Specify the date and time you would like this plugin to be enabled

</td><td>

The date and time must be at least two business days from the current time.**Note:** Plugins are activated in two batches, in the morning and in the evening, on every business day in the US Pacific time zone. If the plugin must be activated at a specific time, enter the request in the **Reason/Comments** field.

</td></tr><tr id="reasons-comments"><td>

Reason/Comments

</td><td>

Information that would be helpful for the ServiceNow personnel who are activating the plugin. For example, if you need the plugin activated at a specific time instead of during one of the default activation windows, specify that in the comments.

</td></tr></tbody>
</table>7.  Select **Submit**.


## Password Reset Windows Application

The Password Reset Windows Application enables a user, who forgets the password or is locked out of a Windows computer, to reset the password directly from the Windows login screen.

### How the Password Reset Windows Application works

Download the Password Windows Reset application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) and run an EXE or MSI file to install or distribute the application to user computers. The application installs a link on the Windows login screen. The user clicks the link \(**Forgot Password?** as depicted in the examples on various Windows versions\) and is then guided through the process of resetting the password.

![Windows login screen](../image/password-reset-login-win10.png "Windows login screen")

![Windows login screen](../image/password-reset-login-win8.png "Windows login screen")

![Windows login screen](../image/password-reset-login-win7.png "Windows login screen")

By default, when a user requests a reset, the instance sends the user a URL with a user-specific token. After the user opens the URL, the instance prompts the user to enter and confirm the new password. The instance does not send a temporary password.

### Restrictions on the Password Reset Windows Application

-   The Password Reset Windows Application does not support custom verifications.
-   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface. See the section titled "Settings on the Details tab" in [Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md). .
-   The Password strength indicator is not supported. See [Configure the connection to a credential store for the Password Reset processes](../task/t_CreateACredentialStore.md).
-   For some verification types, you can use only one verification. Custom verifications are not supported. See [Password Reset verifications](c_PWRVerifications.md) for details.
-   Custom UI macros configured on the **Process** &gt; **Advanced** page are not supported \(for example, entry, success, or failure macros\). The system displays only the default success and failure messages.
-   The Password Reset Windows Application supports newline characters in the **Password rule hint** text. Other formatting is not supported \(bold, underline, hyperlink, and so on\). See [Configure the connection to a credential store for the Password Reset processes](../task/t_CreateACredentialStore.md).

### Password Reset Windows Application installation requirements

Activate the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin and activate the Microsoft AD for Password Reset store app to use the Password Reset Windows Application. You must [activate the Password Reset Windows App](setup-guide-ad.md#) to use the Password Reset Windows Application.

<table id="table_sjp_y3t_2r"><thead><tr><th>

Requirement

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Required ServiceNow release

</td><td>

Password Reset Windows Application latest version can be downloaded from store.

</td></tr><tr><td>

Required hardware

</td><td>

-   1 GHz or faster processor
-   512 MB of RAM
-   10 MB of available hard disk space \(x86\)
-   10 MB of available hard disk space \(x64\)

</td></tr><tr><td>

Required software

</td><td>

-   Version of Password Reset Windows Application: 4.1
-   Microsoft .NET Framework: 4.7.1 and newer
-   Microsoft Visual C++: Redistributable Visual Studio 2017

</td></tr><tr><td>

Supported operating systems

</td><td>

-   Windows 7
-   Windows 8.1
-   Windows 10 Enterprise
-   Windows 10 Pro

</td></tr><tr><td>

Supported processor architecture

</td><td>

-   X86
-   X64

</td></tr><tr><td>

Supported network architecture

</td><td>

-   Password Reset Windows Application clients must have direct access to both the Internet and the ServiceNow instance where the Password Reset Windows Application is configured
-   For Password Reset Windows Application versions that use an SHA certificate, the corporate network must not block the SHA certificate.
-   To reset an AD password, the client must be on the corporate network.

</td></tr></tbody>
</table>