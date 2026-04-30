---
title: Enforce relative links \[Updated in Security Center 1.3 and 1.5\]
description: Use the glide.cms.catalog\_uri\_relative property to enforce relative links from the URI parameter on /ess/catalog.do.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce relative links \[Updated in Security Center 1.3 and 1.5\]

Use the **glide.cms.catalog\_uri\_relative** property to enforce relative links from the URI parameter on `/ess/catalog.do`.

The **glide.cms.catalog\_uri\_relative** property enforces relative links from the URI parameter on /ess/catalog.do. If **glide.cms.catalog\_uri\_relative** is not set to the recommended value of true, then the URL will not be sanitized with the enforceRelativeURL\(url\) function. Absolute URLs can pose a security risk when used as a part of parameter or a field value, thus redirecting the source page to an adversary-controlled website.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.cms.catalog\_uri\_relative**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|To restrict attempts to link external unauthorized content.|
|Recommended value|true|
|Default value|false|
|Security risk rating|2.6|
|Functional impact|This remediation enforces validation on Catalog page such that only Relative URLs are permitted. Existing links to external web applications become broken.|
|Security risk|\(High\) Absolute URLs can pose a security risk when used as a part of parameter or a field value, thus redirecting the source page to an adversary-controlled website.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

