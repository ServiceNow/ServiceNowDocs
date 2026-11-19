---
title: User Experience Analytics funnel component setup
description: The Usage Insights funnel lets you review the performance of your conversation flows through cumulative filtering. This component lets you put the same funnel functionality on a UI Builder page that you have in the Usage Insights dashboard.Select the Usage Insights data source and the details of the steps to show in the funnel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/user-experience-analytics-funnel-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# User Experience Analytics funnel component setup

The Usage Insights funnel lets you review the performance of your conversation flows through cumulative filtering. This component lets you put the same funnel functionality on a UI Builder page that you have in the Usage Insights dashboard.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for  that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Usage Insights funnel component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "uxa-funnel-config-panel.png"\] Alt text: Config panel for User Experience Analytics funnel component.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## User Experience Analytics funnel component properties

Select the Usage Insights data source and the details of the steps to show in the funnel.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="id_rmw_jbq_frb"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show header \[showHeader\]

</td><td id="entry_show-header">

The visualization header, including title and icons.

</td></tr><tr><td>

Show header separator \[showHeaderSeparator\]

</td><td id="entry_show-header-separator">

Option to display a line separating the header from the rest of the component.

</td></tr><tr><td>

Chart title \[headerTitle\]

</td><td id="entry_chart-title">

Title of the visualization.

</td></tr><tr><td>

Description \[description\]

</td><td id="entry_description">

A short overview about the visualization that the end user sees. Descriptions help users find the visualization.

</td></tr><tr><td>

Wrap title \[wrapTitle\]

</td><td id="entry_wrap-title">

Option to wrap long titles onto a second line. If false, displays an ellipsis to truncate long titles.

</td></tr><tr><td>

Show border \[showBorder\]

</td><td id="entry_show-border">

Option to display a line around the component.

</td></tr><tr><td>

Show refresh option

</td><td id="entry_show-refresh-option">

Option to show or hide the refresh option from data visualizations. If cache is enabled on a dashboard, the Refresh option is hidden.

</td></tr><tr><td>

Bare \[bareBorder\]

</td><td id="entry_bare">

Option to remove padding around data visualization to provide more compact positioning on the page. Only available when **Show border** is turned off.

</td></tr></tbody>
</table><table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data sources\[funnelSelectionConfig\]

</td><td>

A JSON array of the Usage Insights application and the funnel. You have a link also to create a new funnel.

</td></tr><tr id="date-range-heading"><td class="sub-head" colspan="2">

Date range \[dateRangeConfig\]

</td></tr><tr id="set-absolute-period"><td>

Set absolute period

</td><td id="entry_set-abs-period">

Option to set absolute start and end date.

</td></tr><tr id="period-start"><td>

\(first time field, untitled\)

</td><td id="entry_period-start">

Start date for the absolute period.This property applies only when **Set absolute period** is true.

</td></tr><tr id="period-end"><td>

\(second time field, untitled\)

</td><td id="entry_period-end">

End date for the absolute period.This property applies only when **Set absolute period** is true.

</td></tr><tr id="number-of-periods"><td>

Number of periods

</td><td id="entry_number-periods">

Number of date periods to display. This property applies only when **Set absolute period** is true.

</td></tr><tr id="period"><td>

Period

</td><td id="entry_period-interval">

Time interval for each date period. -   Days `D`
-   Months `M`
-   Years `Y`

 This property applies only when **Set absolute period** is false.

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show conversion time\[showConversionTime\]

</td><td>

Show the conversion time between each pair of steps in the funnel.Default: true

</td></tr><tr><td>

Show conversion percentage\[showConversionPercentage\]

</td><td>

Show the percentage of users who have completed the preceding step.Default: true

</td></tr><tr><td>

Show converted users\[showConvertedUsers\]

</td><td>

Show the number of converted users.Default: true

</td></tr><tr><td>

Show funnel chart\[showFunnelChart\]

</td><td>

Show the data visualization as well as the caption.Default: true

</td></tr><tr><td>

Show step name\[showStageName\]

</td><td>

Show the names of each step in the funnel report.Default: true

</td></tr></tbody>
</table>