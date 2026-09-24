---
title: Activate role based multi-factor authentication
description: Use the glide.authenticate.multifactor property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-role-based-multi-factor-authentication.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Activate role based multi-factor authentication

Use the **glide.authenticate.multifactor** property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.

The **glide.authenticate.multifactor** property enforces multi-factor authentication \(MFA\) based on the roles assigned to the user. When set to **true**, the platform enforces role-based MFA for all users whose roles are listed in the Multi-factor Criteria \[multi\_factor\_criteria\] table.

The Multi-factor Criteria \[multi\_factor\_criteria\] table defines which roles require MFA authentication. If a user has been assigned admin, security\_admin or user\_admin roles in the multi-factor roles list, MFA is enforced.

Enforcing MFA based on roles strengthens authentication security and aligns with best practices for protecting privileged accounts.

-   Navigate to /sys\_properties\_list.do on the instance and verify that the **glide.authenticate.multifactor** property exists and is set to `true`.

-   Navigate to `/multi_factor_criteria_list.do` on the instance and verify that the **Role based multi-factor authentication** record has **Active** set to **true**.


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

-   false
-   The Multi-factor Criteria \[multi\_factor\_criteria\] table record with sys\_id `d427668b73003300fdbd04fbc4f6a7b6` is shipped in a zbooted instance but is not set to active

</td></tr><tr><td>

Fallback value

</td><td>

-   false
-   The Multi-factor Criteria \[multi\_factor\_criteria\] table record with sys\_id `d427668b73003300fdbd04fbc4f6a7b6` has the **Active** field unselected.

</td></tr><tr><td>

Category

</td><td>

[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.7
-   CVSS rating: Medium
-   Security risk details: Enforcing MFA based on roles strengthens authentication security. This approach aligns with best practices for protecting privileged accounts.

</td></tr><tr><td>

Functional impact

</td><td>

Users assigned the admin, security\_admin, or user\_admin role will be prompted for a second authentication factor at login, and their password. Users without one of these roles are unaffected.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

For role-based MFA enforcement to take effect, **glide.authenticate.multifactor** must be set to **true** and Multi-factor Criteria \[multi\_factor\_criteria\] must be active.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

