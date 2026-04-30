---
title: Configure the layout of a responsive dashboard
description: You can change the appearance of widgets; change widget layouts; change the colors of the widget title, header, and background; and show or hide widget headers.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-01-28"
reading_time_minutes: 3
breadcrumb: [Edit a responsive dashboard, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Configure the layout of a responsive dashboard

You can change the appearance of widgets; change widget layouts; change the colors of the widget title, header, and background; and show or hide widget headers.

## Before you begin

Role required: User. dashboard\_admin for all dashboards, or any role for dashboards that you own or ones that you have been given the right to edit. See [Platform Analytics dashboard roles](../../par-for-workspace/concept/pa-dashboard-roles.md) for more information about viewing and editing rights on dashboards.

**Note:** Responsive dashboards do not support the Sticky Notes widget.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  From the dashboard picker, select the dashboard that you want to edit.

3.  Click the plus sign \(![Plus sign button](../image/AddWidgetButton.png)\) to put the dashboard in edit mode.

4.  Perform any of the following actions.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d39541e114">

Action

</th><th align="left" id="d39541e117">

Steps

</th></tr></thead><tbody><tr><td id="d39541e123">

**Show or hide the widget border, header, and title**

</td><td>

1.  Point to the widget, then click the gear icon \(![Edit widget icon](../image/Pa_dashboard_cog.png)\).
2.  In the Edit Widget window, select or clear the boxes to show or hide the border, header, and title.

**Note:** If you hide the header, point to the handlebar at the top of the widget to show the icons.

3.  To align the title, select **Left**, **Center**, or **Right**.
 ![Edit Widget window with Show Border, Header, and Title boxes selected.](../image/edit-widget-window.png) When you hide the widget header, no header icons are visible, including the icon indicating that you have applied an interactive filter to the widget.

 It is not possible to change the title of a widget from within a dashboard. The title is taken from the visualization the widget is based on. Edit the visualization itself to change the title.

</td></tr><tr><td id="d39541e171">

**Change the widget title color and header color**

</td><td>

1.  Point to the widget, then click the gear icon \(![Edit widget icon](../image/Pa_dashboard_cog.png)\).
2.  In the Edit Widget window, click the color picker icon \(![Color picker icon](../image/color-picker.png)\) for Title color or Header color.
3.  In the color picker, use the slider to choose a hue and select a color to choose it. You can also enter the hexadecimal code for the color in the **Title color** or **Header color** field. Delete the hexadecimal code to return to the default title or header color.
 **Note:** When you select a dark header color, the icons in the header change to white. When you select a light header color, the icons in the header change to black.

</td></tr><tr><td id="d39541e209">

**Resize or change the layout of widgets**

</td><td>

Drag to move and resize widgets.

-   To make a widget larger, point to the widget header and then click the resize icon \(![Resize icon](../image/WidgetResizeIcon.png)\).
-   To make a widget smaller, point to the widget header and press SHIFT as you click the resize icon.


</td></tr><tr><td id="d39541e233">

**Apply a dashboard background color**

</td><td>

1.  Click the configuration icon \(![Configuration pane icon](../image/ConfigurationPaneButton.png)\) to open the Configuration pane.
2.  Select **Use custom background color** and click on the color to open the color picker. It has five option icons: Color Wheel, Color Sliders, Color Palettes, Spectrum, and Pencils.
3.  From the Sliders option, choose Grayscale, RGB, CMYK, or HSB. RGB enables you to specify hexadecimal codes.
4.  Drag any color to the palette at the bottom of the color picker to use it in other Core UI dashboard backgrounds.
5.  Uncheck **Use custom background color** to return to the default background color.
 **Note:** The selected background color applies to all tabs on the dashboard.

Core UI dashboard backgrounds are not themeable with custom colors.

</td></tr><tr><td id="d39541e276">

**Apply a quick layout to a dashboard**

</td><td>

1.  Click the configuration icon \(![Configuration pane icon](../image/ConfigurationPaneButton.png)\) to open the Configuration pane.
2.  Click a layout to snap the widgets against. Resize or change the layout of widgets as desired.


</td></tr><tr><td id="d39541e299">

**Delete a widget from the dashboard**

</td><td>

1.  Click the plus sign \(![Plus sign button](../image/icon-add-user-db.png)\) to put the dashboard in edit mode.
2.  Point to the top of the widget, then click the X icon \(![Remove widget icon](../image/RemoveWidgetButton.png)\) that appears.
 **Note:** There is no confirmation message. The widget disappears from the dashboard.

</td></tr></tbody>
</table>5.  Add content blocks to divide the content of the dashboard or to provide other content.

    From the **Add Widgets** list, select Content Blocks. For information about static content blocks, see [Configure a static HTML block](https://www.servicenow.com/docs/access?context=t_StaticHTMLBlock&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).


**Parent Topic:**[Edit a responsive dashboard](t_EditADashboard.md)

