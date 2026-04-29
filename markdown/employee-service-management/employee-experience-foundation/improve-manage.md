---
title: Managing portal performance
description: Discover ways to reduce portal loading time and enhance portal display.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Managing portal performance

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

For step-by-step instructions to enable asynchronous loading, see [Improve portal load time with asynchronous loading](../task/optimize-performance-of-employee-center-home-page.md) and [Configure Mega menu async load system properties](../task/config-mega-menu-async-load.md).

## Optimize connected content

To improve page load times, limit the number of connected content items in topics. Connect only the required content to topics and remove any unnecessary content like outdated or unpublished versions.

For guidance on managing connected content, see [Create and associate topics](../task/create-topics-for-taxonomy.md) and [Taxonomy and connected content](track-new-content.md).

-   **[Portal performance optimization](ec-load-experience-optimization.md)**  
Learn more about the heavy-load and high-traffic scenarios and ways to optimize the user experience and portal performance.
-   **[Improve portal load time with asynchronous loading](../task/optimize-performance-of-employee-center-home-page.md)**  
Reduce the time employees spend waiting for the portal to load by enabling widgets to load data asynchronously. This allows widgets to display information as it becomes available, improving overall portal performance.
-   **[Improve the image load time on Employee Center](../task/optimize-image-loading.md)**  
Use CDN URLs to reduce the load time of the banner images, background images, and app icons on the Employee Center portal.
-   **[View widget performance metrics](../task/view-widget-performance-metrics.md)**  
View the metrics provided by the performance window to identify which widgets take the longest to load data.
-   **[Add hotspots to track custom widget performance](../task/add-hotspots-track-custom-widget-performance.md)**  
Hotspots help capture and log widget load times, which enables better debugging of long portal load times.

**Parent Topic:**[Configuring Employee Center Pro](configuring-employee-center-pro.md)

