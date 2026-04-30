---
title: Disable JavaScript tags in embedded HTML \[Updated in Security Center 1.3\]
description: Use the glide.ui.security.codetag.allow\_script property to disable support for embedding HTML JavaScript code created using of the \[code\] tag.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable JavaScript tags in embedded HTML \[Updated in Security Center 1.3\]

Use the **glide.ui.security.codetag.allow\_script** property to disable support for embedding HTML JavaScript code created using of the \[code\] tag.

The ServiceNow AI Platform mitigates many injection and cross-site attacks by implementing escaping and encoding techniques. As a result, users can't write and submit HTML formatted inputs for journal fields. However, journal fields can render text enclosed within code tags as HTML. Ensure the**glide.ui.security.codetag.allow\_script** property exists in the sys\_properties table and is set to false.

-   However, there is an associated security risk. If set to **true**, malicious users can write harmful HTML JavaScript code that may be executed on a different client browser after rendering of journal fields.
-   Set this property to **false** so that administrators can prevent journal fields from rendering HTML JavaScript code by disabling support for the `[code]` tag.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.security.codetag.allow\_script**

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

Protects against cross-site scripting and malicious script execution

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Security risk rating

</td><td>

8.8

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces JavaScript escaping to occur on the UI and renders the encoded results to the user. It can have a functionality impact based on the instance user interaction with the resulted data.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Input validation must occur in the application to defend against cross-site scripting attacks. These attacks enable foreign scripts to execute on the user session in the logged in browser's context. Attackers can use it to steal session information and sensitive data.

</td></tr><tr><td>

References

</td><td>

[Restrict the CODE tag in journal fields](https://www.servicenow.com/docs/access?context=t_RestrictTheCODETagInJrnalFlds&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

 [Render journal field entries as HTML](https://www.servicenow.com/docs/access?context=render-journal-field-entries-as-html&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

 [High Security Settings](../../security/concept/c_HighSecuritySettings.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

