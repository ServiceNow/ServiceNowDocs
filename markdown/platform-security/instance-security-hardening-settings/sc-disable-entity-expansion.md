---
title: Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]
description: If customizations do not require entity expansion, use the glide.stax.allow\_entity\_resolution property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-11"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]

If customizations do not require entity expansion, use the **glide.stax.allow\_entity\_resolution** property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

Disable entity expansion on your instance to secure your instance from attacks such as ability to read system files, and Denial of Service. Use the system property to disallow XML entities to be expanded during parsing by the streaming parser \(XMLDocument2\).

Set the **glide.stax.allow\_entity\_resolution** system property to **false** to disable entity expansion on your instance. If this property does not appear in the System Properties \[sys\_properties\] table, the default value is **true**. Create the property record and set the value to **false** to change it's value.

## Prerequisites

Before setting this property:

-   Set the **glide.xml.entity.whitelist.enabled** and **glide.stax.whitelist\_enabled** properties to true. To learn more, see [Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]](sc-xml-entity-validation-url-allowlist.md) and [Require XMLdoc2 entity validation with allowlistDisable entity expansion \[Updated in Security Center 1.3\]](sc-xmldoc2-entity-validation-with-entity-expansion.md).
-   Define a listing of comma-delimited FQDN in the **glide.xml.entity.whitelist** property, which is the only URLs that can be reached using XML Entity processing. property. To learn more, see [Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]](sc-xml-entity-validation-url-allowlist.md).

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.stax.allow\_entity\_resolution**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|This remediation control must be enabled to defend against an XML Entity Expansion/Billion Laugh attack.|
|Recommended value|false|
|Default value|true|
|Functional impact|If the customization is using entity expansion, then, the ServiceNow AI Platform might block further processing.|
|Security risk|\(Critical\) An attacker can use this vulnerability to expand data exponentially, quickly consuming all system resources.|
|Workaround|If the customization requires entity expansion, set this property to true and follow the steps documented in [Require XMLdoc2 entity validation with allowlistDisable entity expansion \[Updated in Security Center 1.3\]](sc-xmldoc2-entity-validation-with-entity-expansion.md).|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

For more information about OWASp resources, see [OWASp](https://owasp.org/www-project-top-ten/2017/A4_2017-XML_External_Entities_(XXE)).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

