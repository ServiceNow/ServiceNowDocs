---
title: User Experience Analytics related properties for Service Portal
description: Use system properties to configure User Experience Analytics for Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-user-interface/service-portal/sp-analytics-properties.html
release: xanadu
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics for Service Portal, Analytics and Reporting Solutions for Service Portal, Using portal analytics, Service Portal, Configure UIs and portals, Configure user experiences]
---

# User Experience Analytics related properties for Service Portal

Use system properties to configure User Experience Analytics for Service Portal.

-   **__glide.analytics.tracking.force\_allowed.portals__**

    Turns off the user consent pop-up for specified portals. You specify a portal by pasting its sys\_id in the **Value** field. To specify multiple portals, enter a comma-separated list with no spaces.

    -   Type: string
    -   Default value: none
-   **__glide.analytics.tracking.restricted.portals__**

    Turns off user analytics tracking for specified portals. You specify a portal by pasting its sys\_id in the **Value** field. To specify multiple portals, enter a comma-separated list with no spaces.

    -   Type: string
    -   Default value: none

**Parent Topic:**[User Experience Analytics for Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-user-interface/service-portal/sp-analytics.md)

**Related topics**  


[Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/r_AvailableSystemProperties.md)

[Unique record identifier \(sys\_id\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/c_UniqueRecordIdentifier.md)

