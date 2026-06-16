---
title: Usage Insights Funnel release notes
description: Version history for the Usage Insights Funnel on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-user-experience-analytics-funnel.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Usage Insights Funnel release notes

Version history for the Usage Insights Funnel on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.2.2 - June 2026**
    -   Added session-based funnel analysis to the Usage Insights Conversion Funnel.
    -   Users can toggle Session-based vs. user-based mode via the Funnel type filter.
-   **Version 6.1.12 - March 2026**

    Usage Insights funnel capabilities are now available as part of PA Dashboard visualization experiences. Funnels created in Usage Insights can now be configured and displayed directly within Platform Analytics inline dashboards, enabling a unified view of conversion analytics in PA Dashboards. Existing funnels can be selected through the PA dashboard configuration and identical metrics and conversion rates are ensured across both surfaces. Access controls defined in Usage Insights are respected, and clear messages are displayed if a funnel is unavailable or access has been revoked.

-   **Version 5.1.2 - February 2026**

    Fix: uxa funnel saves relative dates as absolute, so relative dates period is not being calculated correctly

-   **Version 5.0.8 - August 2025**

    Fixed: In Funnels, for Use data sampling toggle on/off - data is not changed unless we do a cache refresh

-   **Version 4.0.22 - July 2025 \(Yokohama\)**

    Fix for: Role access check and enforcement. When funnel is created with "SessionStartedAny" as first step, the data is being filtered for new user sessions\(usertype=new\) and funnel values are shown for only new user sessions.

-   **Version 4.0.17 - March 2025**

    No changes in the UI. Funnel Page Duration is not Displayed between the Funnel Steps - that is the only change, but backend still does not support it so it is not exposed in the UI yet.

-   **Version 4.0.16 - February 2025**

    No changes.

-   **Version 3.1.3 - May 2024**

    The User Experience Analytics Funnel component helps users view conversion rates in aggregate user behavior to uncover the reasons behind success or failure of a user flow. This visualization only works with User Experience Analytics data.


