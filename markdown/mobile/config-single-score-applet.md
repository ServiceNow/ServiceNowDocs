---
title: Create a chart screen for a data visualization
description: Configure a chart screen to give your users access to pre-configured mobile dashboard views for several types of data visualizations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Chart screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a chart screen for a data visualization

Configure a chart screen to give your users access to pre-configured mobile dashboard views for several types of data visualizations.

## Before you begin

Role required: admin or delegated developer

You must have an existing data visualization to display on your screen. If you haven’t yet configured a data visualization, see the following documentation topics: [Platform Analytics overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center.md) and [Data visualizations in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-data-visualizations.md).

In addition, you also need a mobile analytics preview contained within a mobile dashboard preview. For more information, see [Create a mobile analytics preview](sg-mobile-dashboard-preview.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select **New**.

4.  Select the **Chart** option in the Create a screen page, and then select **Continue**.

5.  Complete the following fields as needed.

<table id="table_mll_r4w_4wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

Name for the chart screen. This name is displayed as the screen header and the name of the screen in the UI section.

</td></tr><tr><td>

Description

</td><td>

Additional information about the screen.

</td></tr><tr><td>

Hide screen name

</td><td>

Determines if the screen name should be shown as the screen header. Hiding is useful if, for example, the text already appears in the header name or if it doesn't provide any value to the user.

</td></tr><tr><td>

Enable tooltip

</td><td>

Enables tooltips on each chart element.

</td></tr><tr><td>

Type

</td><td>

Determine your chart screen type. Select Data visualization.

**Note:**

From the Washington DC version, to work with Data Visualization charts and Data Visualization single score section types, you must select the Data Visualization option.

For versions before the Washington DC version, you can still use the charts and reports previously created. However, these options are set to be replaced by data visualizations.

</td></tr><tr><td>

Data Visualization

</td><td>

The data visualization to display in the chart screen. Select Data visualization from the list.

</td></tr><tr><td>

Report

</td><td>

The report to display in the chart screen. Select a report from the list.

 This field is only visible when **Type** is set to **Report**.

**Note:** This option is set to be replaced by data visualizations.

</td></tr><tr><td>

PA Widget

</td><td>

Select the PA Widget to display in the chart screen. This list is automatically filtered for latest score reports on your instance.

 This field is only visible when **Type** is set to **Performance Analytics \(PA\)**.

**Note:** This option is set to be replaced by data visualizations.

</td></tr><tr><td>

Icon

</td><td>

Icon used to represent your mobile chart screen when added to a launcher screen.

</td></tr><tr><td>

Chart header function instances

</td><td>

Creates a function instance that resides in the upper-right corner of your chart header.

</td></tr><tr><td>

Role access

</td><td>

Determine which user roles can access this screen. If you don’t select any roles, users with any role will have access to the screen.

</td></tr></tbody>
</table>6.  Select Data visualization from the **Type** field.

7.  From the **The Data Visualization** field, select the data visualization to display in the chart field.

8.  Select **Save**.


## What to do next

Configure a navigation function to direct your users from an analytics preview to your chart screen. For details on this process, see [Create a navigation function to a chart screen](config-chart-nav.md).

