---
title: Enable a deny-list password validation check
description: Manage the deny-list passwords in the Excluded Password table.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable a deny-list password validation check

Manage the deny-list passwords in the Excluded Password table.

Use the **glide.enable.blacklist\_password** property to monitor deny-list passwords. When the property is set to `true`, the user's password is checked against a specific list of deny-listed passwords. This denial prevents users from using a password from a set of breached passwords. You can maintain the list by inserting passwords into the Excluded Password \[blacklisted\_password\] table. ServiceNow provides a small, medium, or large password list that can be inserted to the Excluded Password table through the UI page found at **All** &gt; **Password Policy** &gt; **Exclusion List Management**. ServiceNow installs the small list of 5,000 passwords to new instances.

Ensure that the **glide.enable.blacklist\_password** system property is set to `true` and that the Excluded Password \[blacklisted\_password\] table contains a minimum of 5,000 records.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.enable.blacklist\_password** system property
-   **Excluded Password \[blacklisted\_password\]** table

</td></tr><tr><td>

Configuration type

</td><td>

-   System Properties \(/sys\_properties\_list.do\)
-   Table record \(/blacklisted\_password\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   Table record

</td></tr><tr><td>

Recommended value

</td><td>

-   true
-   A minimum of 5,000 records

</td></tr><tr><td>

Default value

</td><td>

-   true
-   ServiceNow provided list of 5,000 records

</td></tr><tr><td>

Fallback Value

</td><td>

-   false
-   ServiceNow provided list of 5,000 records

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: Attackers often target commonly used or previously exposed passwords. This can lead to account compromise through credential stuffing or brute-force attacks. Enforcing deny-listed password checks strengthens authentication security and reduces exposure to credential-based attacks.

</td></tr><tr><td>

Functional Impact

</td><td>

Some users may have difficulty selecting a password.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Exclude passwords through password policies on your instance](../../../integrate/authentication/task/blacklist-passwords.md)

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

