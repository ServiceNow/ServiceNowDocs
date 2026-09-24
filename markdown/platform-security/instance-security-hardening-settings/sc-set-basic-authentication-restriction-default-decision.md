---
title: Set basic authentication restriction default decision
description: The glide.authenticate.basic\_auth.restriction.default\_decision property controls the automatic decision applied to basic-auth accounts during the Basic Authentication Restriction tracking period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-set-basic-authentication-restriction-default-decision.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [basic authentication, authentication restriction, system property, MFA, web service access]
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Set basic authentication restriction default decision

The **glide.authenticate.basic\_auth.restriction.default\_decision** property controls the automatic decision applied to basic-auth accounts during the Basic Authentication Restriction tracking period.

This property sets the decision automatically applied to a basic-auth account the first time it is detected during the [Basic authentication restriction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/basic-auth-restriction.md) tracking period. This decision also applies to any account whose per-row entry in the Basic Auth Exception table is explicitly left as Apply default from system property.

Three outcomes are available:

-   **Maintain current login**: Keeps unrestricted basic-auth access.
-   **Revoke Basic Auth API login**: Blocks API basic-auth once enforcement begins. UI login is unaffected.
-   **Convert to web service access only account**: Keeps basic-auth API access but blocks interactive UI login for that account, satisfying multi-factor authentication \(MFA\) policy because it no longer has an interactive session to protect.

## More information

<table id="table_7ou_ijk_2ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.basic\_auth.restriction.default\_decision**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

</td></tr><tr><td>

Data type

</td><td>

String \(Choice list\)

</td></tr><tr><td>

Recommended value

</td><td>

Revoke Basic Auth API login-Basic Auth API login blocked; UI login allowed

</td></tr><tr><td>

Default value

</td><td>

Maintain current login-Basic Auth API and UI login allowed

</td></tr><tr><td>

Fallback value

</td><td>

Maintain current login-Basic Auth API and UI login allowed

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

When left at the default `Maintain current login`, two groups of accounts automatically keep unrestricted basic-auth API access. The first group: accounts first detected using basic auth during tracking. The second group: accounts an administrator leaves on `Apply default from system property`. Neither group satisfies multi-factor authentication \(MFA\) once enforcement begins.

This creates the same credential-abuse exposure as any unrestricted basic-auth account. An attacker who obtains a valid password can use it directly against the API. They bypass the MFA that would otherwise protect interactive login.

Because this is the default applied to unreviewed accounts, an instance that runs through tracking without changing this property grandfathers every detected account into permanent MFA bypass. This requires no deliberate administrator action.


</td></tr><tr><td>

Functional impact

</td><td>

This property only takes effect for exception-table rows resolved to **Apply default from system property**. Any per-account decision in the exception table overrides this system property default.

 Changing the default to `Revoke` means any account an administrator has not yet explicitly reviewed will lose basic-auth API access once enforcement begins. UI login remains unaffected.

 Before or immediately after changing this default, complete the review of the Basic Auth Exception table:

 1.  Convert genuine integration accounts to Web Service Access \(WSO\) Only
2.  Explicitly grant continued access only where justified

 Completing this review confirms unreviewed accounts retain API access.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

