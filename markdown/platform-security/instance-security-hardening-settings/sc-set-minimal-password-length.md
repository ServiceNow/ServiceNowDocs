---
title: Set minimal password length \[Removed in Security Center 2.0\]
description: Set the minimum length for a user password on your instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Set minimal password length \[Removed in Security Center 2.0\]

Set the minimum length for a user password on your instance.

The **set.password.length** property defines the minimum length required for a password and is used to evaluate compliance against the current password policy. The property value is an integer with a minimum recommended value of **12**. Using a shorter length could lead to compliance failure against recommended regulations.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**set.password.length**

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

12

</td></tr><tr><td>

Default value

</td><td>

12

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: Setting the property to less than a value of 12 could lead to compliance issues and increases the risk of an attacker successfully brute forcing passwords.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

