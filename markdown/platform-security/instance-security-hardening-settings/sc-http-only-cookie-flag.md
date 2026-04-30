---
title: Enable HTTP Only Cookie Flag \[Updated in Security Center 1.3\]
description: Use the glide.cookies.http\_only property to enable the HTTPOnly attribute for sensitive cookies.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Enable HTTP Only Cookie Flag \[Updated in Security Center 1.3\]

Use the **glide.cookies.http\_only** property to enable the HTTPOnly attribute for sensitive cookies.

Use the HTTPOnly attribute to prevent attacks, such as cross-site scripting, because it doesn't allow access to the cookie using a client-side script, such as JavaScript. It does not eliminate cross site scripting risks but does eliminate some exploitation vectors.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.cookies.http\_only**

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

To mitigate the risk of client-side script accessing the protected cookie.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

8

</td></tr><tr><td>

Functional impact

</td><td>

This remediation adds an extra HTTPOnly flag in on session cookies, thus protecting them from being stolen. -   If you have custom functionality that requires JavaScript to access the user's cookie, it breaks that functionality. It should not be the case under normal circumstances.
-   The ServiceNow AI Platform handles session management and there shouldn't be a reason for a custom script to access the user's cookies.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Session cookies in the application authenticate an end user and provide implicit access permissions on the application. That means there is a need to secure them from being stolen or exported. HTTP Only flags protect the session cookies from JavaScript injections or cross site scripting vulnerabilities stealing them.

</td></tr><tr><td>

References

</td><td>

[Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Session management](sc-session-management.md)

