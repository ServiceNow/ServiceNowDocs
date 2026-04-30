---
title: Improve portal performance
description: Discover ways to reduce portal loading time and enhance portal display.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage, Employee Center, Employee Service Management]
---

# Improve portal performance

Discover ways to reduce portal loading time and enhance portal display.

## Review widget performance metrics

The **Performance details** feature provides comprehensive tracking of each widget on a page, enabling better assessment of the user experience. You can view load times, customization status, and display visibility for each widget. For guidance on accessing the widget performance metrics, see [View widget performance metrics](../task/view-widget-performance-metrics.md).

## Enable asynchronous loading for widgets

By default, widgets try to load and display data simultaneously. This can cause longer load times in content-heavy portals. To improve loading speed and reduce employee wait times, select the **Asynchronous** option to enable widgets to display data as it becomes available, instead of waiting for all the data to load.

The following widgets support asynchronous loading:

-   Content experience
-   Recommended for you
-   Popular topics
-   Quick Links
-   My applications
-   My active items

**Note:** Performance tracking is not supported for widgets with asynchronous data loading enabled.

For step-by-step instructions to enable asynchronous loading, see [Improve portal load time with asynchronous loading](../task/optimize-performance-of-employee-center-home-page.md).

## Reduce the amount of connected content

Reducing the amount of connected content can help improve page load times, as topics with more linked items—like quick links, knowledge articles, and catalog items—take longer to load. Aim to connect only 80% of published content to topics, allowing the remaining items to be accessible through search. Also, remove any unnecessary content, such as outdated or unpublished versions, from topics.

For guidance on navigating to a topic and viewing its connected content, see [Create and associate topics](../task/create-topics-for-taxonomy.md).

-   **[Improve portal load time with asynchronous loading](../task/optimize-performance-of-employee-center-home-page.md)**  
Reduce the time employees spend waiting for the portal to load by enabling widgets to load data asynchronously. This allows widgets to display information as it becomes available, improving overall portal performance.
-   **[Improve the image load time on Employee Center](../task/optimize-image-loading.md)**  
Use CDN URLs to reduce the load time of the banner images, background images, and app icons on the Employee Center portal.
-   **[Add hotspots to track custom widget performance](../task/add-hotspots-track-custom-widget-performance.md)**  
Hotspots help capture and log widget load times, which enables better debugging of long portal load times.
-   **[View widget performance metrics](../task/view-widget-performance-metrics.md)**  
View the metrics provided by the performance window to identify which widgets take the longest to load data.

**Parent Topic:**[Managing Employee Center](manage-emp-center.md)

**Related topics**  


[Action framework](action-framework.md)

[Creating campaigns with Content Experiences](ecpro-campaigns.md)

[Managing content requests with Content Governance](ec-content-governance.md)

[Creating employee communications with Content Publishing](ec-publish-content.md)

[Content management on topic pages](cm-ec-manage.md)

[Integrated service and experience feedback management](ex-fdbck-manage.md)

