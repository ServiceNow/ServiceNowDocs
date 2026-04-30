---
title: Define restricted downloadable MIME types \[Updated in Security Center 1.3, 1.5, and 2.0\]
description: Use the glide.ui.attachment.force\_download\_all\_mime\_types property to download MIME types and not to render inline in the browser.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Define restricted downloadable MIME types \[Updated in Security Center 1.3, 1.5, and 2.0\]

Use the **glide.ui.attachment.force\_download\_all\_mime\_types** property to download MIME types and not to render inline in the browser.

If **glide.ui.attachment.download\_mime\_types** does include dangerous MIME types such as text/html, image/svg ,image/svg+xml,application/xml, then dangerous files could be rendered inline in the browser, which could lead to Cross Site Scripting attacks \(XSS\). This property is the list of comma-separated attachment mime types, which won’t render inline in the browser. For example, including text/html forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser. Maintaining this list properly prevents cross-site scripting attacks.

If the **glide.ui.attachment.download\_mime\_types** system property doesn't include dangerous MIME types such as "text/html, image/svg,image/svg+xml,application/xml", then dangerous files could be rendered inline in the browser. This can lead to Cross Site Scripting \(XSS\) attacks. This check is only relevant when **glide.ui.attachment.force\_download\_all\_mime\_types** is set to **false**.

This property is a list of comma-separated attachment MIME types, which don’t render inline in the browser. For example, including `text/html` forces HTML files to be downloaded to the client as attachments rather than viewed inline in the browser.

If **glide.ui.attachment.force\_download\_all\_mime\_types** is set to **false**, verify that the **glide.ui.attachment.download\_mime\_types** system property includes the dangerous MIME types `text/html,image/svg,image/svg+xml,application/xml`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.attachment.force\_download\_all\_mime\_types**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String \(Comma-separated list of MIME types\)

</td></tr><tr><td>

Recommended value

</td><td>

text/html,image/svg,image/svg+xml,application/xml

</td></tr><tr><td>

Default value

</td><td>

text/html,image/svg,image/svg+xml,application/xml

</td></tr><tr><td>

Fallback value

</td><td>

text/html,image/svg,image/svg+xml,application/xml

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.3
-   CVSS score: Medium
-   Security Risk: Maintaining this list properly can prevent cross site scripting attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This check is only relevant when **glide.ui.attachment.download\_mime\_types** is set to **false** or doesn’t exist in the System Properties \[sys\_properties\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

