---
title: Platform Analytics overview
description: Provides a role-specific, quick direct view of the Dashboards, Data Visualizations, Indicators, Filters, and Scheduled exports from the Platform Analytics library. Also provides a direct link to the Usage Insights page for the Platform Analytics library.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics experience, Platform Analytics]
---

# Platform Analytics overview

Provides a role-specific, quick direct view of the Dashboards, Data Visualizations, Indicators, Filters, and Scheduled exports from the Platform Analytics library. Also provides a direct link to the Usage Insights page for the Platform Analytics library.

To find Platform Analytics Overview, navigate to **All** &gt; **Platform Analytics** &gt; **Analytics Overview**.

## User roles applicable for Platform Analytics overview

Users with the following roles can access/create artifacts on the Platform Analytics overview page:

|Role|Dashboards|Data visualizations|Filters|Scheduled export|Indicators|
|----|----------|-------------------|-------|----------------|----------|
|platform\_analytics\_admin|Access enabled|Access enabled|Access enabled|Access enabled|Access enabled|
|pa-admin|Access enabled|Access enabled|Access enabled|Access enabled|Access enabled|
|dashboard\_admin|Access enabled|Access enabled|Access enabled|Access enabled|No access|
|viz\_admin|Access enabled|Access enabled|Access enabled|Access enabled|No access|
|par\_scheduler|Access enabled|Access enabled|No access|Access enabled|No access|
|report\_admin|Access enabled|Access enabled|Access enabled|Access enabled|No access|
|Users with all roles|Access enabled|Access enabled|Access enabled|Access enabled|Access enabled|

## Platform Analytics library navigation

Library pages like this one include a navigation pane that provides access to the other libraries and the Usage Insights page. Use it to navigate between the libraries without interrupting your workflow.

![Left navigation pane in PA library for analytics admin users](../../par-for-workspace/image/overview-left-nav-admin.png "Platform Analytics library navigation for analytics admin users")

**Note:** Users with non-admin roles \(roles other than analytics admin category\) can only access Dashboards, Data Visualizations, and Indicators in the left navigation pane. For more information on role-based access and enabled actions, see [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

![Left navigation pane in PA library for users with non-admin roles](../../par-for-workspace/image/overview-left-nav-non-admin.png "Platform Analytics library navigation for non-admin users")

## Platform Analytics overview elements

![Platform analytics overview page for analytics admin users](../../par-for-workspace/image/analytics-overview-admin.png "Platform Analytics overview for analytics admin users")

![Platform analytics overview page for users with non-admin roles](../../par-for-workspace/image/analytics-overview-non-admin.png "Platform analytics overview for non-admin users")

The following table shows the elements that users can view in the Analytics Overview page. Refer to the numbered call-outs in the image and their descriptions in the table.

<table id="table_avg_rs2_yhc"><thead><tr><th>

No

</th><th>

Field \(or\) Element Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

-   **Create Dashboard**
-   **Create Data Visualization**
-   **Create Filter**
-   **Create Scheduled Export**
-   **Create Indicator**

</td><td>

Button \(with drop-down options\)

</td><td>

-   Creates dashboard using Inline editor or Technical editor.
-   Creates data visualization using Visualization designer.
-   Creates filter.
-   Creates new scheduled export.
-   Creates indicator.

**Note:** This option is enabled only if the Performance analytics - premium \(com.snc.pa.premium\) plugin is installed.


</td></tr><tr><td>

2

</td><td>

**Search**

</td><td>

Search bar

</td><td>

Type name and search for any platform analytics artifact such as dashboard, data visualization, filter, or indicator across multiple libraries. The **Search** option uses AI search functionality if enabled in the instance, otherwise, uses Zing search functionality.

</td></tr><tr><td>

3

</td><td>

Data Collection Metrics for classic indicators

</td><td>

Single score filter

</td><td>

Consists of single score cards for the following data collection filters:-   Latest data collection jobs with errors
-   Latest data collection jobs with warnings
-   Latest data collection jobs running over 1 hour

**Note:** Users with pa\_admin, pa\_data\_collector, and pa\_power\_user roles can view the single scorecards related to job logs.

Users with dashboard\_admin role can only view scorecards related to dashboards.

Users with platform\_analytics\_admin can view all scorecards.

Users with viz\_admin and/or reports\_admin roles can’t view any scorecards.

</td></tr><tr><td>

4

</td><td>

Usage and performance metrics

</td><td>

Single score filter

</td><td>

Consists of single score cards for the following dashboards filters:-   Usage of recently created dashboards

**Note:** This value indicates the usage of the dashboards created by the user logged in currently.

-   Dashboards with load time less than 5 secs
-   Dashboards with load time greater than 5 secs

**Note:** You can view the data in this scorecard only if the Usage Insights \(glide.analytics.enabled property\) is enabled for your instance and if corresponding Usage Insights data is available.

Users with only dashboard\_admin and platform\_analytics\_admin roles can view these scorecards.

</td></tr><tr><td>

5

</td><td>

Quick access

</td><td>

List

</td><td>

-   Bookmarked: This tab lists the bookmarked Dashboards, Data Visualizations, and Indicators from the Usage Insights library.
-   Created by me: This tab lists the Dashboards, Data Visualizations, and Indicators you created in the Usage Insights library.
-   Certified: This tab lists the certified Dashboards, Data Visualizations, and Indicators from the Usage Insights library.

 **Note:** You can see Dashboards, Data Visualizations, and Indicators \(only in the Active state\) from both Core UI and Next Experience libraries listed in the same table.

</td></tr></tbody>
</table>