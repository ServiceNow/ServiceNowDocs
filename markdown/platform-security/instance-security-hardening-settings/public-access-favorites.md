---
title: Disable public access to favorites \[Updated in Security Center 1.3 and 2.0\]
description: Use the glide.ui.magellan.favorites.allow\_public to specify whether unauthenticated users are allowed to see Favorites in the navigator.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
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
|References|[Create or view favorites](https://www.servicenow.com/docs/access?context=view-favorite-lists&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)|

**Parent Topic:**[Access control](../../security-center/reference/sc-access-control.md)

