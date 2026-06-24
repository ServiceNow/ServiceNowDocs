---
title: Usage Insights related properties for Service Portal
description: Use system properties to configure Usage Insights for Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/service-portal/sp-analytics-properties.html
release: zurich
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Usage Insights for Service Portal, Analytics and Reporting Solutions for Service Portal, Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Usage Insights related properties for Service Portal

Use system properties to configure Usage Insights for Service Portal.

-   **__glide.analytics.tracking.force\_allowed.portals__**

    Turns off the user consent pop-up for specified portals. You specify a portal by pasting its sys\_id in the **Value** field. To specify multiple portals, enter a comma-separated list with no spaces.

    -   Type: string
    -   Default value: none
-   **__glide.analytics.tracking.restricted.portals__**

    Turns off user analytics tracking for specified portals. You specify a portal by pasting its sys\_id in the **Value** field. To specify multiple portals, enter a comma-separated list with no spaces.

    -   Type: string
    -   Default value: none

**Parent Topic:**[Usage Insights for Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/service-portal/sp-analytics.md)

**Related topics**  


[Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md)

[Unique record identifier \(sys\_id\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/c_UniqueRecordIdentifier.md)

