---
title: Minimize reset password max SMS per day
description: Manage the maximum number of SMS codes sent for verification per day by user.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize reset password max SMS per day

Manage the maximum number of SMS codes sent for verification per day by user.

The **password\_reset.sms.max\_per\_day** system property determines the maximum number of SMS codes sent for verification per day for a user.

Set the property **password\_reset.sms.max\_per\_day** to a value of `` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.sms.max\_per\_day**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

iIteger

</td></tr><tr><td>

Recommended value

</td><td>

10

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

5

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: If the value is too high, it's easier for attackers to brute force the SMS code.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

