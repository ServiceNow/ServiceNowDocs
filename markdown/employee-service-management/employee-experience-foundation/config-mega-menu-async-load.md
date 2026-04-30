---
title: Configure Mega menu async load system properties
description: The mega menu async improves the homepage interactivity by loading the Mega Menu in the background, enabling you to engage with visible content faster.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [mega menu, servicenow mega menu, menu taxonomy]
breadcrumb: [Mega menu configuration, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure Mega menu async load system properties

The mega menu async improves the homepage interactivity by loading the Mega Menu in the background, enabling you to engage with visible content faster.

## Before you begin

Role required: admin

## About this task

You can decouple the mega menu load from the homepage using the asynchronous process.

-   Use the mega menu async load system properties to display placeholder elements resembling the final content layout while the actual data is being fetched.
-   Show a blank screen or a spinner, skeleton loaders create an improved perception of performance and user experience.
-   Continue work on homepage and other widget items irrespective of the mega menu load time.
-   Enable cache, reduce the load-time, and improve responsiveness.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The list of properties in the System Properties \[sys\_properties\] table appears.

2.  Search for the following properties and click open.

    ![Async load system properties with sample timeout and skeleton load](../images/mm-sys-properties-megamenu.png "Megamenu async load system properties")

    1.  Toggle **sn\_ex\_sp.megamenu \_async\_load** to enable or disable the asynchronous mega menu loading feature.

        -   True: Show skeleton loader
        -   False: \(Default\)
    2.  Toggle **sn\_ex\_sp.megamenu\_async\_load\_skeleton\_view** to enable or disable the Mega Menu skeleton loader.

        -   True: Show the skeleton loader until the async flow gets the data.
        -   False: Show that previous session data until the async flow gets the data and then update the UI. For more information, see [User portal data map](user-portal-data-map.md).
    3.  Specify the **sn\_ex\_sp.megamenu\_async\_timeout** timeout duration \(in milliseconds\) for loading the asynchronous mega menu.

        The default value is 15000. After 15 seconds, the UI aborts the data load and displays an error message

        ```
        There was a problem with loading the menu. Please try again later.
        ```

        .

3.  Click **Save** or **Update**.


## Result

The system properties improve the async load and overall performance.

**Related topics**  


[Portal performance optimization](../concept/ec-load-experience-optimization.md)

[User portal data map](user-portal-data-map.md)

