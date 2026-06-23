---
title: Disable public access to favorites \[Updated in Security Center 1.3 and 2.0\]
description: Use the glide.ui.magellan.favorites.allow\_public to specify whether unauthenticated users are allowed to see Favorites in the navigator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-security/instance-security-hardening-settings/public-access-favorites.html
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable public access to favorites \[Updated in Security Center 1.3 and 2.0\]

Use the **glide.ui.magellan.favorites.allow\_public** to specify whether unauthenticated users are allowed to see **Favorites** in the navigator.

Public Access to Favorites will be compliant if **glide.ui.magellan.favorites.allow\_public** is set to **false**.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.ui.magellan.favorites.allow\_public**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Configure in Instance Security Center|Yes|
|Purpose|Control if unauthenticated users are allowed to see **Favorites** in the navigator.|
|Type|true/false|
|Recommended value|false|
|Security Dependencies|Set **glide.ui.magellan.favorites.allow\_public** to **false**.|
|Functional impact|\(Medium\) Enabling this property acts as a layer of protection from unauthorized users.|
|Security risk|\(Medium\) If this property is not enabled, there is a risk of unauthorized access to sensitive data.|
|References|[Manage favorites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/employee-experience-foundation/web-configure-favorites-employee.md)|

**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/instance-security-hardening-settings/sc-access-control.md)

