---
title: Enable email spam scoring and filtering \[Updated in Security Center 1.3\]
description: Install the Email Filter \(com.glide.email\_filter\) plugin to install email filtering within the instance. This filtering identifies existing headers, which enables you to decide what to do with the email based on the associated header. Alternatively, set com.glide.email\_filter to false.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Enable email spam scoring and filtering \[Updated in Security Center 1.3\]

Install the Email Filter \(**com.glide.email\_filter**\) plugin to install email filtering within the instance. This filtering identifies existing headers, which enables you to decide what to do with the email based on the associated header. Alternatively, set **com.glide.email\_filter** to false.

Every message sent through ServiceNow AI Platform email servers is assessed for the likelihood of being spam.

**Note:** If an instance uses a private email server, this topic is not applicable. For more information, see Email Spam Scoring and Filtering.

## Prerequisites

Before setting this property:

Set the **glide.email.read.active** property to true. To learn more, see [Enable using your own POP3 server](https://www.servicenow.com/docs/access?context=t_ConfAltEmailConfPOP3Server&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Plugin Name

</td><td>

com.glide.email\_filter, glide.email.read.active

</td></tr><tr><td>

Configuration type

</td><td>

System Definition &gt; Plugins

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Purpose

</td><td>

To enforce filtering to avoid spamming of emails.

</td></tr><tr><td>

Recommended value

</td><td>

Either:-   The **glide.email.read.active** property to **false**
-   The **glide.email.read.active** property to **true** and activate the **Email Filter** \(com.glide.email\_filter\) plugin.

Active

</td></tr><tr><td>

Default value

</td><td>

None. This is a plugin, not a Glide property so there is no default value.

</td></tr><tr><td>

Security risk rating

</td><td>

8.1

</td></tr><tr><td>

Functional impact

</td><td>

Email is never filtered, blocked, or quarantined from the instance as part of spam scoring. It is only scored and then sent on to the instance. All filtering is done within the instance with the Email Filters plugin.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Email filters enable administrators to use a condition builder or conditional script to specify when to ignore malicious incoming emails from known/unknown sender.

</td></tr><tr><td>

References

</td><td>

[Email filters](https://www.servicenow.com/docs/access?context=c_EmailFilters&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

 [https://support.servicenow.com/kb\_view.do?sysparm\_article=KB0549426](https://support.servicenow.com/kb_view.do?sysparm_article=KB0549426)

</td></tr></tbody>
</table>To learn more about activating a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Parent Topic:**[File and resources](sc-file-resources.md)

