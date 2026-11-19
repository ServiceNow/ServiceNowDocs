---
title: Use the Capture element dialog
description: Identify and capture the elements on a web-based, Java, or Windows application screen by using the Capture element dialog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-context-dialog.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Chromium connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Capture element dialog

Identify and capture the elements on a web-based, Java, or Windows application screen by using the Capture element dialog.

## Before you begin

The Capture element dialog is available in the following connectors:

-   Java
-   Chromium
-   IE
-   Windows
-   Universal App Connector

Role required: none

## Procedure

1.  Move the mouse device to the element that you want to capture.

    The Capture element dialog shows information.

    \[Omitted image "context-dialog-window.png"\] Alt text: Capture dialog.

    **Note:** By default, the name of the element appears in the **Name** field of the Capture element dialog. If the name of the element is not available, its Id appears in the **Name** field. Otherwise, the element type appears in the **Name** field.

2.  To capture the element, select the Add element icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add element icon.\).

    **Note:**

    -   To prevent the Capture element dialog from moving after you have moved the mouse pointer over the screen element you want to capture, press the CTRL key.
    -   You can optionally provide a custom name to the element in the **NAME** field. In that case, the element is captured with the custom name in both the **Screens and elements** pane and under the Connector object in the Global Objects. Else, it's captured with the default name the target application provides.
    -   If you capture the same element multiple times, the Capture Dialog provides a unique name to each instance of the element. For example, if you capture an H4 element three times, its naming convention can be like H4, H4\_1, and H4\_2.
3.  To capture elements that are higher in the hierarchy of the current element, select the move to parent element icon \(\[Omitted image "move-to-parent-tag-icon.png"\] Alt text: Move to parent element icon.\).

    For example, the elements in an HTML table elements appear in a hierarchical order. The `table` element is the highest and `th` is lowest. If you try to capture an HTML table elements, the Capture element dialog will move from `th` to `tr` to the `table` element. The image shows the hierarchy of elements.

    \[Omitted image "element-hierarchy.png"\] Alt text: Element capture hierarchy.

4.  To capture more elements, move the mouse pointer over other elements and repeat the previous steps.

5.  To close the Capture element dialog, select the close Capture element dialog icon \[Omitted image "close.png"\] Alt text: Close context dialog icon..

    The captured elements appear in both the **Screens and elements** pane and under the Connector object in the Global Objects.

    \[Omitted image "elements-captured.png"\] Alt text: Elements captured.


**Parent Topic:**[Chromium connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/chrome-connector.md)

