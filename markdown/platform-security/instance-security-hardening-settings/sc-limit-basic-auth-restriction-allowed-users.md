---
title: Limit basic authentication restriction allowed users
description: The glide.authenticate.basic\_auth.allowed\_users property defines specific user accounts that bypass the Basic Authentication Restriction gate without multi-factor authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-limit-basic-auth-restriction-allowed-users.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [basic authentication, MFA bypass, user exemption, security gate]
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Limit basic authentication restriction allowed users

The **glide.authenticate.basic\_auth.allowed\_users** property defines specific user accounts that bypass the Basic Authentication Restriction gate without multi-factor authentication.

This system property contains a comma-separated list of user sys\_ids exempt from the [Basic authentication restriction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/basic-auth-restriction.md) gate. When restriction is active, any interactive-login user whose sys\_id appears in this list can authenticate through Basic Auth without multi-factor authentication or time-based one-time password. This user check runs unconditionally, before enforcement-date tracking logic and before any per-account review in the Basic Auth Exception table. A user match is never logged as a tracked exception and always bypasses the gate regardless of whether enforcement is enabled.

The out-of-box value is empty, so no account is exempted unless an administrator explicitly adds one. This property is intended for narrowly-scoped integration accounts that cannot satisfy multi-factor authentication requirements and do not hold a role listed in the allowed\_roles property.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Ensure the **glide.authenticate.basic\_auth.allowed\_users** property contains only sys\_ids for dedicated integration accounts with a documented business justification. Remove any account that no longer requires a standing MFA exemption for Basic Auth API access.

## More information

<table id="table_property_details-limit-basic-auth-restriction-allowed-users"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.basic\_auth.allowed\_users**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String \(comma-delimited list of sys\_ids\)

</td></tr><tr><td>

Recommended value

</td><td>

&lt;Empty&gt; or limited to specific, individually-reviewed dedicated service accounts

</td></tr><tr><td>

Default value

</td><td>

&lt;Empty&gt;

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

Any user sys\_id added to this property receives a permanent, unconditional bypass of the Basic Authentication Restriction gate for that one account. This is not a temporary tracking-mode allowance. Unlike an account left to the default review flow, a listed sys\_id is never logged and never subject to further review. That account permanently loses multi-factor authentication protection on its Basic Auth API access.

An attacker who obtains that account's password through phishing, credential stuffing, or a prior breach can authenticate directly against the API without satisfying a second factor. Entries are added by sys\_id rather than username. A stale entry can silently persist and continue exempting an account long after the original justification for adding it is gone. Nothing in the property's own value indicates which account it refers to.


</td></tr><tr><td>

Functional impact

</td><td>

This property takes effect for users not already allowed through an earlier check. Earlier checks include WSAO accounts, oauth\_token requests, an active TOTP or multi-factor authentication session, or the allowed\_roles list.

 Because this property ships empty, any populated entry is always a deliberate administrator action, never an inherited default. Removing a sys\_id from this list does not deny that account access outright. Affected users fall through to the same allowed\_roles check and enforcement-date tracking-mode review flow as any other basic-auth user. There is a review safety net before actual denial takes effect.

 Administrators should periodically re-validate every sys\_id in this list against a live user record. Confirm each is still a legitimate, currently-needed integration account rather than a stale holdover. A bare sys\_id gives no indication of which account it names.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Plugin **com.snc.integration.multifactor.authentication** must be Active. No effect unless **glide.authenticate.basic\_auth.restriction.active** is **true**.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

