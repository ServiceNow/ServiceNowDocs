---
title: Escape HTML in list views \[Updated in Security Center 1.3 and 1.5\]
description: Use the glide.ui.escape\_html\_list\_field property to force HTML escapes for HTML fields in a list view.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape HTML in list views \[Updated in Security Center 1.3 and 1.5\]

Use the **glide.ui.escape\_html\_list\_field** property to force HTML escapes for HTML fields in a list view.

Set **glide.ui.escape\_html\_list\_field** to **true** to prevent HTML from being rendered in HTML fields in list view. Leaving HTML sanitization inactive platform wide \(via system property\) or by field \(via a schema attribute\), may lead to XSS style attacks. XSS attacks may allow a low privileged user to hijack the session of a high privileged user or interfere in standard web application behaviors, including redirects or defacement.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It’s non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.escape\_html\_list\_field**

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

To prevent application against cross-site scripting attacks

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

3.1

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces HTML encoding to occur on the UI at the HTML parser level and thus renders back encoded results to the user. It can have a functionality impact based on the instance user interaction with the resulted data.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Input validation must occur on the application to defend against cross-site scripting attacks. These attacks enable foreign scripts to execute on user sessions in the logged in browser's context. Attackers can use it to steal session information and sensitive data.

</td></tr><tr><td>

References

</td><td>

[High Security Settings](../../security/concept/c_HighSecuritySettings.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

