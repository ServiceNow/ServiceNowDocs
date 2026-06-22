---
title: Remove remember me
description: Use the glide.ui.forgetme property to remove the Remember Me check box from the login page to prevent login information from being cached.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-remove-remember-me.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
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

[Data protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-data-protection.md)

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

Functional impact

</td><td>

This remediation would change the user experience by automatically logging them out of the instance when their session expires. The session expiration would solely depend on the value set in the system property as detailed in [Managing user sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/user-administration/c_ManageUserSessions.md).

</td></tr><tr><td>

Security risk

</td><td>

\(Low\) When you select the **Remember me** check box at login, an extra cookie is stored on the user's computer. -   Its purpose is to automatically re-establish the session for the subsequent visits of the logged-in user.
-   It poses a security risk as it allows the user session to be active until they deliberately log out. The likelihood of an attack for this scenario increases when the end user has left the browser unattended, or if it is compromised from a different attack.

</td></tr><tr><td>

References

</td><td>

[Remove the Remember me check box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/c_ChSetRemMeChkbxCookie.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md)

**Parent Topic:**[Data protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-data-protection.md)

