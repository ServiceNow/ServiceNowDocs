---
title: Minimize reset password max SMS per day \[Updated in Security Center 1.3\]
description: Manage the maximum number of SMS codes sent for verification per day by user.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize reset password max SMS per day \[Updated in Security Center 1.3\]

Manage the maximum number of SMS codes sent for verification per day by user.

The **password\_reset.sms.max\_per\_day** property represents the maximum number of SMS codes that can be sent for verification daily by a user.

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

integer

</td></tr><tr><td>

Recommended value

</td><td>

10

</td></tr><tr><td>

Default value

</td><td>

10

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: If this property is not set to the recommended value of **10** or less, it's easier to brute force the SMS code.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

