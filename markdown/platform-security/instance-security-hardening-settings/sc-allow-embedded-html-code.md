---
title: Disable embedded HTML code \[Updated in Security Center 1.3\]
description: Use the glide.ui.security.allow\_codetag property to disable support for embedding HTML code created using the \[code\] tag.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable embedded HTML code \[Updated in Security Center 1.3\]

Use the **glide.ui.security.allow\_codetag** property to disable support for embedding HTML code created using the \[code\] tag.

The ServiceNow AI Platform mitigates many injection and cross-site attacks by implementing escaping and encoding techniques. As a result, users can't write/submit HTML formatted inputs for journal fields. But journal fields can render text enclosed within code tags as HTML.

-   However, there is an associated security risk. If set to `true`, malicious users can write harmful HTML JS code that may be executed on a different client browser after rendering of journal fields.
-   Set this property to `false` so that administrators can prevent journal fields from rendering HTML code by disabling support for the `[code]` tag.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

glide.ui.security.allow\_codetag

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Configure in Instance Security Center

</td><td>

Yes

</td></tr><tr><td>

Purpose

</td><td>

Protect against cross-site scripting and malicious script execution

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

4.2

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces HTML encoding to occur on the UI and renders the encoded results to the user. This property is set to `true` by default. In this state, your instance displays rendered HTML in journal fields and forms.

If this property is set to `false`, HTML is not rendered properly and HTML tags may appear in journal fields on forms. It can have an adverse impact on functionality, and on user interactions with the resulting data.

</td></tr><tr><td>

Security risk

</td><td>

\(Medium\) Input validation must occur in the application to defend against cross-site scripting attacks. These attacks enable foreign scripts to execute on a user session in the logged in browser's context. Attackers can use it to steal session information and sensitive data.

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

