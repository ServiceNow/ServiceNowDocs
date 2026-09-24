---
title: Enable basic authentication restriction
description: The glide.authenticate.basic\_auth.restriction.active property controls whether the platform evaluates inbound basic-auth API requests against allowed access paths.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-basic-auth-restriction.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable basic authentication restriction

The **glide.authenticate.basic\_auth.restriction.active** property controls whether the platform evaluates inbound basic-auth API requests against allowed access paths.

This property controls the [Basic authentication restriction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/basic-auth-restriction.md) gate. This gate evaluates inbound basic-auth API requests \(username + password\) from interactive-login accounts. When set to `true`, the gate evaluates each request against allowed access paths. When set to `false`, every basic-auth API request bypasses evaluation.

**Important:** Set to `false` only as a temporary emergency measure—for example, to restore basic-auth access during an active security investigation. Revert to `true` as soon as the emergency resolves.

## More information

<table id="table_lzs_xpx_2kcb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.basic\_auth.restriction.active**

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

[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details:

When set to `false`, accounts that authenticate interactively through the browser or service portal can also authenticate to the API using only a username and password. This bypasses any multi-factor authentication that would otherwise be required for those accounts' interactive logins.

This creates a credential-compromise attack path: an attacker who obtains a valid password through phishing, credential stuffing, or a prior breach can use it directly against the API without satisfying a second factor. Leaving this property set to false for an extended period removes multi-factor authentication \(MFA\) protection for every interactive-login account, substantially increasing the risk of account takeover.


</td></tr><tr><td>

Functional impact

</td><td>

When set to `true` for the first time, the basic authentication restriction starts in tracking mode. Basic-auth requests are recorded \(not restricted\) in the exception table \(sys\_user\_basic\_auth\_exception\) for admin review. Actual restriction begins once the separate enforcement mechanism activates, at which point users who don't qualify under an allowed access path are denied access.

 If this property was previously set to `false` after enforcement began, setting it back to `true` resumes enforcement immediately. Tracking mode doesn't start.

 Before enforcement begins, administrators must review the exception table. Set an appropriate decision for each listed account. Convert integration accounts to Web Service Access Only where possible.

 Setting this property to `false` after enforcement has begun immediately restores unrestricted basic-auth access for every account including previously-restricted accounts. Set it back to `true` as soon as any investigation is complete.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.snc.integration.multifactor.authentication** plugin must be active.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

