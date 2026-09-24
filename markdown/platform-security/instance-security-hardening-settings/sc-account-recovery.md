---
title: Enable account recovery
description: Use the glide.sso.acr.enabled property to manage the account recovery feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-account-recovery.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable account recovery

Use the **glide.sso.acr.enabled** property to manage the account recovery feature.

The **glide.sso.acr.enabled** property controls whether the Account Recovery \(ACR\) feature is available on an instance configured for Single Sign-On \(SSO\) authentication. When set to the recommended value of **true**, the platform blocks turning on multi-SSO until account recovery is enabled. At least one user account is enrolled for it. It confines any session authenticated through the recovery path to writing only SSO and account-recovery-related configuration. This preserves a controlled, auditable path back into the system for users who lose access to their normal SSO credentials.

Verify that the property **glide.sso.acr.enabled** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sso.acr.enabled**

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

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details: Without an account recovery path, a user who loses access to their normal sign-in method has no supported way back into the system. That gap commonly pushes administrators and help desks toward manual, ad hoc identity verification workarounds to restore access. Those workarounds are a well-known target for social engineering and account takeover because they bypass the organization's standard authentication controls. Leaving a recovery path unavailable increases the risk of unauthorized account access and loss of control over who can regain entry to affected accounts.

</td></tr><tr><td>

Functional impact

</td><td>

Enabling this control doesn't disable SSO. It requires that an account-recovery path exist and restricts write access on a recovery-authenticated session to SSO- and recovery-related properties only. Admin users that have never configured account recovery, or that have zero users enrolled, are blocked from turning on Multi-SSO until at least one user opts in. Users may test the Multi-SSO activation flow and the account-recovery login flow when removing or disabling ACR-enrolled users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

SSO is enabled \(the property **glide.authenticate.multisso.enabled** is set to `true`\).

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

