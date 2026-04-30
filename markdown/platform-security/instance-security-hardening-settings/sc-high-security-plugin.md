---
title: Enable High Security Plugin \[Updated in Security Center 1.3\]
description: When you activate the High Security plugin, it creates or updates hundreds of different configurations to control the level of security on your instance. These configurations mitigate many of the top OWASP attacks by enabling strict access control, input validation, and output encoding.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable High Security Plugin \[Updated in Security Center 1.3\]

When you activate the High Security plugin, it creates or updates hundreds of different configurations to control the level of security on your instance. These configurations mitigate many of the top OWASP attacks by enabling strict access control, input validation, and output encoding.

These configurations include:

-   Access Control
-   Business rules
-   System properties
-   UI policy action
-   script actions
-   script includes

## Example

Refer to the examples for the following properties:

|Property|Topic|
|--------|-----|
|glide.ui.escape\_all\_script|[Escape jelly script \[Updated in Security Center 1.3 and 1.5\]](sc-escape-jelly.md)|
|glide.security.strict.actions|[Check UI action conditions before execution](sc-check-ui-action-conditions-before-execution.md)|
|glide.security.csrf\_previous.allow|[Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]](sc-anti-csrf-token.md)|
|glide.security.csrf.strict.validation.mode|[Prevent Users From Accepting Warning To Bypass CSRF Validation \[Updated in Security Center 1.3 and 1.5\]](sc-csrf-strict-validation.md)|

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Plugin Name

</td><td>

com.glide.high\_security

</td></tr><tr><td>

Configuration type

</td><td>

System Definition &gt; Plugins - Development

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

It is mandatory to activate this plugin. It increases the security level of an instance, which reduces the attack surface by mitigating owasp top 10 attacks, including CSRF, XSS, Securing Session Cookies, and File uploads.

</td></tr><tr><td>

Recommended value

</td><td>

Active

</td></tr><tr><td>

Security risk rating

</td><td>

9.8

</td></tr><tr><td>

Functional impact

</td><td>

This plugin enables several system security configurations, which may impact UI and functionality as well.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Many security configurations are unintentionally left open, which may open the door for some of the critical vulnerabilities.

</td></tr><tr><td>

References

</td><td>

[Activating High Security Settings](../../security/task/t_ActivateHighSecuritySettings.md)

 [High Security Settings](../../security/concept/c_HighSecuritySettings.md)

</td></tr></tbody>
</table>To learn more about activating a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

**Parent Topic:**[Access control](sc-access-control.md)

