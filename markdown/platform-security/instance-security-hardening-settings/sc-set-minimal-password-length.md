---
title: Require Minimum and Maximum Password Length
description: Set minimum and maximum password lengths to avoid compliance issues and reduce the risk of a successful brute force attack
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Require Minimum and Maximum Password Length

Set minimum and maximum password lengths to avoid compliance issues and reduce the risk of a successful brute force attack

Password policies define the requirements for passwords your users create on your instance. The password length must fall within the range accepted by the NIST 800-63B document.

Ensure that a password policy is being enforced for each password credential store in use on your instance. Ensure that the password policy mandates a minimum password length of at least 15 characters and maximum password length of at least 64 characters.

For each password credential store record in the Password Reset Credential Stores \[pwd\_cred\_store\] table:

1.  Ensure that a password policy is being enforced for each password credential store in use on your instance:

    For each password credential store record in the Password Reset Credential Stores \[pwd\_cred\_store\] table, ensure that **Enable password policy** field is activated.

2.  Ensure that the password policy mandates a minimum password length of at least 15 characters and maximum password length of at least 64 characters.

    Navigate to the Password Policy \[password\_policy\] record referenced in the record's **Password policy** field. Ensure that the **Minimum Password Length** field is set to at least 15 and **Maximum Password Length** field is set to at least 64.

3.  Further instructions on configuring a password policy can be in the documentation: [Enable password policies on your instance](../../../integrate/authentication/task/enable-password-policies.md)

Further instructions on configuring a password policy, see [Enable password policies on your instance](../../../integrate/authentication/task/enable-password-policies.md).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   Password Reset Credential Store \[pwd\_cred\_store\] table
-   Password Policy \[password\_policy\]

</td></tr><tr><td>

Configuration type

</td><td>

-   Table records
-   Table records

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   Integer

</td></tr><tr><td>

Recommended value

</td><td>

-   The **Enable password policy** field on each Password Reset Credential Stores \[pwd\_cred\_store\] record must be activated\(true\).
-   The **Minimum Password Length** on the associated Password Policy \[password\_policy\] record must be at least 15.
-   The **Maximum Password Length** on the associated Password Policy \[password\_policy\] record must be equal or less than 64.

</td></tr><tr><td>

Default value

</td><td>

-   The **Minimum Password Length** on Password Policy \[password\_policy\] records is 8 by default.
-   The **Maximum Password Length** on Password Policy \[password\_policy\] records is 100 by default.

</td></tr><tr><td>

Fallback value

</td><td>

-   The fallback value of **Minimum Password Length** on Password Policy \[password\_policy\] records is 8.
-   The fallback value of **Maximum Password Length** on Password Policy \[password\_policy\] record is 100.

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS score: Medium
-   Security risk details: Allowing passwords that are too short or not long enough could lead to compliance issues and increases the risk of an attacker successfully brute forcing passwords.

</td></tr><tr><td>

Functional impact

</td><td>

Instances do not suffer any impact from a minimum password length of 15 or maximum password length of 64.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

