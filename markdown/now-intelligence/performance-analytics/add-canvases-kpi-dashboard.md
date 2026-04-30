---
title: Add canvases to a dashboard tab
description: Combine analytics artifacts and widgets to create visual components, called canvases, on a KPI Composer dashboard mock-up. "Widgets" include reports, interactive filters, Spotlight, and content blocks.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Designing dashboards, Design your indicator solution, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add canvases to a dashboard tab

Combine analytics artifacts and widgets to create visual components, called canvases, on a KPI Composer dashboard mock-up. "Widgets" include reports, interactive filters, Spotlight, and content blocks.

Prerequisites
:   [Add a dashboard](add-dashboard-kpi-comp.md#)

:   [Add tabs and rows to a dashboard](add-tabs-kpi-dashboard.md)

## Before you begin

You have an existing KPI Composer project with a complete draft of the KPI tree in the Analytics tab. You also have at least one dashboard defined in the Dashboard Visualization tab. Lastly, one of these dashboards has at least one tab, containing at least one row.

Role required: sn\_kpi\_composer.user \(own project\), sn\_kpi\_composer.admin \(any project\), admin. No role required for responsible user or user with edit access from project sharing.

## Procedure

1.  Open a **KPI Composer** project and navigate to the Dashboard Visualization tab.

2.  Select one of the dashboards in the tab.

    Select a dashboard with at least one tab and a row with empty canvas slots.

3.  In the upper right of the Dashboard Visualization tab, expand the Artifacts icon \(![](../image/kpi-comp-elements-icon.png)\).

4.  Select an artifact that you want to represent in a canvas slot, and drag the artifact to the slot.

    You previously defined these artifacts in the KPI tree in the Analysis tab.

    You can drop multiple artifacts into the same canvas slot. You can even drop artifacts onto a canvas slot after you have added a widget to that slot. However, you cannot drop artifacts onto a canvas slot that contains a content block or an interactive filter widget.

    When you drag an artifact onto an unnamed canvas, you give the name of the artifact to the canvas. Dragging additional artifacts onto the canvas does not change the name.

    If you have selected any personas in the dashboard properties, only the artifacts that are linked to those personas are available.

5.  In the upper right of the Dashboard Visualization tab, expand the Widgets icon \(![](../image/kpi-comp-widgets-icon.png)\).

6.  Decide which widget represents the data in the artifact you previously selected, and drag it to the same canvas slot.

    Widget designs use static images and not actual data visualizations.

    Interactive Filter widgets only affect Report widgets that are on the same dashboard.

    Spotlight "widgets" represent Spotlight interactive analysis, which is usually accessed through a shared URL instead of a report on a dashboard. For more inforrmation, see [Spotlight interactive analysis](../concept/spotlight-interactive-analysis.md).

    To replace a widget on a canvas, drag another widget onto it. The title of the original widget remains, unless you replace it with a Content Block. Replacing widgets does not affect artifacts associated with a canvas.

    After you drag a widget, the Canvas Details dialog opens.

7.  Fill in the Canvas Details, as follows:

    **Note:** To change the Canvas Details of an existing widget, click the pencil icon \(![](../image/kpi-composer-edit-item.png)\) on the canvas. This icon appears when you point to the top-right corner of a canvas.

<table id="table_hqq_c3t_tnb"><thead><tr><th>

Field

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

Widget type

</td><td>

Select the type of widget that represents the artifact. If you have already selected a widget type, you can change that type. The other fields depend on which widget type you select.

</td></tr><tr><td>

Title

</td><td>

Enter a meaningful title, such as `Percent of incidents per assignment group`.

</td></tr><tr><td>

Description

</td><td>

Information about the widget for internal use, such as `Widget based on formula indicator % open incidents by assignment group`

.This entry is not visible in the widget.

</td></tr></tbody>
</table><table id="table_pa-properties"><thead><tr><th>

Field

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

Visualization type

</td><td>

Decide which visualization best illustrates the element.

</td></tr><tr><td>

Follow element

</td><td>

Set whether this widget follows the breakdown element that a viewer selects on a Performance Analytics breakdown dashboard.

</td></tr><tr><td>

Time Series

</td><td>

Show results in daily, weekly, or monthly increments.

</td></tr><tr><td>

Measurement

</td><td>

The artifact measured in this widget. You can select any artifact in this field, not only Measurements.

</td></tr><tr><td>

PA Widget

</td><td>

Select an existing Performance Analytics widget that matches this mock-up widget. For more information, see [Performance Analytics widgets](../concept/c_Widgets.md).

</td></tr></tbody>
</table><table id="table_content-block"><thead><tr><th>

Field

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

Content block

</td><td>

Select from an existing content block. For more information, see [Content blocks](https://www.servicenow.com/docs/access?context=c_ContentBlocks&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table><table id="table_interactive-filters"><thead><tr><th>

Field

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

UI control type

</td><td>

Choose the UI style for the interactive filter.

</td></tr><tr><td>

Interactive filter

</td><td>

Select an existing interactive filter. For more information, see [Interactive Filters](../../dashboards/concept/c_HomepagePublishers.md)

</td></tr></tbody>
</table><table id="table_reports"><thead><tr><th>

Field

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

Visualization type

</td><td>

Decide which visualization best illustrates the element.

</td></tr><tr><td>

Follow interactive filter

</td><td>

Set whether the report can be filtered by an interactive filter on the dashboard. If you select Yes, also include an interactive filter widget.

</td></tr><tr><td>

Measurements

</td><td>

Select the Measurements artifact that this report shows.

</td></tr><tr><td>

Report

</td><td>

Select an existing Report. For more information, see [Creating reports](../../reporting/reference/report-types-creation-details-rd.md)

</td></tr></tbody>
</table><table id="table_spotlights"><thead><tr><th>

Field

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

Measurements

</td><td>

Select the Measurements artifact that this report shows.

</td></tr><tr><td>

Spotlight group

</td><td>

Select an existing Spotlight group. For more information, see [Ranking records with Spotlight](../concept/spotlight.md).

</td></tr></tbody>
</table>
## Result

You have an artifact from your analysis and a visualization to illustrate that artifact on your dashboard.

## Adding a canvas to a dashboard

**Note:** In this short animation, a canvas is added to the Quality of Service tab of the Customer Experience dashboard. The user first picks an artifact from their KPI Tree and then selects a widget to illustrate that artifact. ![Adding a canvas to a dashboard](../image/kpi-comp-add-canvas.gif)

## What to do next

When you have populated a dashboard, you can change the row order, widget order, or widget title in the artifact banner. The following short animation demonstrates how to move dashboard components.

![Design artifacts being moved around a KPI Composer dashboard mock-up](../image/kpi-comp-move-elements.gif)

**Parent Topic:**[Designing dashboards](../concept/create-a-dashboard-mock-up.md)

**Previous topic:**[Add tabs and rows to a dashboard](add-tabs-kpi-dashboard.md)

**Next topic:**[Create a dashboard tab template](kpi-comp-create-dashboard-template.md)

