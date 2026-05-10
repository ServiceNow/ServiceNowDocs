---
title: Create a mobile analytics preview
description: Use a mobile analytic preview within a mobile dashboard to display data visualizations on your launcher screen pages.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile dashboard preview, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a mobile analytics preview

Use a mobile analytic preview within a mobile dashboard to display data visualizations on your launcher screen pages.

## Before you begin

Role required: admin

To display a data visualization in a launcher screen you need a chart or single score report. For information about creating data visualizations, see [Platform Analytics overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center.md) and [Data visualizations in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-data-visualizations.md).

For details about data visualization settings and configurations that are available for display in the mobile platform, see [Data visualization fields available for display in mobile](../reference/data-visualization-mobile-fields.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Analytics preview \[sys\_sg\_chart\]**, and then select **New**.

5.  On the form, fill in the fields.

<table id="table_cbg_pzm_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

The name for your analytics preview.

</td></tr><tr><td>

Title

</td><td>

The title that appears at the top of your analytics preview in the mobile device screen.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Type

</td><td>

Determine your preview type. Select Data Visualization.**Note:** From the Washington DC version, to work with Data Visualization charts and Data Visualization single score section types, you must select the Data Visualization option.

For versions before the Washington DC version, you can still use the charts and reports created. However, these options are set to be replaced by data visualizations.

</td></tr><tr><td>

Data Visualization

</td><td>

Data visualization to be displayed in your chart preview.Click the arrow to display a list of all data visualizations hosted on the instance. If you select a data visualization not supported for mobile, when you open the launcher screen, a message displays which states that the content can't be shown.

For more information, see [Data visualizations in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-data-visualizations.md). For information about the data displayed in data visualizations for mobile devices, see [Data visualization fields available for display in mobile](../reference/data-visualization-mobile-fields.md).

</td></tr><tr><td>

Report

</td><td>

Report to be displayed in your preview. This field appears only when the **Type** field is set to **Report**.Click the arrow to display a list of all reports hosted on the instance. If you select a report not supported for mobile, when you open the launcher screen, a message is displayed which states that the content can't be shown.

 **Note:** This option is set to be replaced by data visualizations.

</td></tr><tr><td>

PA Widget

</td><td>

Performance Analytics widget to be displayed in your chart preview. This field appears only when **Performance Analytics \(PA\)** is selected from the **Type** field.Click the arrow to display a list of all widgets hosted on the instance. If you select a Performance Analytics widget not supported for mobile, when you open the launcher screen, a message displays which states that the content can't be shown.

**Note:** This option is set to be replaced by data visualizations.

</td></tr><tr><td>

Destination screen navigation

</td><td>

Select **Choose** to select an existing navigation type function to use when a user taps the chart preview or select **New** to create a navigation function. For more information, see [Navigation functions](../concept/mobile-nav-functions.md).

</td></tr></tbody>
</table>6.  Select Data visualization in the **Type** field.

7.  From the **Data Visualization** field, select the data visualization to be displayed in your chart preview.

8.  From the Destination screen navigation field, select **Choose** to select an existing navigation type function to use when a user taps the chart preview.

    Alternatively, select **New** to create a navigation function.

9.  Select **Save**.


## What to do next

After creating a mobile analytics dashboard preview, you need to create a data visualization chart screen. For more information, see [Create a chart screen for a data visualization](config-single-score-applet.md).

