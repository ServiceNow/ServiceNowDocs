---
title: Disable unauthenticated published reports \[Updated in Security Center 2.0\]
description: Deactivate this property to prevent the user from publishing or accessing reports. This property disables the published reports feature in reporting.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable unauthenticated published reports \[Updated in Security Center 2.0\]

Deactivate this property to prevent the user from publishing or accessing reports. This property disables the published reports feature in reporting.

Enable publishing reports by setting the **glide.report.published\_reports.enabled** to **true**.

Ensure the Glide Property **glide.report.published\_reports.enabled** exists and is set to the value false. If the property does not appear in the sys\_properties table, add a new record.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.report.published\_reports.enabled**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)|
|Purpose|Disables the published reports feature in reporting.|
|Type|true \| false|
|Recommended value|**false**|
|Security risk rating|6.5|
|Functional impact|The user cannot publish reports.|
|Security risk|\(Moderate\) If this property is not enabled, users may be able to access or publish reports exposing sensitive data. Publishing a report creates a URL that anyone can use to access the report, including people who are not users. When anyone navigates to the URL, the report is generated with current data from the instance.|
|References|[Publish a report](https://www.servicenow.com/docs/access?context=t_PublishAReport&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

