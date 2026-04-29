---
title: Popular topics widget
description: Popular topics widget lets you quickly view and access the most popular topics. You can configure the instance options to control the appearance of the widget, such as the title, number of topics, display size, and border color.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Employee Center browse experience widgets, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Popular topics widget

Popular topics widget lets you quickly view and access the most popular topics. You can configure the instance options to control the appearance of the widget, such as the title, number of topics, display size, and border color.

## Before you begin

Role required: sp\_admin or admin

## About this task

Employee Center uses an algorithm to determine which topics must appear on the widget.

**Note:** Retired articles are not considered for topic popularity calculation.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

    The Employee Center home page is displayed.

2.  Press and hold the control key, right-click the Popular topics widget, and then select **Instance Options**.

    ![Popular topics widget instance options](../images/popular-inst-opts.png)

3.  Configure the instance options.

<table><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the widget. For example**Popular topics** for EC

**Browse help content** for Kiosk

</td></tr><tr><td>

Number of topics

</td><td>

Number of topics you want to appear on the widget. Default value: 8For Kiosk, the default value is 6.

</td></tr><tr><td>

Display size

</td><td>

Size of the card tiles on the widget. The choices are:-   **Normal** \(Default for EC\)
-   **Small**
For Kiosk, the default size is small.

</td></tr><tr><td>

Border color

</td><td>

The border color of the widget. The choices are:-   **Border-primary**
-   **Border-secondary**
-   **Border-tertiary**
-   **Hexcode**
Default value: Border-tertiary

</td></tr><tr><td>

Hexcode

</td><td>

Option to specify a hexcode for the border color. Enter a value in this field only if you select **Hexcode** in the **Border color** field.

</td></tr><tr><td>

Show topic icon

</td><td>

Option to show the topic icon. This option is selected by default. You can hide the topic icon by deselecting this option.

</td></tr><tr><td>

Load configuration

</td><td>

Order in which the page and widgets data loads. Select one of the following options:-   Asynchronous: First the page loads, then the widgets data loads. Users see content appear in the widgets as soon as each individual widget loads.
-   Synchronous: Page and widget data loads at the same time. The page remains blank until all the data loads.


</td></tr><tr><td>

Show empty state

</td><td>

Option to show the widget with empty state message.

</td></tr><tr><td>

Widget behavior during high load

</td><td>

Option to show the view from the available options:-   None
-   Lite view: Select this option to minimize the load and display a message that the portal is experiencing heavy usage.
-   Regular view: Select this option for regular view.


</td></tr></tbody>
</table>4.  Click **Save**.


**Parent Topic:**[Employee Center browse experience widgets](../concept/custom-widget-landing-ec.md)

