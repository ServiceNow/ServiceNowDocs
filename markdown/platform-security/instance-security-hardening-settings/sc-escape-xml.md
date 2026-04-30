---
title: Escape XML markup \[Updated in Security Center 1.3\]
description: Use the glide.ui.escape\_text property to force escape of XML values at the parser level before transmitting them to the client's browser.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape XML markup \[Updated in Security Center 1.3\]

Use the **glide.ui.escape\_text** property to force escape of XML values at the parser level before transmitting them to the client's browser.

Cross-site scripting occurs when an attacker injects malicious JavaScript into an entry point. The platform/application fails to escape the malicious JavaScript before transmitting it to the victim's browser for execution. Escaping in this context means the following:

-   **&amp;** --&gt; `&amp;`
-   **&lt;** --&gt; `&lt;`
-   **&gt;** --&gt; `&gt;`
-   **"** --&gt; `&quot;`
-   **'** --&gt; `&#x27;`
-   **/** --&gt; `&#x2F;`

Example: `<script>alert('XSS Attack');</script>`

Escaping: `&lt;script&gt;alert(&#39;XSS Attack&#39;);&lt;/script&gt;`

Ensure the **glide.ui.escape\_text** property exists in the sys\_properties table and is set to true.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.escape\_text**

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

Escaping XML ensures that browsers do not parse the malicious JavaScript embedded in untrusted data, and execute it as JavaScript. -   A malicious user may try XSS attack to either hijack other users' session or redirect the user to a malicious website.
-   The NOW Platform contains code to secure cookies, but escaping it relies on this property being set to **true**.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

8.8

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces XML encoding at the XML parser level on the UI. It renders the encoded results for the user, which can have a functionality impact based on the instance user interaction with the resulted data.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Input validation must occur on the application to defend against cross-site scripting attacks. These attacks enable foreign scripts to execute on user session in the logged in browser's context. Attackers can use it to steal session information and sensitive data.

</td></tr><tr><td>

Workaround

</td><td>

After you set this property to **true**, rendering stops on the HTML tags in the catalog item description or in the catalog item variable help text. You may not be able to use HTML formatting for some fields.

 However, if the **glide.ui.escape\_text** property is turned of, all JEXL expressions would be prefixed with an output encoder:

 `$⁠{JS:expression}`

 `$⁠{HTML:expression}`

 or

 `$⁠{JS,HTML:expression}`

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

