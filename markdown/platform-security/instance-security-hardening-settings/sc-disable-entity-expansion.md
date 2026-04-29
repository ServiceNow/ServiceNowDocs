---
title: Disable Entity Expansion within the XMLDocument2 Streaming Parser
description: If customizations do not require entity expansion, use the glide.stax.allow\_entity\_resolution property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable Entity Expansion within the XMLDocument2 Streaming Parser

If customizations do not require entity expansion, use the **glide.stax.allow\_entity\_resolution** property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

If the **glide.stax.allow\_entity\_resolution** is not set to the recommended value of **false**, then this property allow XML entities to be expanded during parsing by the streaming parser \(XMLDocument2\).

Ensure that the property **glide.stax.allow\_entity\_resolution** exists in the System Properties \[sys\_properties\] table and is set to **false**. If the property does not appear in the System Properties \[sys\_properties\] table the default value is **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

****

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

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 9.0
-   CVSS rating: Critical
-   Security risk details: XML entity expansion can lead to attacks such as ability to read system files, and Denial of Service.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Before setting this property:

-   Set the **glide.xml.entity.whitelist.enabled** and **glide.stax.whitelist\_enabled** properties to true. To learn more, see [Restrict XML external entities](sc-xml-entity-validation-url-allowlist.md) and [Require XMLdoc2 entity validation with allowlist](sc-xmldoc2-entity-validation-with-entity-expansion.md).
-   Define a listing of comma-delimited FQDN in the **glide.xml.entity.whitelist** property, which is the only URLs that can be reached using XML Entity processing. property. To learn more, see [Restrict XML external entities](sc-xml-entity-validation-url-allowlist.md).

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

