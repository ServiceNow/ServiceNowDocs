---
title: Disable legacy JQuery behavior \[Updated in Securty Center 1.3\]
description: The glide.jquery.legacy is used to prevent older prepatched JQuery versions from being used which will introduce unpatched vulnerabilities in the library.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable legacy JQuery behavior \[Updated in Securty Center 1.3\]

The **glide.jquery.legacy** is used to prevent older prepatched JQuery versions from being used which will introduce unpatched vulnerabilities in the library.

Set **glide.jquery.legacy** to the recommended value of **false** to prevent older prepatched JQuery versions from being used which introduce unpatched vulnerabilities in the library. Set the value to **true** to allow prepatched JQuery versions.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.jquery.legacy**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)|
|Purpose|To prevent potential security risks arising from attacks on vulnerabilities discovered in outdated JQuery library versions.|
|Recommended value|False|
|Configuration type|Boolean|
|Security risk|\(High\) Prevent older prepatched JQuery versions from being used which introduce unpatched vulnerabilities in the library. The system property is a failsafe in case any organizations depend on the non-patched versions of angularJS to run their custom implementations.|
|Security risk rating|7.1|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

