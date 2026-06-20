---
title: Configure mobile re-authentication login timespan
description: Define a time period in seconds that a user is not required to re-authenticate themselves. This parameter only applies when a user has permission to re-authenticate multiple times.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/mobile/mobile-platform/mobile-reauthentication-token-lifespan.html
release: xanadu
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure mobile re-authentication system properties, Mobile system property configurations, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile re-authentication login timespan

Define a time period in seconds that a user is not required to re-authenticate themselves. This parameter only applies when a user has permission to re-authenticate multiple times.

## Before you begin

If **glide.sg.reauthentication.single\_use\_token** is set to `false`, you can configure this property.

Make sure to select `Global` as the application scope.

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the Filter Navigator.

2.  Select **New** in the System Property table.

3.  In the form, match the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.authenticate.reauth.token.lifespan**|
    |Type|`integer`|
    |Value|Integer value in seconds.|


**Parent Topic:**[Configure mobile re-authentication system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/mobile/mobile-platform/mobile-reautentication-concept.md)

