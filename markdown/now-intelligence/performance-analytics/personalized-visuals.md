---
title: Personalized visuals
description: Configure visuals with dynamic elements to show information that applies only to the person looking at the visual on a dashboard, service portal, or Workspace canvas.Personalized visuals enable you to share the information that is most relevant to the person who uses the visual on a dashboard or canvas. You personalize the visuals of a widget by applying an element filter.To personalize a visual, you create an element filter and configure a Performance Analytics widget with the same filter. In this example, you create a filter to show only the incidents that belong to the user, then you configure a score widget with the filter you create.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Personalized visuals

Configure visuals with dynamic elements to show information that applies only to the person looking at the visual on a dashboard, service portal, or Workspace canvas.

A visual can display only the tickets assigned to a support agent or the number of tasks assigned to the team of a manager, for example. When you navigate to an Analytics Hub from a personalized visual, the Analytics Hub is personalized as well.

Use personalized visuals to push Performance Analytics down to the managers and line workers. It can be particularly useful to add widgets with personalized visuals to service portals. Enable managers who log in to their portal to see analytics only for records that belong to groups they own. Enable line workers who log in to their portal to see analytics only for records that belong to them or to one of their groups. Performance Analytics comes with the "One of my groups," "Groups I manage," and "Me" element filters to let you create such personalized visuals.

Personalization applies to Time Series, Score, and Breakdown widgets. When you configure personalized visuals, the personalization applies wherever the widget appears: a dashboard, landing page, or the Service Portal.

Technically, you personalize a visual by applying an element filter to the widget instead of specifying [breakdown elements](performance-analytics-glossary.md#). The personalization comes about through using a dynamic condition on the filter, such as \[is \(dynamic\)\] \[me\].

**Note:** Personalized visuals apply only to first-level breakdowns.

## Showing multiple elements

When an element filter returns more than one element, the scores for these elements are shown as an aggregated value on Score and Time Series widgets. However, these scores are shown separately on Breakdown widgets. The following example shows a Time Series widget and a Breakdown widget with the same personalized visuals. The logged in viewer is a member of the Technical Services Support, SAP Support, and Marketing Systems Support groups. The Time Series widget, on top, shows an aggregate view of these groups, while the Breakdown widget underneath shows a separate view.

![The time series widget shows the aggregate score of the three groups to which the viewer belongs, while the Breakdown widget shows the scores separately.](../image/personal-vis-time-series-vs-bkdown.png "Time Series widget and Breakdown widget with personalized visuals")

**Note:** When you configure a widget to follow the elements on a breakdown dashboard, your choice of an **Aggregate** or **Separate** view of multiple elements does not affect personalized visuals. For example, the following time series widget on a breakdown dashboard is configured to show multiple elements separately. This configuration applies to elements of the Category breakdown on the dashboard. However, the widget still shows the elements of Assignment Group from the personalized visual as an aggregate.

![A widget on a breakdown dashboard showing multiple elements from the breakdown dashboard separately but showing multiple elements from the personalized visual as an aggregate](../image/personal-vis-bkdown-dashboard.png "Widget with personalized visual on breakdown dashboard")

For more information, see [Configure widgets for breakdown dashboards](../task/set-up-widgets-for-breakdown-dashboards.md).

## Configure a widget with personalized visuals

Personalized visuals enable you to share the information that is most relevant to the person who uses the visual on a dashboard or canvas. You personalize the visuals of a widget by applying an element filter.

### Before you begin

**Note:** Personalized visuals apply only to first-level breakdowns.

Role required: pa\_admin, pa\_power\_user

### Procedure

1.  Create one or more [breakdown element filters](c_BreakdownElementFilters.md#) with a dynamic condition, such as \[is \(dynamic\)\] \[me\].

    Before you create an element filter, verify whether you can use an existing one.

2.  Navigate to **Performance Analytics** &gt; **Widgets**.

3.  Select the widget that you want to personalize.

4.  On the Widget form, select the breakdown that applies to the personalization, such as Assigned To or Assignment Group.![Widget form with breakdown and elements filter fields highlighted.](../image/personalize-widget.png)

5.  On the Element Settings tab, click the magnifier to select the Elements filter that applies to the breakdown and personalizes the widget.

6.  Click **Update**.


### Result

On a dashboard, Service Portal, or canvas that has this widget, the widget shows breakdown elements filtered for the viewer.

## Personalized visuals example

To personalize a visual, you create an element filter and configure a Performance Analytics widget with the same filter. In this example, you create a filter to show only the incidents that belong to the user, then you configure a score widget with the filter you create.

### Before you begin

Role required: pa\_admin, pa\_power\_user

Element filters are persistent. Once you create an element filter, you can apply it to multiple visuals.

### About this task

In this example, you create an element filter that uses the `Users.Active` breakdown source to filter on the user viewing a widget. Then you configure the widget to use the new element filter, and then you view the widget on a dashboard.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Elements Filters** and create a new elements filter with the details in the Element filter fields table.

    For more information, see [Create an elements filter](c_BreakdownElementFilters.md#).

<table id="table_yvq_m5s_vv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown source

</td><td>

Click the magnifier and choose `Users.Active`. The element filter is available for any breakdowns based on this breakdown source.

</td></tr><tr><td>

Facts table

</td><td>

Choose the breakdown source facts table. The facts table for `Users.Active` is **Group Member \[sys\_user\_grmember\]**.

</td></tr><tr><td>

Filter

</td><td>

Specify the filter conditions to limit the available elements. Only elements that meet these conditions are displayed when you apply this element filter.For this element filter, specify `[User][is (dynamic)][Me]`.

 For [Personalized visuals](personalized-visuals.md#), the operator in the filter condition must be `[is (dynamic)]`.

</td></tr><tr><td>

Roles

</td><td>

Select any roles that a user must have to select this element filter on a widget form. A user must have at least one of the specified roles. If no roles are specified, all users who can edit a Performance Analytics widget can add this element filter. For this example, we don't want to limit who can select the filter.

</td></tr></tbody>
</table>    ![Elements filter personalized visual example with user is dynamic Me specified as the condition.](../image/elements-filter-example.png)

2.  Create a score widget with the details in the widget fields table.

    For more information, see [Performance Analytics widgets](c_Widgets.md). The important thing to know is that the elements filter applies to the indicator's first-level breakdown.

    |Field|Description|
    |-----|-----------|
    |Name|My open incidents|
    |Indicator|Number of open incidents|
    |Breakdown|Select `Assigned To`. If this breakdown is not available, add it to the indicator. For more information, see [assign and map breakdowns](../task/create-breakdown-mapping.md#).|
    |Type|Score|
    |Visualization|Latest Score|

3.  On the **Element Settings** tab of the widget, select `Me`, the Elements filter you created in step 1.

    Users who can see the widget My open incidents, see the score only for the incidents assigned to them.

4.  Add the My open incidents widget to a dashboard.


### What to do next

Log in as a user who is assigned incidents and open a dashboard with the My open incidents widget. The My open incidents widget shows the score only for the incidents assigned to that user. ![The My open incidents single score widget showing eight open incidents for the logged in user.](../image/my-open-incidents-widget.png)

Click the score to open the Analytics hub for this indicator, filtered on the user looking at the dashboard. ![Analytics hub for the Number of open incidents indicator filtered on the user named ITIL user.](../image/my-open-incidents-drilldown.png)

