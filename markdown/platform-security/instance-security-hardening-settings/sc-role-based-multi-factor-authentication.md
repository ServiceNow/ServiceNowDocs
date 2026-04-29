---
title: Activate role based multi-factor authentication
description: Use the glide.authenticate.multifactor property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Activate role based multi-factor authentication

Use the **glide.authenticate.multifactor** property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.

The **glide.authenticate.multifactor** system property enforces multi-factor authentication based on the roles assigned to the user. If this property is set to **true**, then it enforces role-based multi-factor authentication for all users described in the Multi-factor Criteria \[multi\_factor\_criteria\] table. This table enforces multi-factor authentication based on the roles assigned to the user. If a user has been assigned admin, security\_admin or user\_admin roles in the multi-factor roles list, MFA is enforced.

Ensure that the property **glide.authenticate.multifactor** is set to **true** and that the Multi-factor Criteria \[multi\_factor\_criteria\] table has a **Role base multi-factor authentication** record with the **Active** field set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.authenticate.multifactor** system property
-   **Role base multi-factor authentication** record on the Multi-factor Criteria \[multi\_factor\_criteria\] table

</td></tr><tr><td>

Configuration type

</td><td>

-   System Properties \(/sys\_properties\_list.do\)
-   Multi-factor Criteria \(/multi\_factor\_criteria\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   Record configuration

</td></tr><tr><td>

Recommended value

</td><td>

-   true
-   The Multi-factor Criteria \[multi\_factor\_criteria\] table record with sys\_id `d427668b73003300fdbd04fbc4f6a7b6` should be present, with the **Active** field selected.

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   false
-   The Multi-factor Criteria \[multi\_factor\_criteria\] table record with sys\_id `d427668b73003300fdbd04fbc4f6a7b6` has the **Active** field unselected.

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.7
-   CVSS rating: Medium
-   Security risk details: Enforcing MFA based on roles strengthens authentication security and aligns with best practices for protecting privileged accounts.

</td></tr><tr><td>

Functional impact

</td><td>

Enabling this property improves the experience of the user. It acts as an extra layer of protection and security against compromised credentials.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

