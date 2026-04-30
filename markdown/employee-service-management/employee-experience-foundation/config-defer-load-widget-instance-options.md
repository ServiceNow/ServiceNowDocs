---
title: Modify homepage banner instance for high-traffic
description: You can configure the instance options to control the display of widgets and improve the homepage banner instance for high-traffic experience.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [High-traffic experience, Portal performance optimization, Admin configurations, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Modify homepage banner instance for high-traffic

You can configure the instance options to control the display of widgets and improve the homepage banner instance for high-traffic experience.

## Before you begin

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **Self-Service** &gt; **Employee Center**.

    The Employee Center home page is displayed.

2.  Press and hold the control key on the keyboard, right-click the widget, and then select **Instance Options**.

3.  Configure the instance options.

    ![Instance option fields and description](../images/defer-homepage-instance.png "Homepage banner instance")

<table id="table_cq4_vdk_crb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visibility

</td><td>

The choices are **Yes** and **No**. For high-load scenarios, the default is yes.

</td></tr><tr><td>

Alert message type

</td><td>

Type of the message to display on the widget. The choices are:-   **Warning** \(Default\)
-   **Information**
-   **Error**


</td></tr><tr><td>

Alert message text

</td><td>

Message text that you want to display, for example, ```
Some information may be temporarily unavailable as we're experiencing heavy usage. Try again later.
```

</td></tr><tr><td>

Show dismiss action icon

</td><td>

Icon to click and dismiss the message.

</td></tr></tbody>
</table>4.  Click **Save**.

    **Note:** The homepage banner message is available in the EC, EC Pro, and Kiosk home pages.


## What to do next

You can find a similar experience for the following widgets:

-   **Popular topics**: During high-traffic, the widget displays the message.

    ```
    We're experiencing heavy usage. Try again later.
    ```

    For more information, see [Popular topics widget](config-popular-topics.md).

-   **My active items**: During high-traffic, the widget doesn't display the count of items.

**Related topics**  


[Defer load in Employee Center](../concept/ec-load-expe-defer-load.md)

