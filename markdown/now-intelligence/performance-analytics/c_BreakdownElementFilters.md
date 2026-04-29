---
title: Element filters
description: Element filters enable you to specify or limit the displayed breakdown elements on visualizations.Select the breakdown source and filter conditions to filter breakdown elements from that breakdown source.Element filters can be seen in a Platform Analytics data visualization or on KPI Details. In the Core UI, they can be seen in Performance Analytics widgets or the Analytics Hub. Some restrictions apply.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Element filters

Element filters enable you to specify or limit the displayed breakdown elements on visualizations.

An elements filter consists of a conditional filter or related list conditions and the breakdown source that the conditions apply to.

**Tip:** Use an elements filter with dynamic conditions to create personalized visuals on a widget. For more information, see [Personalized visuals](personalized-visuals.md#).

**Parent Topic:**[Indicator breakdowns](c_CreatingBreakdowns.md)

**Related topics**  


[Analytics Hub](c_UsePerformanceAnalyticsScorecards.md)

[Examining indicators with KPI Details](../../par-for-workspace/reference/kpi-details-components.md)

[Performance Analytics widgets](c_Widgets.md)

## Create an elements filter

Select the breakdown source and filter conditions to filter breakdown elements from that breakdown source.

### Before you begin

Role required: pa\_data\_collector or admin

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Elements Filters** and create a new record \(see table for field descriptions\).

<table id="table_yvq_m5s_vv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown source

</td><td>

Select the breakdown source you want to create an element filter for. The element filter is available for any breakdowns based on this breakdown source.

</td></tr><tr><td>

Facts table

</td><td>

Read-only. Displays the breakdown source facts table.

</td></tr><tr><td rowspan="2">

Filter

</td><td>

CONDITIONS: Specify the filter conditions to limit the available elements. Only elements that meet these conditions are displayed when you apply this element filter.For example, if the breakdown source facts table is User \[sys\_user\], you can add a filter condition to include only users in the HR department. This filter condition is \[Department\]\[is\]\[HR\].

 For [Personalized visuals](personalized-visuals.md#), the operator in the filter condition must be `[is (dynamic)]`.

</td></tr><tr><td>

RELATED LIST CONDITIONS: Include a relationship with another table in the conditions. For example, you could create an element filter on the Groups breakdown source, which uses the Group \[sys\_user\_group\] table. If you added a related list condition on Incident \[incident\]-&gt;Assignment group, you would get only groups that had an incident assigned to them. If this condition included \[\[Created\]\[on\]\[Last 6 Months\]\], you would get groups that were assigned an incident that was created within the last six months. ![Element filter form showing related list condition example](../image/element-filters-related-list-cons.png)

</td></tr><tr><td>

Roles

</td><td>

Select any roles that a user must have to select this element filter on a widget form. A user must have at least one of the specified roles. If no roles are specified, all users who can edit a Performance Analytics widget can add this element filter.

</td></tr></tbody>
</table>
### What to do next

Use an element filter with dynamic conditions to create personalized visuals on a widget. For more information, see [Personalized visuals](personalized-visuals.md#).

All widget indicators that use this elements filter and all diagnostic results that mention this elements filter are listed at the bottom of the elements filter record.

## Element filters in visualizations

Element filters can be seen in a Platform Analytics data visualization or on KPI Details. In the Core UI, they can be seen in Performance Analytics widgets or the Analytics Hub. Some restrictions apply.

You can select the element filter in the following ways on different visualizations:

-   On the Core UI Analytics Hub: When you select a breakdown, if that breakdown has elements filters, you get a list of them to choose from.
-   In a Core UI Performance Analytics widget: When configuring the widget, fill in the **Elements filter** field in the **Element settings** tab. Only breakdown, time series, and score widgets support elements filters. For time series and score widgets, an elements filter replaces the first-level breakdown element. For breakdown widgets, an elements filter limits the elements that are shown.
-   In a Core UI widget indicator on a time series widget: Select a filter in the **Elements filter** field in the Element Settings. You must first select a breakdown with element filters on its breakdown source.

    **Note:** The names of all elements that get applied are appended to the name or label of the indicator.

-   On KPI Details in Platform Analytics: When you select a breakdown in the **Filters** pane, if that breakdown has elements filters, you get a list of them to choose from under **Refine by**.
-   In a Platform Analytics data visualization: While configuring the data visualization, select an indicator data source, a breakdown, and the \[is \(dynamic\)\] operator. Any elements filters for that breakdown are then available in the **Element** field. Only automated indicators with the Count, Minimize, or Maximize aggregate are supported.

In all of these cases, you can select an elements filter only if you first select a breakdown with at least one elements filter on its breakdown source. You may also need a certain role to select an elements filter, depending on the configuration of that filter.

Besides specifying an elements filter on a visualization, you can specify a **Default element filter** on a breakdown record. That elements filter is selected automatically for that breakdown in any visualization. Users that view the breakdown on the Analytics Hub or on KPI Details can change or clear the selected elements filter.

**Note:** It is not possible to change elements filters that are used to personalize visuals when simply viewing the visual on a dashboard or workspace. Only a user with the rights to edit the underlying widget or data visualization can change the elements filter. For more information, see [Personalized visuals](personalized-visuals.md#).

