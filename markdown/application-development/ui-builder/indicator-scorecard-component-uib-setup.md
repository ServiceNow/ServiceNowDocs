---
title: Indicator scorecard component setup
description: The Indicator scorecard component allows users to visualize and compare data between multiple Performance Analytics indicators. It highlights the information regarding the last score collected, the change from the previous data point, the trend over time, and the value of the target to achieve.​Configure the filtering and sorting capabilities of your Indicator scorecard with these properties.Select event handlers to configure the actions \(events\) provided with the Indicator scorecard component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/indicator-scorecard-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Indicator scorecard component setup

The Indicator scorecard component allows users to visualize and compare data between multiple Performance Analytics indicators. It highlights the information regarding the last score collected, the change from the previous data point, the trend over time, and the value of the target to achieve.​

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Indicator scorecard that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "indicator-scorecard-component-tree.png"\] Alt text: Component tree showing indicator scorecard named MyWorkspace indicator scorecard

2.  Select the Indicator scorecard component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Indicator scorecard label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Indicator scorecard component properties

Configure the filtering and sorting capabilities of your Indicator scorecard with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_j2v_zll_4nb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scorecard Type

</td><td>

scorecardType

</td><td>

List to select from scorecard types. Options include:-   **List**: Shows the list of indicators and metrics as columns.
-   **Pivot**: Shows indicators as rows and breakdown as columns or vice versa.

</td></tr><tr><td>

Show Header

</td><td>

showHeader

</td><td>

Toggle to show or hide header.

</td></tr><tr><td>

Heading level

</td><td>

headingLevel

</td><td>

HTML heading tag level of the header title \(H1 to H6\)Default: H2

</td></tr><tr><td>

Show header separator

</td><td>

showHeaderSeparator

</td><td>

When true, displays a line separating the header from the rest of the componentDefault: false

</td></tr><tr><td>

Title

</td><td>

title

</td><td>

Component title.

</td></tr><tr><td>

Use large font size

</td><td>

headingVariant

</td><td>

Defines the styles used to render the header title. When true, the non-bold Title-tertiary font is used. Otherwise, the bold Header-secondary font is used.Default: false

</td></tr><tr><td>

Description

</td><td>

description

</td><td>

Component description displayed in the info icon during runtime.

</td></tr><tr><td>

Source definition

</td><td>

sourceType

</td><td>

List to select from source definition types. Options include:-   **Condition based**: Allows you to set a condition to determine which indicators to display.
-   **Manually selected**: Allows you to add indicators manually one at a time.

You can set a breakdown and element to filter each indicator that you select manually.

If you select only one indicator, you can set **Show only breakdowns** to show the elements of that indicator without the indicator score.

-   **Indicator group**: Sets an indicator group as the source.

</td></tr><tr><td>

Filter

</td><td>

query

</td><td>

Encoded query string for filtering which indicators to show. To create a filter statically, use the condition builder that is provided.**Note:** Only available if **Source definition** is Condition based.

</td></tr><tr><td>

Indicator group

</td><td>

indicatorGroup

</td><td>

Filters the table based on an indicator group from the list.**Note:** Only available if **Source definition** is Indicator group.

</td></tr><tr><td>

Breakdown

</td><td>

breakdowns

</td><td>

A JSON array of the breakdowns and their associated elements that you have selected to display. The objects in the array each have a breakdownId, a breakdownLabel, and a child array of elementIds.

</td></tr><tr><td>

Show breakdown elements as columns

</td><td>

swapBreakdownsAsColumns

</td><td>

Displays the breakdown as columns and indicator as rows.**Note:** Only available when **Scorecard Type** is Pivot.

</td></tr><tr><td>

Show only breakdowns

</td><td>

showBreakdownsOnly

</td><td>

If set to true, hides indicator total and shows only breakdown elements and the metrics selected. Available only on List scorecards with sourceType=Manually selected and only one indicator selected.Default: false

</td></tr><tr><td>

Allow change breakdown

</td><td>

allowChangeBreakdown

</td><td>

When true, the viewer can change the breakdown that is displayed. Available only on List scorecards and only when **Show only breakdowns** is true.Default: false

</td></tr><tr><td>

Breakdown visibility selector

</td><td>

breakdownVisibilitySelector

</td><td>

When true, the breakdown selector is visible to viewers of the scorecard. When false, the breakdown selector has to be opened from the More options menu. Only available when **Allow change breakdown** is true.

Default: false

</td></tr><tr><td>

Max number of groups

</td><td>

perPage

</td><td>

The maximum number of elements to show for a breakdown. If you do not specify the elements to show in **Filter elements** \[breakdownLabel\], the elements that are shown depend on the breakdown source and the value of **Sort direction** \[sortDir\]. For example, consider the Assignment Group breakdown, which uses string fields from the Group \[sys\_group\] table. If the **Max number of groups** is the default 5, you show either the first 5 elements or the last 5 elements alphabetically, depending on whether the sort direction is ascending or descending. In such cases, consider selecting the elements in the **Filter elements** field.Default: 5

</td></tr><tr><td>

Filter elements

</td><td>

breakdowns:elementId

</td><td>

Select the elements to show for the relevant breakdown. If you don’t select any elements, all elements up to the max number of groups are shown.

</td></tr><tr><td>

Metrics

</td><td>

metrics

</td><td>

Selects analytics to show in the indicator list. You can drag metrics tiles to reorder them.Default: lastScore, changeAndChangePercent, target, trend

</td></tr><tr><td>

Time series aggregation

</td><td>

aggregateId

</td><td>

Time series aggregation to apply to all Indicators selected. To learn more about time series aggregations, see [Applying time series aggregations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/applying-time-series-aggregations.md).

</td></tr><tr><td>

Sort by

</td><td>

sortBy

</td><td>

The column to sort the indicators by. Values: Name, Score, Target, Change, changePercent, indicator\_group

 Default: Name

</td></tr><tr><td>

Sort Direction

</td><td>

sortDir

</td><td>

The sorting direction for the indicators and/or breakdown elements. The effect on breakdown elements varies depending on the breakdown source. For example, breakdown elements from the Choice \[sys\_choice\] table are sorted according to the value of the Sequence field, whereas breakdown elements from Group \[sys\_group\] are sorted alphabetically according to the Name field.Values: Ascending \(Asc\) or Descending \(Desc\)

 Default: Asc

</td></tr><tr><td>

Follow filters

</td><td>

followFilters

</td><td>

Enable to filter the scorecards with filters set for the workspace.Default: true

</td></tr><tr><td>

Show filter icon

</td><td>

showFilterIcon

</td><td>

Show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.Default: true

</td></tr><tr><td>

Enable drilldown

</td><td>

enableDrilldown

</td><td>

Redirects user to underlying data when they click a data point. Toggle off to prevent this interaction.Default: true

</td></tr><tr><td>

Show filter element

</td><td>

showFilterElement

</td><td>

Option to show the applied filter elements next to the indicator name. If a filter cannot apply to a visualization, the elements do not show. Toggle off to hide the filter elements and show only the indicator name.Default: true

</td></tr><tr><td>

Show bookmark

</td><td>

showFavorite

</td><td>

Toggle to show or hide a column of bookmarks. When on, users can bookmark indicators and breakdowns for themselves.Default: true

</td></tr><tr><td>

Show indicator info

</td><td>

showIndicatorInfo

</td><td>

Toggle to show or hide the indicator information icon. When shown, indicator information includes information about the last collection date, frequency of collection, and direction.Default: true

</td></tr><tr><td>

Show bookmarked items only

</td><td>

showBookmarkedOnly

</td><td>

Toggle on to show only bookmarked indicators or breakdown elements.Default: false

</td></tr><tr><td>

Use data cache Requires the latest Data Visualizations application from the ServiceNow Store

</td><td>

useDataCache

</td><td>

If activated, user queries are cached. This cached data is used on page refreshes instead of the database being queried. The load time for the data visualization is thereby shortened.The user can get current data on demand by using the manually refreshing the data visualization with the **Refresh** button.

Turning on **Real time update**, if that is available for this data visualization, overrides the use of data caching. Setting a value for **Refresh after being away for X min.** or **Refresh requested** also disables data caching.

Default: false

</td></tr><tr><td>

Show cache time Requires the latest Data Visualizations application from the ServiceNow Store

</td><td>

showCacheTime

</td><td>

When true, shows an icon that indicates that returned data are from the cache. On hover, the user sees how old the data is. Applies only when useDataCache is true.Default: true \(only when useCacheData is true\)

</td></tr><tr><td>

Cache expiration time \(h\) Requires the latest Data Visualizations application from the ServiceNow Store

</td><td>

cacheExpirationTime

</td><td>

Number denoting the lifespan of cached data in hours. When the lifespan is exceeded, a page refresh results in the cached data being updated through a database query.A value for **Refresh after being away for X min** or **Refresh requested** can result in the data cache being updated before its expiration time.

Default: 0

</td></tr><tr><td>

Max elements per page

</td><td>

pageSize

</td><td>

The page size as determined by the maximum number of indicators or breakdown elements that the page can show. The increments are 10, 20, 50, and 100 indicators/elements. Default: 10

​

</td></tr><tr><td>

Target color scheme

</td><td>

colorSchemeId

</td><td>

Selects a target color scheme. By default, the value defined in the **Default indicator target color scheme** property on the Performance Analytics Properties page is applied.

</td></tr><tr><td>

Show alternate row colors

</td><td>

showAlternateRowColors

</td><td>

Alternates colors of rows.

</td></tr><tr><td>

Show row lines

</td><td>

showRowDividers

</td><td>

Displays border row lines to show separate rows.

</td></tr><tr><td>

Show column lines

</td><td>

showColumnDividers

</td><td>

Displays border column lines to show separate columns.

</td></tr></tbody>
</table><table id="table_xcz_lr2_b1c"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow chart interaction \[chartInteractionEnabled\]

</td><td id="entry-allow-chart-interaction">

Enable an event to occur when a user selects a visualization or one of its segments.

</td></tr><tr><td>

Action \[chartInteractionAction\]

</td><td>

Choose the event that occurs when a user clicks in a visualization or one of its segments. Choices depend on the visualization type and data source. Applies only when **Allow chart interaction** \[chartInteractionEnabled\] is true.-   **Go to data view** opens the records view or KPI Details relevant to the associated segment or visualization.

Usage Insights data sources redirect to the appropriate user, sessions, page, event pages that are based on corresponding usage data.

-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.

</td></tr></tbody>
</table>## Indicator scorecard component events

Select event handlers to configure the actions \(events\) provided with the Indicator scorecard component.

The Events tab shows the events used by the Indicator scorecard component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Indicator scorecard actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_my5_24l_4nb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indicator Clicked

</td><td>

The user selects and indicator. Redirects based on the Indicator sys\_id and Domain information. Suggested redirection is to the KPI Details component.Event handler: Link to Destination

 Suggested app route: KPI Details component

 Destination navigation field values: **uuid**=`@payload.indicatorSysid`, **domain**=`@payload.domain` from Data binding.

</td></tr></tbody>
</table>### Linking Indicator Clicked event to KPI Details component

To link the Report Visualization Clicked event in an Indicator scorecard component to a KPI Details component, follow these steps:

1.  Create a page using the legacy KPI Details template. Only copy the contents.
2.  Add the required and optional parameters to that page.
3.  In the Indicator Scorecard component, add a **Link to destination** event handler to the Indicator Clicked event.
4.  In the destination of the event handler, select an app route to the page that holds the KPI Details component.
5.  Configure the event handler properties.

|Parameters on page containing KPI Details|Value of corresponding Config fields on KPI Details|Link to Destination event handler properties|
|-----------------------------------------|---------------------------------------------------|--------------------------------------------|
|uuid \(required\)|@context.props.uuid|@payload.indicatorSysid|
|scoreDate \(optional\)|@context.props.scoreDate|@payload.scoreDate|
|breakdown \(optional\)|@context.props.breakdowns|@payload.breakdowns|
|domain \(optional\)|@context.props.domain|@payload.domain|

In the following image, the Link to Destination event handler for an Indicator Clicked event is configured to link to a page with the route ac\_kpi\_details, which contains a KPI Details component.

\[Omitted image "indicator-scorecard-event-handler-config.png"\] Alt text: Configuration of Link to destination event handler for an Indicator Overview component.

