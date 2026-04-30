---
title: Enable Jelly JS Interpolation Protection
description: Use the glide.ui.jelly.js\_interpolation.protect property to ensure that any JavaScript about to be executed on a Jelly page is protected from injection with the help of Jelly interpolation.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable Jelly JS Interpolation Protection

Use the **glide.ui.jelly.js\_interpolation.protect** property to ensure that any JavaScript about to be executed on a Jelly page is protected from injection with the help of Jelly interpolation.

When you set property to **true**, an application goes through a Jelly script tree \(nested\). It wraps potentially dangerous Jelly expressions with a filter that:

-   Escapes their results to be safe, or
-   If their safety can't be guaranteed, generates a SecurityException because the expression that was going to be evaluated represents a possible security issue.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.jelly.js\_interpolation.protect**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

To mitigate against malicious code execution attacks that can occur using Jelly Injection.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Security risk rating

</td><td>

9

</td></tr><tr><td>

Functional impact

</td><td>

This property makes a best guess at whether an expression is quoted. It may wrongly quote legitimate expression. In that case manually marking an expression as safe may be necessary.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) JEXL injection is a form of input injection unique to the ServiceNow AI Platform that can lead to both cross-site request forgery and code execution. Completely turning off the protection may potentially open many P1 security vulnerabilities.

</td></tr><tr><td>

Workaround

</td><td>

To manually mark an expression as safe add SAFE prefix to Jelly expression:

 `${SAFE:sysparm_input};`

 Blindly adding SAFE to each expression is the wrong way to approach the problem, because it may open a security vulnerability.

-   Only add SAFE to an expression if you can guarantee that the expression does not contain input from the client.
-   If it does, it's possible for a malicious client to cause evaluation of privileged JavaScript.

</td></tr><tr><td>

References

</td><td>

[Jelly tags](https://www.servicenow.com/docs/access?context=r_JellyTags&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) [High Security Settings](../../security/concept/c_HighSecuritySettings.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

