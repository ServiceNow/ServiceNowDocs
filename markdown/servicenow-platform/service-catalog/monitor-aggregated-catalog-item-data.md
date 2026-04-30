---
title: Monitoring aggregated catalog item data
description: Monitor aggregated catalog item data like fulfillment automation coverage, translation coverage, and conversational coverage using the Service Catalog Overview dashboard.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Monitoring aggregated catalog item data

Monitor aggregated catalog item data like fulfillment automation coverage, translation coverage, and conversational coverage using the Service Catalog Overview dashboard.

## Aggregated catalog item data graphs

You can access the aggregated catalog item data graphs in the Service Catalog Overview dashboard by navigating to **All &gt; Service Catalog &gt; Service Catalog Overview** if you have the catalog\_admin role.

The Catalog item translation coverage graph is displayed only if you have enabled the Localization framework. For more information, see [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

|Graph|Description|
|-----|-----------|
|Catalog request channel analytics - last 12 months|Vertical bar graph representing the count of catalog requests made through different channels such as Virtual Agent, Service Portal, Mobile in the last 12 months.|
|Catalog item best practice deviations|Pie-chart representing the Item Diagnostic Results report scores for catalog items, which indicate the health of items. A higher score means that an item has more deviations from best practices. For example, duplicate variables for a catalog item will represent a higher score. Each score is represented by a different color.|
|Catalog item VA render type|Horizontal bar graph representing the individual count of the way catalog items are rendered in Virtual Agent. It specifies whether an item is rendered as a pop-up, window, or conversation in Virtual Agent.|
|Catalog item fulfillment automation coverage|Vertical bar graph representing the count of fulfillment automation coverage of catalog items. It specifies whether items are fully automated, semi-automated, manual, unspecified, or empty.|
|Catalog item translation coverage|Vertical bar graph representing the count of the translation status of catalog items. It specifies whether items are completely translated, partially translated, not translated, or in-progress.|

![Service Catalog Overview dashboard](../image/sc-overview-dashboard.png)

**Parent Topic:**[Service Catalog items](../concept/c_IntroductionToCatalogItems.md)

**Related topics**  


[Dashboards overview](https://www.servicenow.com/docs/access?context=dashboards-overview&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

