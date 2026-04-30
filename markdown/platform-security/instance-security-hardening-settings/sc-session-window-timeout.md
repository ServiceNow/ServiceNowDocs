---
title: Minimize session window timeout duration \[Updated in Security Center 1.3\]
description: Use the glide.ui.user\_cookie.life\_span\_in\_days property to set the expiration time period for the Remember Me cookie. The default value is 15 days and the maximum cap is at 30 days.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize session window timeout duration \[Updated in Security Center 1.3\]

Use the **glide.ui.user\_cookie.life\_span\_in\_days** property to set the expiration time period for the Remember Me cookie. The default value is 15 days and the maximum cap is at 30 days.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.user\_cookie.life\_span\_in\_days**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Purpose

</td><td>

To enable the default expiry of the **remember me** cookie.

</td></tr><tr><td>

Data type

</td><td>

Integer

</td></tr><tr><td>

Recommended value

</td><td>

15

</td></tr><tr><td>

Default value

</td><td>

15

</td></tr><tr><td>

Security risk rating

</td><td>

4.9

</td></tr><tr><td>

Functional Impact

</td><td>

This property is enabled by the end user when the end user checks the **Remember me** check box from the login page and logs in to the ServiceNow AI Platform.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) The user cookies being active for an indefinite amount of time is a security risk and should expire on a time-based configuration.

</td></tr><tr><td>

References

</td><td>

[Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) [Remember me](../../login/concept/c_ChSetRemMeChkbxCookie.md#)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Session management](sc-session-management.md)

