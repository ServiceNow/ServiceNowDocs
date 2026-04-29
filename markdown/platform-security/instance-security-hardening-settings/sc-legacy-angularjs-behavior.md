---
title: Disable legacy AngularJS behavior \[Removed in Security Center 2.2\]
description: Use the glide.angular.legacy property to protect from potential security risks arising from attacks on vulnerabilities discovered in outdated AngularJS library versions.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable legacy AngularJS behavior \[Removed in Security Center 2.2\]

Use the **glide.angular.legacy** property to protect from potential security risks arising from attacks on vulnerabilities discovered in outdated AngularJS library versions.

Set **glide.angular.legacy** to the recommended value of **false** to prevent older prepatched angularJS versions from being used. Set the property to **true** to use older prepatched angularJS versions.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.angular.legacy**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)|
|Purpose|The system property is a failsafe in case any organizations depend on the non-patched versions of angularJS to run their custom implementations.|
|Recommended value|False|
|Configuration type|Boolean|
|Security risk|\(High\) Using older versions of angularJS could potentially lead to security risks arising from attacks on vulnerabilities discovered in outdated AngularJS library versions.|
|Security risk rating|7.1|

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

