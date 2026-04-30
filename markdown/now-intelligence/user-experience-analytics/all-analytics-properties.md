---
title: User Experience Analytics related properties
description: Use system properties to configure User Experience Analytics in Platform Analytics, ServiceNow Mobile Platform, Service Portal, and the Conversational Analytics area of Virtual Agent.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, User Experience Analytics, Platform Analytics]
---

# User Experience Analytics related properties

Use system properties to configure User Experience Analytics in Platform Analytics, ServiceNow Mobile Platform, Service Portal, and the Conversational Analytics area of Virtual Agent.

## General User Experience Analytics related properties

Use the following system properties in Platform Analytics, ServiceNow Mobile Platform, Service Portal, and the Conversational Analytics area of Virtual Agent.

-   **__glide.analytics.enabled__**

    Select whether to enable the option to track user analytics.

    -   Type: true \| false
    -   Default value: false
-   **__glide.analytics.user.consent.script\_timeout__**

    Maximum time in milliseconds that a script can run during the User Experience Analytics consent policy mechanism, when triggering the provider's custom script. The minimum value is 100 ms. The maximum value is 5000 ms.

    -   Type: string
    -   Default value: 2000

## User Experience Analytics related properties for Service Portal

Use the following system properties in the Service Portal only.

-   **__glide.analytics.tracking.force\_allowed.portals__**

    Turns off the user consent pop-up for specified portals.

    -   Type: string
    -   Default value: none
-   **__glide.analytics.tracking.restricted.portals__**

    Turns off user analytics tracking for specified portals.

    This property overrides the **glide.sp.analytics.enabled.portals** property. You specify a portal by pasting its sys\_id in the **Value** field. To specify multiple portals, enter a comma-separated list with no spaces.

    -   Type: string
    -   Default value: none
-   **__glide.sp.analytics.enabled.portals__**

    Enables user analytics tracking for specified portals. By default, tracking is enabled for the base system Service Portal.

    -   Type: string
    -   Default value: 81b75d3147032100ba13a5554ee4902b

**Note:** If you make certain key changes to portals, such as changing the sys\_id, data is not carried over and you see a different dashboard.

**Parent Topic:**[User Experience Analytics reference](../content-framework/landing-page/user-experience-analytics-reference.md)

