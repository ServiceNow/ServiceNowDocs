---
title: Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]
description: If customizations do not require entity expansion, use the glide.stax.allow\_entity\_resolution property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable Entity Expansion within the XMLDocument2 Streaming Parser \[Updated in Security Center 1.5\]

If customizations do not require entity expansion, use the **glide.stax.allow\_entity\_resolution** property to completely disable external entity expansion. The XML completes parsing but doesn't include any internal or external entities.

-   If you set this property to **true**, all external entities attempt to resolve or expand subject entities, subject to the setting of the **glide.stax.whitelist\_enabled** property.
-   If you set that property to **false**, all entity resolution and expansion is blocked. To learn more, see XMLdoc2 entity validation with whitelist.

## Prerequisites

Before setting this property:

-   Set the **glide.xml.entity.whitelist.enabled** and **glide.stax.whitelist\_enabled** properties to true. To learn more, see XMLdoc/XMLUtil entity validation with whitelist and XMLdoc2 entity validation with whitelist.
-   Define a listing of comma-delimited FQDN in the **glide.xml.entity.whitelist** property, which is the only URLs that can be reached using XML Entity processing. property. To learn more, see XML external entity processing - whitelist.

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
|Workaround|If the customization requires entity expansion, set this property to true and follow the steps documented in XMLdoc2 entity validation with whitelist.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

For more information about OWASp resources, see [OWASp](https://owasp.org/www-project-top-ten/2017/A4_2017-XML_External_Entities_(XXE)).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

