---
title: Enable HTML Sanitizer \[Updated in Security Center 1.3\]
description: Use the glide.html.sanitize\_all\_fields property to enable the HTMLSanitizer script include, which sanitizes HTML input based on exclusion listed and inclusion listed attributes configured in a script.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable HTML Sanitizer \[Updated in Security Center 1.3\]

Use the **glide.html.sanitize\_all\_fields** property to enable the HTMLSanitizer script include, which sanitizes HTML input based on exclusion listed and inclusion listed attributes configured in a script.

The field types available with dictionary/fields include HTML and Translated HTML. These HTML input fields enable users to write HTML formatted input, for example:

`<h1>Test</h1>`, using the most basic HTML tags such as `<img>`, `<a href …>`, and `<iframe>`.

It can open a door for a malicious attacker to inject malicious vector with HTML tags such as:

`[<IMG SRC=" &#14; JavaScript:alert('XSS');">][<IMG onmouseover="alert('xss')">],[a href="" onclick=alert(/xss/)]`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.html.sanitize\_all\_fields**

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

Prevents application against cross site scripting and HTML injection attacks

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

8.8

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces HTML-output encoding mechanism before the user data is rendered back to the user. If customer has any customization that involves rendering of the HTML attribute or content data, then there is a functionality impact.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) User input should be securely treated when the data is being stored and processed on the application.This reduces client-side cross-site scripting attacks by output encoding the data.

</td></tr><tr><td>

Workaround

</td><td>

This property sanitizes all HTML fields in the system. If you must enable HTML sanitization on individual fields, see [Enable sanitization on individual fields](../../security/task/t_EnSanitizIndFlds.md).

 You can also configure the inclusion list or exclusion list to sanitize HTML tags and attributes as per your organizations policy.

</td></tr><tr><td>

References

</td><td>

[Enabling HTML sanitizer](../../security/task/t_ActivateHTMLSanitizer.md)

 [HTML sanitizer](../../security/concept/c_HTMLSanitizer.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

