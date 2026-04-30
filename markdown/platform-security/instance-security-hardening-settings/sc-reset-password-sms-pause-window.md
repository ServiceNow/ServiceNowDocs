---
title: Maximize reset password SMS pause window duration \[Updated in Security Center 1.3\]
description: Manage the time duration in minutes that a user must wait before they can request a new password reset code.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password SMS pause window duration \[Updated in Security Center 1.3\]

Manage the time duration in minutes that a user must wait before they can request a new password reset code.

If this property is not set to the recommended value of **2** minutes or more, then a malicious user could initiate many passwords reset codes in a brief window of time. This increases the chance of a bad actor predicting the SMS reset code.

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

integer

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
-   Security risk details: Ensure that **password\_reset.sms.pause\_window** is set to a value of 2 or more.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

