---
title: Limit Allowed Number of Failed Login Attempts Before Lockout
description: Two script actions are available that enable a site administrator to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable either of these script actions to manage failed login attempts.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Limit Allowed Number of Failed Login Attempts Before Lockout

Two script actions are available that enable a site administrator to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable either of these script actions to manage failed login attempts.

The **SNC User Lockout Check** or **SNC User Lockout Check with Auto Unlock** script actions enable the administrator to manage the number of failed login attempts for a user. Two script actions are available that enable a site administrator to manage the number of times a user can provide correct password before getting locked out from the Now Platform.

Additionally, the **glide.user.max\_unlock\_attempts** system property controls the number of allowed failed login attempts. If the value of **glide.user.max\_unlock\_attempts** is increased above the recommended value of `5`, it increases the number of login attempts an attacker could make against a given user.

Ensure at least one of the script actions: **SNC User Lockout Check** or **SNC User Lockout Check with Auto Unlock** is enabled to manage failed login attempts. These script actions are stored in the Script Actions \[sysevent\_script\_action\] table.

Additionally, ensure the property **glide.user.max\_unlock\_attempts** is set to `5` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **SNC User Lockout Check** \(Script action\)
-   **SNC User Lockout Check with Auto Unlock** \(Script action\)
-   **glide.user.max\_unlock\_attempts**\(System property\)

</td></tr><tr><td>

Configuration type

</td><td>

-   Script Action \(/sysevent\_script\_action.do\)
-   System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer \(for system property\)

</td></tr><tr><td>

Recommended value

</td><td>

-   The Script Actions \[sysevent\_script\_action\] table has the record with sys\_id `5e44f9bf0a0a0a0a019a6440b2137767` and/or the record with sys\_id `d92636b2975301008e00958e3b297567` set to **active**
-   **glide.user.max\_unlock\_attempts** system property is set to an integer less than or equal to 5.

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

5 \(for system property\)

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.3
-   CVSS rating: High
-   Security risk details: Allowing more attempts gives attackers additional opportunities to guess passwords, increasing the likelihood of unauthorized access and credential compromise. Proper lockout configuration is critical to maintaining strong authentication security.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

