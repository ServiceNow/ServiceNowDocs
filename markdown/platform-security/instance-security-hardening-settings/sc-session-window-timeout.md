---
title: Minimize session window timeout duration
description: Use the glide.ui.user\_cookie.life\_span\_in\_days property to set the expiration time period for the Remember Me cookie. The default value is 15 days and the maximum cap is at 30 days.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize session window timeout duration

Use the **glide.ui.user\_cookie.life\_span\_in\_days** property to set the expiration time period for the Remember Me cookie. The default value is 15 days and the maximum cap is at 30 days.

The **glide.ui.user\_cookie.life\_span\_in\_days** system property affects the expiry of cookies. After each successful authentication, the cookie will expire after the number of days specified as the property value. If **glide.ui.user\_cookie.life\_span\_in\_days** isn't set to the recommended value of `15` or less, then there is a higher risk that the cookie, if stolen, can be used for longer.

Ensure the property **glide.ui.user\_cookie.life\_span\_in\_days** is set to `15` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

****

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

15 or less

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

15

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.9
-   CVSS rating: Medium
-   Security risk details: A longer life span increases the time window that a stolen cookie can be used.

</td></tr><tr><td>

Functional impact

</td><td>

This property is enabled by the end user when the end user checks the **Remember me** check box from the login page and logs in to the ServiceNow AI Platform.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

