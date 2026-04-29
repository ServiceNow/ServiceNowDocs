---
title: Maximize reset password SMS pause window duration
description: Manage the time duration in minutes that a user must wait before they can request a new password reset code.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password SMS pause window duration

Manage the time duration in minutes that a user must wait before they can request a new password reset code.

If the **password\_reset.sms.pause\_window** system property is not set to the recommended value of `2` minutes or greater, then a malicious user could initiate many password reset SMS codes in a brief window of time.

Ensure that the property **password\_reset.sms.pause\_window** is set to `2` or greater.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.sms.pause\_window**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer

</td></tr><tr><td>

Recommended value

</td><td>

2

</td></tr><tr><td>

Default value

</td><td>

2

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.8
-   CVSS score: Medium
-   Security risk details: This increases the attacker's likelihood of predicting the SMS reset code.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

