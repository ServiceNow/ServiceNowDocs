---
title: Escape XML markup
description: Use the glide.ui.escape\_text property to force escape of XML values at the parser level before transmitting them to the client's browser.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape XML markup

Use the **glide.ui.escape\_text** property to force escape of XML values at the parser level before transmitting them to the client's browser.

Use the **glide.ui.escape\_text** system property to escape XML values at the parser level for the user interface. It prevents reflected and stored cross-site scripting attacks. This property is not applicable in Service Portal.

Cross-site scripting occurs when an attacker injects malicious JavaScript into an entry point. The platform/application fails to escape the malicious JavaScript before transmitting it to the victim's browser for execution. Escaping in this context means the following:

-   **&amp;** --&gt; `&amp;`
-   **&lt;** --&gt; `&lt;`
-   **&gt;** --&gt; `&gt;`
-   **"** --&gt; `&quot;`
-   **'** --&gt; `&#x27;`
-   **/** --&gt; `&#x2F;`

Example: `<script>alert('XSS Attack');</script>`

Escaping: `&lt;script&gt;alert(&#39;XSS Attack&#39;);&lt;/script&gt;`

Ensure the **glide.ui.escape\_text** property exists in the System Properties \[sys\_properties\] table and is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.escape\_text**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.8
-   CVSS rating: High
-   Security risk details:

If **glide.ui.escape\_text** is not set to the recommended value of **true**, then XML values will not be escaped at the parser level for the user interface; this will leave jelly templates susceptible to reflected and stored cross site scripting attacks.


</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

