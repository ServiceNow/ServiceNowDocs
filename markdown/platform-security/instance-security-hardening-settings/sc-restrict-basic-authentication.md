---
title: Restrict basic authentication external role exemption
description: The glide.authenticate.basic\_auth.allow\_snc\_external property controls whether users with the snc\_external role are exempt from the basic authentication restriction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-restrict-basic-authentication.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Restrict basic authentication external role exemption

The **glide.authenticate.basic\_auth.allow\_snc\_external** property controls whether users with the snc\_external role are exempt from the basic authentication restriction.

The snc\_external role is the base role for all external users of the instance—customers and portal constituents. Unlike the other exception checks in the [Basic authentication restriction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/basic-auth-restriction.md) gate, this check returns unconditionally. When a user holds this role, the value of the **glide.authenticate.basic\_auth.allow\_snc\_external** property is the sole, final determinant of whether that request is allowed. The property doesn't fall back to `allowed_users`, `allowed_roles`, or the `enforcement-date` tracking flow.

External and portal users have normal interactive sessions. They can complete multi-factor authentication \(MFA\) enrollment through the standard UI flow. Nothing in the platform blocks them from MFA enrollment the way Web Service Access Only \(WSAO\) accounts are blocked. Whether an external user is exempt from MFA is governed by a separate, admin-configured MFA context policy mechanism, not a technical requirement. This property doesn't compensate for a population that structurally can't satisfy MFA.

## Before enforcing this restriction

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Identify any integration or automation accounts that hold the `snc_external` role and use Basic Auth. Migrate them to a dedicated integration role or WSAO status.
3.  Set the **glide.authenticate.basic\_auth.allow\_snc\_external** property to `false`.

## More information

<table id="table_a7c_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.basic\_auth.allow\_snc\_external**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

</td></tr><tr><td>

Category

</td><td>

[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Functional impact

</td><td>

Setting this property to `false` requires all `snc_external` users to satisfy MFA \(or use allowed\_users, allowed\_roles paths\) to continue using Basic Auth.

 Before disabling, verify that external integrations or automation accounts don't depend on this role. Migrate service accounts to a dedicated integration role or WSAO status instead.

</td></tr><tr><td>

Security risk

</td><td>

-   CVSS score: 8.1
-   CVSS rating: High
-   The external-role check returns unconditionally. Leaving the `glide.authenticate.basic_auth.allow_snc_external` property at its default value of `true` grants every `snc_external` user an unconditional, unlogged Basic Authentication Restriction gate bypass. This applies to the entire external and customer-facing population. These users gain access regardless of MFA enrollment.

This covers a broader population than other exception mechanisms in this control family. Unlike WSAO accounts, these users can enroll in MFA. The exemption here is a compatibility allowance, not a technical necessity. An attacker who obtains an external-role password can authenticate directly against the API. No second factor is required.


</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Takes effect only when **glide.authenticate.basic\_auth.restriction.active** is `true`.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

