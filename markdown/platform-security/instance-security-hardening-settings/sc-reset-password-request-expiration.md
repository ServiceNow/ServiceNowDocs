---
title: Minimize reset password request expiration duration
description: The password\_reset.request.expiry denotes the time period in minutes during which a user must perform the password reset process.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize reset password request expiration duration

The **password\_reset.request.expiry** denotes the time period in minutes during which a user must perform the password reset process.

If the **password\_reset.request.expiry** system property is not set to the recommended value of `10` or less, then it increases the opportunity for someone else to guess and use the request and attempt to reset the password.

Ensure that the property **password\_reset.request.expiry** is set to `10` or less.

**Note:** The setting for the**password\_reset.request.expiry** property takes precedence over the setting for **glide.pwd\_reset.onetime.token.validity**property that has a 12 hour default.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.request.expiry**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

An integer less than or equal to 10

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

100

</td></tr><tr><td>

Category

</td><td>

[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS rating: Medium
-   Security risk details: Short expiration windows are critical to reducing the opportunity for unauthorized password resets and maintaining account security.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Authentication](sc-authentication.md)

