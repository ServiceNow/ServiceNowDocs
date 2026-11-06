---
title: Exploring the Data Visualizations library
description: Find any data visualization in the Platform Analytics Data Visualizations library. You can share information about your data with stakeholders and other users to evaluate the trends with real-time data. With the appropriate role, you can also create a visualization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/explore-data-vis-library.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Exploring the Data Visualizations library

Find any data visualization in the Platform Analytics Data Visualizations library. You can share information about your data with stakeholders and other users to evaluate the trends with real-time data. With the appropriate role, you can also create a visualization.

## Data Visualizations Library overview

On Brazil instances, you can find both Core UI reports and Platform Analytics experience data visualizations in the Data Visualizations library.

When you edit Core UI dashboards and their content, you do so in the Core UI tools including Report Designer. For more information, see [Reporting, dashboards, and Performance Analytics in the Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/performance-analytics/classic-vis-overview.md) and [Using Core UI reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/reporting/c_GenerateReports.md).

To open the data visualizations library, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. You can also navigate to this library from other Platform Analytics library pages.

Library pages like this one include a navigation pane that provides access to the other libraries and the Usage Insights page. Use it to navigate between the libraries without interrupting your workflow.

## Data Visualizations library elements

Access to certain elements in the Data Visualizations library is based on whether the user is associated with specific admin roles. For Data Visualizations, the analytics admin roles include report\_admin, pa\_admin, platform\_analytics\_admin, and admin. The lowest required role is viz\_admin. For users with the lowest role, the application navigator provides a direct access only to the [Dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/find-dashboard-library.md), [Data Visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/explore-data-vis-library.md), and [Indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/your-kpis.md) from the Platform Analytics library. For more information on user roles in Data Visualizations, see [Data visualization roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/platform-analytics-roles.md).

The following image shows the Data Visualizations library elements that are accessible for users with the viz\_admin role or higher. \(The **Create data visualization** button requires only viz\_creator or higher.\)

\[Omitted image "analytics-center-data-vis-tab.png"\] Alt text: Data Visualizations library for analytics admin roles.

The following example shows the Data Visualizations library elements that are accessible for users with any role.

\[Omitted image "ac-data-vis-tab-non-admin.png"\] Alt text: Data Visualizations library for users with lower roles.

The following table lists the Data Visualizations library elements. Refer to the numbered call-outs in the image and their descriptions in the table.

<table id="table_c2j_gs3_vfc"><thead><tr><th>

Number

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

viz\_creator or higher

</td><td>

Option to create data visualizations.

</td></tr><tr><td>

2

</td><td>

**Filter by**

</td><td>

Any

</td><td>

Option for filtering the data visualizations list to display the data based on the following predefined conditions:-   **Bookmarked**: Your bookmarked visualizations. Bookmark any data visualization that you have access to so that you can find it easily. To bookmark a visualization, see [Bookmark a visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/bookmark-dv-ac.md).
-   **Certified**: Visualizations that an administrator has certified. To certify a data visualization, see [Certify a data visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/certify-dv-ac.md).
-   **Owned by me**: Visualizations that you own or you created.
-   **Shared with me**: Visualizations that have been shared with you as a user, member of a group, or role. To share a data visualization, see [Share a data visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/share-dv-ac.md).

</td></tr><tr><td>

3

</td><td>

**Single scores**

</td><td>

viz\_admin or higher

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

Any

</td><td>

Search box with a list filter to filter the list of data visualizations by name or description. For example, by searching the word Data, you can see the list of visualizations that contain Data in the Name or Description columns.

</td></tr><tr><td>

5

</td><td>

**Filter list** condition builder

</td><td>

Any

</td><td>

Launches the condition builder for the Data Visualizations library. See [Data visualization library filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/explore-data-vis-library.md).

</td></tr><tr><td>

6

</td><td>

**Personalize List**

</td><td>

Any

</td><td>

Option to add or remove columns in the data visualizations list \(\[Omitted image "icon-personalize-list.png"\] Alt text:\).

</td></tr><tr><td>

7

</td><td>

**Delete**

</td><td>

viz\_admin or higher

</td><td>

Option to delete the selected data visualizations.

</td></tr><tr><td>

8

</td><td>

**Deactivate/Activate**

</td><td>

viz\_admin or higher

</td><td>

Option to deactivate or activate the selected data visualizations .

</td></tr><tr><td>

9

</td><td>

**Show column filter row**

</td><td>

viz\_admin or higher

</td><td>

Option for displaying the row of column filters \(12\) in the data visualizations to filter the data in the columns based on the specified condition. By default, the **Column Filter** is turned off.

</td></tr><tr><td>

10

</td><td>

**Select all**

</td><td>

viz\_admin or higher

</td><td>

Select this box to select all data visualizations currently visible. You can then delete, activate, or deactivate all these data visualizations.Alternatively, you can select or deselect individual data visualizations at the beginning of each row.

</td></tr><tr><td>

11

</td><td>

Sortable column names

</td><td>

Any

</td><td>

All columns can be sorted on the column name, either alphabetically or by date.

</td></tr><tr><td>

12

</td><td>

Column filters

</td><td>

Any

</td><td>

Hidden or shown by **Show column filter row** \(9\). Lets you filter each column by value or date. For more information, see [Column filters in the Data visualization library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/column-filters-data-viz-library.md).

</td></tr></tbody>
</table>**Note:** A user with the viz\_admin role or higher might also see a panel with recommendations about problematic data visualizations. For more information, see [Platform Analytics library recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/pa-library-recommendations.md).

## Data visualization library filter

The funnel button opens a filter on the library list.

\[Omitted image "dv-library-filter.png"\] Alt text: Opened filter section on Data visualization library.

<table id="table_tkb_bzz_wkc"><thead><tr><th>

Number

</th><th>

Field \(or\) Element name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

**Show/Hide labels**

</td><td>

Option to show or hide labels for the fields **Field** and **Operator** in the condition builder.

</td></tr><tr><td>

2

</td><td>

**Saved filters**

</td><td>

Option to save the current condition filters that are set using the condition builder. You can select who can see the filter. The choices available depend on your role.

 \[Omitted image "analytics-center-saved-filters.png"\] Alt text: Save the current condition set

</td></tr><tr><td>

3

</td><td>

**Condition builder**

</td><td>

Build condition set to filter data visualizations in the library. You can dot-walk reference fields.

</td></tr></tbody>
</table>