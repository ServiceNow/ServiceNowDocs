---
title: Require XMLdoc2 entity validation with allowlist
description: If customizations do not require entity expansion, use the glide.xmlutil.max\_entity\_expansion property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Require XMLdoc2 entity validation with allowlist

If customizations do not require entity expansion, use the **glide.xmlutil.max\_entity\_expansion** property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

If the glide property **glide.stax.whitelist\_enabled** doesn't exist in the System Properties \[sys\_properties\] table, or is not set to the recommended value of **true**, then all external entities are allowed when the glide property **glide.stax.allow\_entity\_resolution** is set to the value of **true**.

If customizations don't require entity expansion, use the **glide.stax.allow\_entity\_resolution** property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

-   If you set **glide.stax.allow\_entity\_resolution** to **true**, all external entities attempt to resolve or expand subject entities, subject to the setting of the **glide.stax.whitelist\_enabled** property.
-   If you set **glide.stax.allow\_entity\_resolution** to **false**, all entity resolution and expansion is blocked. To learn more about this property, see [Disable Entity Expansion within the XMLDocument2 Streaming Parser](sc-disable-entity-expansion.md).

When **glide.stax.whitelist\_enabled** is set to **true**, define a listing of comma-delimited FQDN in the **glide.xml.entity.whitelist** property, which are the only URLs that can be reached using the XML entity processing property. To learn more, see [Restrict XML external entities](sc-xml-entity-validation-url-allowlist.md). Attackers can use this vulnerability to expand data exponentially in an External Entities Expansion \(XXE\) attack, quickly consuming all system resources.

## Prerequisites

Before setting this property:

-   Set the **glide.xml.entity.whitelist.enabled** and **glide.stax.whitelist\_enabled** properties to **true**. To learn more, see [Restrict XML external entities](sc-xml-entity-validation-url-allowlist.md).
-   Define a listing of comma-delimited FQDN in the **glide.xml.entity.whitelist** property, which is the only URLs that can be reached using XML Entity processing property. To learn more, see [Restrict XML external entities](sc-xml-entity-validation-url-allowlist.md).

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.stax.whitelist\_enabled**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|This remediation control must be enabled to defend against an XML Entity Expansion/Billion Laugh attack.|
|Recommended value|true|
|Default value|true|
|Security risk rating|9.8|
|Functional impact|If the customization is using entity expansion, then, the ServiceNow AI Platform might block further processing.|
|Security risk|An attacker can use this vulnerability to expand data exponentially in an External Entities Expansion \(XXE\) attack, quickly consuming all system resources.|
|Workaround|If the customization requires entity expansion, set this property to true and follow the steps documented in [Restrict XML external entities](sc-xml-entity-validation-url-allowlist.md).|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

For more information about OWASp resources, see [OWASp](https://owasp.org/www-project-top-ten/2017/A4_2017-XML_External_Entities_(XXE)).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

