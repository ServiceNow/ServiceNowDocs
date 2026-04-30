---
title: Minimize absolute session timeout duration \[Updated in Security Center 1.3\]
description: Use the glide.ui.user\_cookie.max\_life\_span\_in\_days property to set a maximum life span for user cookies created when users log in with the Remember Me checkbox selected. When the cookie expires, users who have selected the Remember Me checkbox are forced to reauthenticate into the instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize absolute session timeout duration \[Updated in Security Center 1.3\]

Use the **glide.ui.user\_cookie.max\_life\_span\_in\_days** property to set a maximum life span for user cookies created when users log in with the **Remember Me** checkbox selected. When the cookie expires, users who have selected the **Remember Me** checkbox are forced to reauthenticate into the instance.

It enables the user cookie to be valid for the duration of specified days, starting when the cookie was first issued. The default value is 30 days, and the maximum cap is at 365 days.

**Note:** To enforce a maximum session time for any active user sessions, see [Managing user sessions](https://www.servicenow.com/docs/access?context=c_ManageUserSessions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.user\_cookie.max\_life\_span\_in\_days**

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

To force users who have selected the **Remember Me** checkbox to reauthenticate after specific days.

</td></tr><tr><td>

Recommended value

</td><td>

Less than or equal to 30

</td></tr><tr><td>

Default value

</td><td>

30 days

</td></tr><tr><td>

Functional impact

</td><td>

This property enforces mandatory relogin by avoiding any sort of cookie rotation after a given timeframe.

</td></tr><tr><td>

Security risk rating

</td><td>

4.2

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\) The user cookies being active for an indefinite amount of time is a security risk and should expire on a time-based configuration.

</td></tr><tr><td>

References

</td><td>

[Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) [Remember me](../../login/concept/c_ChSetRemMeChkbxCookie.md#)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Session management](sc-session-management.md)

