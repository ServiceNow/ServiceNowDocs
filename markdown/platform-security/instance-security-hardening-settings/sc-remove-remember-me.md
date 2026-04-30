---
title: Remove remember me
description: Use the glide.ui.forgetme property to remove the Remember Me check box from the login page to prevent login information from being cached.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Remove remember me

Use the **glide.ui.forgetme** property to remove the **Remember Me** check box from the login page to prevent login information from being cached.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.forgetme**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Data protection](sc-data-protection.md)

</td></tr><tr><td>

Purpose

</td><td>

To ensure that no authentication information is cached.

</td></tr><tr><td>

Security risk rating

</td><td>

3.5

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Functional Impact

</td><td>

This remediation would change the user experience by automatically logging them out of the instance when their session expires. The session expiration would solely depend on the value set in the system property as detailed in [Managing user sessions](https://www.servicenow.com/docs/access?context=c_ManageUserSessions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Security risk

</td><td>

\(Low\) When you select the **Remember me** check box at login, an extra cookie is stored on the user's computer. -   Its purpose is to automatically re-establish the session for the subsequent visits of the logged-in user.
-   It poses a security risk as it allows the user session to be active until they deliberately log out. The likelihood of an attack for this scenario increases when the end user has left the browser unattended, or if it is compromised from a different attack.

</td></tr><tr><td>

References

</td><td>

[Remove the Remember me check box](../../login/concept/c_ChSetRemMeChkbxCookie.md#)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

**Parent Topic:**[Data protection](sc-data-protection.md)

