---
title: View the Reports list
description: View a list of reports and create reports from the Reports list.You can show either all reports or only those reports marked as favorites. Reports can be marked favorite both automatically and manually.Report owners are not shown by default on the reports list, but you can add a column to show the user who created the report. Usually, the creator is the owner. The owner is also the person responsible for the process - the meaning of the data underlying the visualization.You can add parameters to the Reports list URL to filter the list before it loads.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# View the Reports list

View a list of reports and create reports from the Reports list.

Standard platform Access Control Lists \(ACLs\) govern access to reports in the reports list. For information about the ACLs used to control access to reports, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).

**Note:** On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience visualizations are found in the Platform Analytics library. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).

You can sort and filter the search results using the standard report list controls, by selecting tabs, column headings, or the favorites icon \(![Module star select](../image/ModuleStarSelect.png)\).

Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to open the Reports list. Select the gear icon \(![Gear icon](../../performance-analytics/image/Cogwheel.png)\) next to the **New** button to configure the columns displayed in the Reports list.

![Report list configuration window](../image/list-configuration.png "Reports list configuration window")

You can filter the Reports list with the following tabs:

|Tab|Description|
|---|-----------|
|My reports|Reports that you created.|
|Group|Reports that have been shared with you and with the groups that you are a member of.|
|Global|Reports that are available to everyone.|
|All|All reports that you have access to \(Global, Group, and My reports\).|

Select the star icon \(![Favorites icon.](../../../administer/user-exp-analytics/image/favorites-icon.png)\) to show only your Favorites in the Reports list. Select the X next to **Favorites filtering is on** to show all reports you are allowed to see.

![The reports list - only favorites shown](../image/view-create-list.png "View / Create report list")

If you have the report\_admin or admin roles, you also see these columns on the Reports list.

|Column|Description|
|------|-----------|
|Scheduled|Indicates that the report is scheduled to run in the future. You can schedule regular emailing of reports.|
|Published|If the report is published, this column shows a check mark \(![True](../image/True.png)\).|

**Parent Topic:**[Using reporting](../concept/c_GenerateReports.md)

## Viewing favorite reports

You can show either all reports or only those reports marked as favorites. Reports can be marked favorite both automatically and manually.

To toggle between showing only favorite reports and showing all reports, click the favorites icon \(![Module star select](../image/ModuleStarSelect.png)\) in the list header.

**Note:** Favorites filtering is persistent. If you chose to show only favorites the last time you viewed the Reports list, then only favorites are shown the next time. Click the favorites icon or the **Favorites filtering is on** button to show all reports you have the rights to view in the selected category. The **My reports** category is selected by default when you open the Reports list.

![Report favorites](../image/report-favorites-3.png "Report favorites")

A report is automatically marked as a favorite when you open it. You can manually mark a report as a favorite by clicking the star icon beside the report title.

To turn off the automatic marking of reports as favorites, disable the user preference glide.ui.nav.auto\_favorite. For more information, see [User preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UserPreferences.md) .

## View report owners

Report owners are not shown by default on the reports list, but you can add a column to show the user who created the report. Usually, the creator is the owner. The owner is also the person responsible for the process - the meaning of the data underlying the visualization.

### Before you begin

Role required: report\_admin

**Note:** On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select the Personalize List icon![](../../par-for-workspace/image/icon-personalize-list.png) to show the **Edit columns** option.

3.  Move **Created by** up the list so that it is visible.

    ![How to add the Created by column to a list of report visualizations](../image/show-report-created-by.png)

4.  Select **Apply**.


## Reports list URL parameters

You can add parameters to the Reports list URL to filter the list before it loads.

**Note:** On instances with Unified Analytics enabled, and on new Australia instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](../../performance-analytics/concept/explore-data-vis-library.md).

### Reports list URL structure

The URL structure is `https://<instance-name>.service-now.com/report_home.do?<parameter_name>=<parameter-value>`.

For example, the URL `https://yourbusiness.service-now.com/report_home.do?jvar_selected_tab=MyReports` returns the Reports list with the **My Reports** tab selected.

### Parameters

The following parameters are available for Reports list URLs:

<table id="table_zgq_w2h_1cb"><thead><tr><th>

Parameter

</th><th>

Possible values

</th></tr></thead><tbody><tr><td>

jvar\_selected\_tab

</td><td>

Shows the Reports list with the specified tab selected. Use these values:-   myReports
-   groupReports
-   globalReports
-   allReports

</td></tr><tr><td>

jvar\_search\_table

</td><td>

Filter reports created on a specified table. For example, the parameter `jvar_search_table=incident` shows only the reports created on the incident table.

</td></tr><tr><td>

jvar\_list\_order\_by

</td><td>

Sorts the list on one of these columns: -   type
-   title
-   table
-   modificationDate
-   scheduled
-   published
-   createdBy

 For example `https://yourbusiness.service-now.com/report_home.do?jvar_list_order_by=table` returns the list sorted by the source table of the report.

 **Note:** Use jvar\_list\_sort\_direction to specify ascending or descending order.

</td></tr><tr><td>

jvar\_list\_sort\_direction

</td><td>

Specifies the direction of the sort. -   asc — Sorts the list in ascending order
-   desc — Sorts the list in descending order

</td></tr><tr><td>

sysparm\_reportquery

</td><td>

Filters the reports with names that contain the specified value, for example: `sysparm_reportquery=Active` returns reports with the string `Active` in the title.

</td></tr><tr><td>

jvar\_search\_created\_by

</td><td>

the user who has created the report for example: `https://yourbusiness.service-now.com/report_home.do?jvar_selected_tab=allReports&jvar_search_created_by=itil` returns the reports created by the user with user name itil.

</td></tr><tr><td>

sysparm\_query

</td><td>

Enables you to filter on any condition in platform condition builder format. For example, `https://yourbusiness.service-now.com/report_home.do?sysparm_query=titleSTARTSWITHPRB&table!=incident`. For more information, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).

</td></tr></tbody>
</table>