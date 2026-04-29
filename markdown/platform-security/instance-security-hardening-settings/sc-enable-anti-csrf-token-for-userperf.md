---
title: Enable Anti-CSRF Token for Userperf
description: Use a system property to ensure CSRF \(Cross-Site Request Forgery\) protection is enforced when setting user preferences.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enable Anti-CSRF Token for Userperf

Use a system property to ensure CSRF \(Cross-Site Request Forgery\) protection is enforced when setting user preferences.

Use the **glide.security.userpref\_csrf\_check.enable** system property to enforce CSRF \(Cross-Site Request Forgery\) protection when setting user preferences to the User Preference Definitions \[sys\_user\_preference\_definition\] table via URI parameters. If the property isn't set to the recommended value of `true`, then the **CSRF token required** flag is overridden when set on individual preferences, and preferences can be set via URI parameters without requiring a CSRF token.

Ensure the **glide.security.userpref\_csrf\_check.enable** system property is set to `true`.

## More information

<table id="table_ygy_csn_rhc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.userpref\_csrf\_check.enable**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: Failure to implement CSRF protection exposes the instance to unauthorized actions performed on behalf of authenticated users.

</td></tr><tr><td>

Functional Impact

</td><td>

Users or integrations that previously set certain preferences via URL parameters without a CSRF token may now fail if those preferences require a token.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

