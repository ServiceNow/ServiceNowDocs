---
title: Prevent Reuse of REST API Sessions in UI/Web
description: Prevent REST API session cookies from bypassing Single Sign-On \(SSO\) and Multi-Factor Authentication \(MFA\) controls using a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Prevent Reuse of REST API Sessions in UI/Web

Prevent REST API session cookies from bypassing Single Sign-On \(SSO\) and Multi-Factor Authentication \(MFA\) controls using a system property.

Use the **com.glide.processors.aprocessor.donot\_reuse\_api\_session** to help prevent the cookies associated with the session created through the REST API from being reused to initiate UI/web sessions.

Verify that **com.glide.processors.aprocessor.donot\_reuse\_api\_session** exists in the System Properties \[sys\_properties\] table and is set to `true`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.processors.aprocessor.donot\_reuse\_api\_session**

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

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: Reusing REST API session cookies for a web session bypasses Single Sign-On \(SSO\) and Multi-Factor Authentication \(MFA\) controls. This bypass can be an escalation of intended privileges. SSO and MFA controls are important requirements to help prevent unauthorized access to data.

</td></tr><tr><td>

Functional impact

</td><td>

When **com.glide.processors.aprocessor.donot\_reuse\_api\_session** is set to true:

 -   API session cookies can no longer be reused to initiate web sessions.
-   All web sessions require full authentication \(SSO/MFA\), regardless of any existing API session.

 Potential Breakage:

 -   Custom integrations, scripts, or legacy workflows that relied on the ability to transition from an API session to a web session without re-authentication will fail.
-   Automated processes or tools that previously bypassed SSO/MFA using API session cookies are forced to complete the full authentication flow.
-   Users may experience unexpected authentication prompts if their workflows were implicitly relying on this behavior.

 Before enabling, customers should review integrations and customizations:

 -   Audit all integrations, scripts, and tools that interact with the instance via API and web interfaces.
-   Identify any that may be relying on session cookie reuse for seamless transitions between API and web sessions.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

