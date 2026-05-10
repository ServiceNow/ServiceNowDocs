---
title: Portal performance optimization
description: Learn more about the heavy-load and high-traffic scenarios and ways to optimize the user experience and portal performance.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Admin configurations, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Portal performance optimization

Learn more about the heavy-load and high-traffic scenarios and ways to optimize the user experience and portal performance.

Using the following performance enhancements, you can improve the overall user experience.

-   **Optimized high-load experience**: Optimizes the employee experience during high usage such as live events, major announcements.

    For more information, see [High-traffic experience](ec-load-high-traffic.md).

-   **Defer widget load**: Speeds up initial page rendering by loading only essential content first and deferring non-critical elements until later. Delay loading non-critical resources until after the main content is rendered.

    For more information, see [Defer load in Employee Center](ec-load-expe-defer-load.md).

-   **Mega menu async load**: Loads resources or data asynchronously in the background without blocking the main thread.

    For more information, see [Configure Mega menu async load system properties](../task/config-mega-menu-async-load.md).

-   **Skeleton load**: Improves perceived performance by displaying placeholder elements \(like grey boxes or lines\) while actual content is loading. This placeholder UI reassures employees that the system is functional and reducing the wait times.

Admins can select regular or light modes by configuring your widget instances.

**Note:**

-   Skeleton loaders are not applicable to the customized widgets.
-   Defer load configuration at the SP Portal level overrides the instance-level configurations.

**Parent Topic:**[Managing portal performance](improve-manage.md)

**Related topics**  


[Configure Mega menu async load system properties](../task/config-mega-menu-async-load.md)

[Modify defer load instance option](../task/config-defer-load-instance-option.md)

[High-traffic experience](ec-load-high-traffic.md)

