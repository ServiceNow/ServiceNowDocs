---
title: Limit basic authentication restriction allowed roles
description: The glide.authenticate.basic\_auth.allowed\_roles property defines roles that bypass the Basic Authentication Restriction gate without multi-factor authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-limit-basic-authentication-restriction-allowed-roles.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [basic authentication, MFA bypass, role-based access, security gate]
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Limit basic authentication restriction allowed roles

The **glide.authenticate.basic\_auth.allowed\_roles** property defines roles that bypass the Basic Authentication Restriction gate without multi-factor authentication.

This system property contains a comma-separated list of role names exempt from the [Basic authentication restriction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/basic-auth-restriction.md) gate. When restriction is active, any interactive-login user holding one of the listed roles can authenticate through Basic Auth without multi-factor authentication or time-based one-time password. This role check runs unconditionally, before enforcement-date tracking logic and before any per-account review in the Basic Auth Exception table. A role match is never logged as a tracked exception and always bypasses the gate regardless of whether enforcement is enabled.

The out-of-box value is the single, dedicated role **snc\_basic\_auth\_api\_access**. Management, Instrumentation, and Discovery \(MID\) Server accounts pass this check without being separately listed. The **mid\_server** role inherits **snc\_basic\_auth\_api\_access** through the platform role hierarchy, so a MID Server account transitively holds the allowed role without appearing in this property value.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Ensure the **glide.authenticate.basic\_auth.allowed\_roles** property is limited to snc\_basic\_auth\_api\_access or another narrowly-scoped, dedicated integration role. Remove any broadly-held role such as admin, itil, or snc\_internal.

## More information

<table id="table_property_details"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.basic\_auth.allowed\_roles**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String \(comma-delimited list\)

</td></tr><tr><td>

Recommended value

</td><td>

**snc\_basic\_auth\_api\_access**

</td></tr><tr><td>

Default value

</td><td>

**snc\_basic\_auth\_api\_access**

</td></tr><tr><td>

Fallback value

</td><td>

&lt;None&gt;

</td></tr><tr><td>

Category

</td><td>

[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS score: High
-   Security risk details:

If this property includes a widely-held role such as **admin**, **itil**, or **snc\_internal**, every user holding that role receives a permanent, unconditional bypass of the Basic Authentication Restriction gate.

This is not a temporary tracking-mode allowance. Unlike a per-account exception, which is logged and individually reviewed, role-based matches are never logged and never reviewed. An over-broad role grants silent, undetectable multi-factor authentication bypass to every current and future holder of that role. An attacker who obtains a valid password through phishing, credential stuffing, or a prior breach authenticates directly against the API without satisfying a second factor. This exposure extends to the entire population holding the listed role.


</td></tr><tr><td>

Functional impact

</td><td>

This property takes effect for users not already allowed through an earlier checks. Earlier checks include WSAO accounts, oauth\_token requests, an active TOTP or multi-factor authentication session, or the allowed\_users list.

 Keep the value limited to **snc\_basic\_auth\_api\_access** or another narrowly-scoped, dedicated integration role. This does not affect MID Server accounts. The mid-server role holds **snc\_basic\_auth\_api\_access** through role containment, independent of this property literal value. Removing a role from this list doesn't immediately deny access.

 Affected users fall through the same tracking and review flow as any other basic-auth user. This review process provides a safety net before actual denial takes effect. Before narrowing or auditing this property, confirm that any role kept in the list is a dedicated integration or service role, not one held by ordinary interactive users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Plugin **com.snc.integration.multifactor.authentication** must be Active. No effect unless **glide.authenticate.basic\_auth.restriction.active** is **true**.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

