---
title: Prevent verbose HTTP request logging
description: Help prevent access to sensitive information by reducing verbose HTTP request logging.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Prevent verbose HTTP request logging

Help prevent access to sensitive information by reducing verbose HTTP request logging.

Control the level of logging for outbound HTTP requests to help prevent access to sensitive information, such as authorization headers or cookies. This information can be used like credentials to access the requested resource.

The logging level for these requests is controlled by the **glide.outbound\_http\_log.override** and **glide.outbound\_http\_log.override.level** properties. When **glide.outbound\_http\_log.override** is set to **true**, the log level for requests and responses is controlled by the **glide.outbound\_http\_log.override.level** property. If **glide.outbound\_http\_log.override.level** is set to **all** or **elevated**, then request and response headers are logged.

Set **glide.outbound\_http\_log.override** to **false** and **glide.outbound\_http\_log.override.level** to **basic**. If these properties don’t appear in the System Properties \[sys\_properties\] table, they are in a secure state by default.

## More information

<table id="table_zyc_nlf_32c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Technical configuration name

</td><td>

-   glide.outbound\_http\_log.override
-   glide.outbound\_http\_log.override.level

</td></tr><tr><td>

Plugin applicability

</td><td>

None

</td></tr><tr><td>

Security risk

</td><td>

Outbound HTTP request headers logged with verbose settings can include sensitive information such as Authorization headers or cookies. This information can be used like credentials to access the requested resource.

 Users with access to the Outbound HTTP Logs \[sys\_outbound\_http\_log\] table can view this information. The severity depends on what type of outbound requests are made.

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) score

</td><td>

5

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) rating

</td><td>

Medium

</td></tr><tr><td>

Functional impact

</td><td>

The **glide.outbound\_http\_log.override** system property enables you to override outbound http request log level. A value of **false** defaults the log level to basic.

 If **glide.outbound\_http\_log.override** is set to **true**, the level of logging is determined by the value of the **glide.outbound\_http\_log.override.level** property. This value can be **basic**, **elevated**, or **all**. All 3 are string/text based values. Any value other than these is interpreted as **basic**.

 For additional details, see [Configure outbound logging](https://www.servicenow.com/docs/access?context=outbound-logging-configure&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   String

</td></tr><tr><td>

Base system value

</td><td>

-   false
-   &lt;blank&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   false
-   &lt;blank&gt;

</td></tr><tr><td>

Recommended value

</td><td>

-   false
-   basic

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

