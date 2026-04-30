---
title: Minimize reset password SMS expiracy duration \[Updated in Security Center 1.3\]
description: Control the number of minutes remaining before the SMS code expires.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize reset password SMS expiracy duration \[Updated in Security Center 1.3\]

Control the number of minutes remaining before the SMS code expires.

The **password\_reset.sms.expiry** property represents the number of minutes remaining before the SMS code expires.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.sms.expiry**

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

5

</td></tr><tr><td>

Default value

</td><td>

5

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.6
-   CVSS score: Medium
-   Security risk details: If this property is not set to the recommended value of **5** or less, the chances of a bad actor guessing and using the SMS code to reset the password increases.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

