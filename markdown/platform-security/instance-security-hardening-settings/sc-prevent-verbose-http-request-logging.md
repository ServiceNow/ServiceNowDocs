---
title: Prevent verbose HTTP request logging
description: Help prevent access to sensitive information by reducing verbose HTTP request logging.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Prevent verbose HTTP request logging

Help prevent access to sensitive information by reducing verbose HTTP request logging.

The two properties **glide.outbound\_http\_log.override** and **glide.outbound\_http\_log.override.level** work together to control the level of logging for outbound HTTP requests. When **glide.outbound\_http\_log.override** is set to **true**, the log level for requests and responses is controlled by **glide.outbound\_http\_log.override.level**. If the override level is set to **all** or **elevated**, then request and response headers are logged.

Ensure that **glide.outbound\_http\_log.override** is not set to **true** and that **glide.outbound\_http\_log.override.level** is not set to **all** or **elevated**. If these properties do not appear in the System Properties \[sys\_properties table\], they are in a secure state.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.outbound\_http\_log.override**
-   **glide.outbound\_http\_log.override.level**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   String

</td></tr><tr><td>

Recommended value

</td><td>

-   false
-   basic

</td></tr><tr><td>

Default value

</td><td>

-   false
-   &lt;blank&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   false
-   &lt;blank&gt;

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.0
-   CVSS rating: Medium
-   Security risk details: The headers logged through verbose settings for these properties can include sensitive information such as Authorization headers or cookies which can be used like credentials to access the requested resource. Any user who has access to the Outbound HTTP Logs table \(sys\_outbound\_http\_log\) can view this information changing their scope of access. The severity would depend on what type of outbound requests are made.

</td></tr><tr><td>

Functional impact

</td><td>

The **glide.outbound\_http\_log.override** system property enables you to override outbound http request log level. A value of **false** defaults the log level to basic.

 If **glide.outbound\_http\_log.override** is set to **true**, the level of logging is determined by the value of the **glide.outbound\_http\_log.override.level** property. This value can be **basic**, **elevated**, or **all**. All 3 are string/text based values. Any value other than these is interpreted as **basic**.

 For additional details, see [Configure outbound logging](https://www.servicenow.com/docs/access?context=outbound-logging-configure&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

