---
title: Enable email spam scoring and filtering
description: Install the Email Filter \(com.glide.email\_filter\) plugin to install email filtering within the instance. This filtering identifies existing headers, which enables you to decide what to do with the email based on the associated header. Alternatively, set com.glide.email\_filter to false.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Enable email spam scoring and filtering

Install the Email Filter \(**com.glide.email\_filter**\) plugin to install email filtering within the instance. This filtering identifies existing headers, which enables you to decide what to do with the email based on the associated header. Alternatively, set **com.glide.email\_filter** to false.

The Email Filter \(**com.glide.email\_filter**\) plugin installs email filtering within the instance. This filter identifies existing headers, which enables the administrator to decide what to do with the email based on the associated header. The plugin adds a header to each message, which can be used for filtering within the instance. This feature is very helpful for filtering out spam.

**Note:** Please make sure prerequisite property **glide.email.read.active** is set to **true**, as this control only applies when inbound email is enabled.

Ensure that the plugin **com.glide.email\_filter** is activated when the property **glide.email.read.active** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **com.glide.email\_filter**
-   **glide.email.read.active**

</td></tr><tr><td>

Configuration type

</td><td>

-   Plugin \(**All** &gt; **System Definition** &gt; **Plugins**\)
-   System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Plugin
-   Boolean

</td></tr><tr><td>

Recommended value

</td><td>

-   Plugin is active
-   true

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   N/A
-   true

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: Enabling and configuring email filtering is essential for reducing exposure to spam and maintaining system integrity.

</td></tr><tr><td>

Functional impact

</td><td>

Email is never filtered, blocked, or quarantined from the instance as part of spam scoring. It is only scored and then sent on to the instance. All filtering is done within the instance with the Email Filters plugin.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Before setting this property:

 Set the **glide.email.read.active** property to true. To learn more, see [Enable using your own POP3 server](https://www.servicenow.com/docs/access?context=t_ConfAltEmailConfPOP3Server&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

