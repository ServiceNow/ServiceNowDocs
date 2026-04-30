---
title: Maximize failed login unlock timeout duration \[Updated in Security Center 1.3\]
description: A script action is available that enables site administrators to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable this script action to manage failed login attempts.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize failed login unlock timeout duration \[Updated in Security Center 1.3\]

A script action is available that enables site administrators to manage the number of times a user can provide an incorrect password before being locked out from the ServiceNow AI Platform. You can enable this script action to manage failed login attempts.

Help secure your instance against brute force attacks by defining a time period during which a user cannot attempt to log in after being locked out. The **glide.user.unlock\_timeout\_in\_mins** system property unlocks the user account after the time period that is specified in it's value. If no value is specified, your instance unlocks the user account after the default period of 15 minutes.

Set the **glide.user.unlock\_timeout\_in\_mins** system property value to a minimum of **15**. If **glide.user.unlock\_timeout\_in\_mins** does not exist, the default lockout time is set to 15 minutes.

Ensure that the **SNC User Lockout Check with Auto Unlock** script action \(found on the Script Action \[sysevent\_script\_action\] table\) is present and active. The **SNC User Lockout Check with Auto Unlock** script action is installed with the High Security Settings \(com.glide.high\_security\) plugin.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   glide.user.unlock\_timeout\_in\_mins \(System Property\)
-   sysevent\_script\_action \(Script Action\)

</td></tr><tr><td>

Configuration type

</td><td>

System Policy &gt; Script Actions

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Purpose

</td><td>

To enforce strict policy for failed login attempts to avoid brute forcing of credentials.

</td></tr><tr><td>

Recommended value

</td><td>

-   **15** for the **glide.user.unlock\_timeout\_in\_mins** system property
-   **Active** for the **SNC User Lockout Check with Auto Unlock** script action.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation would enable administrator of the instance to monitor and report any malicious user access. No functionality impact, only User experience change.

</td></tr><tr><td>

Security risk

</td><td>

-   Severity Score: 6.8
-   Security Risk Details: If the property is not configured to a secure value and the lockout duration is not enabled, then it may be easier to brute force account logins in a faster time frame. This may allow a malicious user to eventually obtain unauthorized access to the instance. Impact on the instance will be limited to the privileged of the affected user login brute-forced.

</td></tr></tbody>
</table>## Steps to configure

1.  Navigate to **System Policy** &gt; **Script Actions.**
2.  Search for the name **\*SNC User**.
3.  To enable management of failed login attempts, change the Active state of either the **SNC User Lockout Check with Auto Unlock** or **SNC User Lockout Check** scripts actions from **false** to **true**.
4.  To reset the failed login counter after a successful login, you can activate the **SNC User Clear** script action.

**Parent Topic:**[Authentication](sc-authentication.md)

