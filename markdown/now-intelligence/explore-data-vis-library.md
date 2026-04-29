---
title: Exploring the Data Visualizations library
description: Find any data visualization in the Platform Analytics Data Visualizations library so that you can share information about your data with stakeholders and other users to evaluate the trends with real-time data. With the appropriate role, you can also create a visualization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Exploring the Data Visualizations library

Find any data visualization in the Platform Analytics Data Visualizations library so that you can share information about your data with stakeholders and other users to evaluate the trends with real-time data. With the appropriate role, you can also create a visualization.

## Data Visualizations Library overview

On Australia instances, you can find both Core UI reports and Platform Analytics experience data visualizations in the Data Visualizations library.

When you edit Core UI dashboards and their content, you do so in the Core UI tools including Report Designer. For more information, see [Reporting, dashboards, and Performance Analytics in the Core UI](../../reporting/concept/classic-vis-overview.md) and [Using reporting](../../reporting/concept/c_GenerateReports.md).

To open the data visualizations library, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. You can also navigate to this library from other Platform Analytics library pages.

Library pages like this one include a navigation pane that provides access to the other libraries and the Usage Insights page. Use it to navigate between the libraries without interrupting your workflow.

## Data Visualizations library elements

Access to certain elements in the Data Visualizations library is based on whether the user is associated with specific admin roles. For Data Visualizations, the analytics admin roles include report\_admin, pa\_admin, platform\_analytics\_admin, and admin. The lowest required role is viz\_admin. For users with the lowest role, the application navigator provides a direct access only to the [Dashboards](../../dashboards/concept/find-dashboard-library.md), [Data Visualizations](explore-data-vis-library.md), and [Indicators](your-kpis.md) from the Platform Analytics library. For more information on user roles in Data Visualizations, see [Data visualization roles](../../par-for-workspace/reference/platform-analytics-roles.md#table_c3f_kwc_k2c).

The following image shows the Data Visualizations library elements that are accessible for users with analytics admin roles.

![Data Visualizations library for analytics admin roles.](../../par-for-workspace/image/analytics-center-data-vis-tab.png "Platform Analytics Data Visualizations library features for users with analytics admin roles")

The following example shows the Data Visualizations library elements that are accessible for users with lower roles.

![Data Visualizations library for users with lower roles.](../../par-for-workspace/image/ac-data-vis-tab-non-admin.png "Platform Analytics Data Visualizations library features for users with lower roles")

The following table lists the Data Visualizations library elements. Refer to the numbered call-outs in the image and their descriptions in the table.

<table id="table_c2j_gs3_vfc"><thead><tr><th>

No.

</th><th>

Field \(or\) Element name

</th><th>

Accessible to users with roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

**Create data visualization**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin
-   viz\_creator

</td><td>

Option to create data visualizations.

</td></tr><tr><td>

2

</td><td>

**Filter by**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Option for filtering the data visualizations list to display the data based on the following predefined conditions:-   **Bookmarked**: Your bookmarked visualizations. Bookmark any data visualization that you have access to so that you can find it easily. To bookmark a visualization, see [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md).
-   **Certified**: Visualizations that an administrator has certified. To certify a data visualization, see [Certify a data visualization in the Visualization Designer](../../dashboards/task/certify-dv-ac.md).
-   **Owned by me**: Visualizations that you own or you created.
-   **Shared with me**: Visualizations that have been shared with you as a user, member of a group, or role. To share a data visualization, see [Share a data visualization in the Visualization Designer](../../reporting/task/share-dv-ac.md#).

</td></tr><tr><td>

3

</td><td>

**Single scores**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin

</td><td>

Data visualization scores. These scores highlight the key data visualization statistics that are based on the following filter conditions:-   Not used in any dashboard
-   Not viewed in 1 year
-   Not viewed in the last 6 months
-   Deactivated for more than 3 months
-   Updated in the last 30 days

Select a score to filter and display the dashboards that match the condition.

</td></tr><tr><td>

4

</td><td>

**Search**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Search box with a list filter to filter the list of data visualizations by name or description. For example, by searching the word Data, you can see the list of visualizations that contain Data in the Name or Description columns.

</td></tr><tr><td>

5

</td><td>

**Filter list** condition builder

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Launches the condition builder for the Data Visualizations library.

</td></tr><tr><td>

6

</td><td>

**Personalize List**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Option to add or remove columns in the data visualizations list \(![](../../par-for-workspace/image/icon-personalize-list.png)\).

</td></tr><tr><td>

7

</td><td>

**Delete**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Option to delete the selected data visualizations.

</td></tr><tr><td>

8

</td><td>

**Deactivate/Activate**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin

</td><td>

Option to deactivate or activate the selected data visualizations .

</td></tr><tr><td>

9

</td><td>

**Show/Hide labels**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Option to show or hide labels for the fields **Field** and **Operator** in the condition builder.**Note:** The **Show/Hide labels** option is visible only on selecting the **Condition Filter icon**.

</td></tr><tr><td>

10

</td><td>

**Saved filters**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Option to save the current condition filters that are set using the condition builder. You can select the visibility of the filter.

 ![Save the current condition set](../../par-for-workspace/image/analytics-center-saved-filters.png)

 **Note:** The **Saved filters** option is visible only on selecting the **Condition Filter icon**.

</td></tr><tr><td>

11

</td><td>

**Condition builder**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Build condition set to filter data visualizations in the library.**Note:** The **Condition builder** option is visible only on selecting the **Condition Filter icon**.

</td></tr><tr><td>

12

</td><td>

**Column Filter**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Option for displaying the column filters in the data visualizations to filter the data in the columns based on the specified condition. By default, the **Column Filter** is turned off.

</td></tr><tr><td>

13

</td><td>

**Data visualization List**

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

List of all data visualizations. You can personalize and also sort the list by Name, Description, Views, and Certified.

</td></tr><tr><td>

14

</td><td>

Application navigator

</td><td>

-   report\_admin
-   pa\_admin
-   platform\_analytics\_admin
-   admin
-   viz\_admin

</td><td>

Provides direct access to the [Dashboards](../../dashboards/concept/find-dashboard-library.md), [Data Visualizations](explore-data-vis-library.md), [Indicators](your-kpis.md), [Filters](../../par-for-workspace/concept/interactive-filters-workspace.md), and [Scheduled exports](../../par-for-workspace/task/schedule-visn-export-vd.md) from the Platform Analytics library and the Usage Insights page.**Note:** Users with non-admin roles can only access Dashboards, Data Visualizations, and Indicators from the Platform Analytics library using the application navigator.

</td></tr></tbody>
</table>**Note:** A user with the viz\_admin role or higher might also see a panel with recommendations about problematic data visualizations. For more information, see [Platform Analytics library recommendations](../../par-for-workspace/concept/pa-library-recommendations.md).

