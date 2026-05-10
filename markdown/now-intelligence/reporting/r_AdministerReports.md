---
title: Report Administration module
description: Learn how to administer reports on the ServiceNow platform using the Reports Administration module.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report Administration module

Learn how to administer reports on the ServiceNow platform using the **Reports** &gt; **Administration** module.

This module is not enabled by default, and must be activated. For a list of the reporting roles delivered with the ServiceNow platform, see [Reporting roles](reporting-roles.md#).

**Note:** Restricting a report by role restricts who can view a report. Users without the admin role cannot edit global reports. If a non-admin user edits a global report, saving that report creates a personalized version belonging to that user

Use the record list view to filter, view, or modify reports using any of the standard record list controls. Click **New** to create reports or select any of the records to display the report as a form. All the standard ServiceNow form controls apply.

You can select the table and field on which to report and the characteristics of the report format. Create a condition in the **Filter** field to further restrict the data that is presented in the report and select a role that can use the report.

## Report Security

The Report Security enforce access control checks plugin allows administrators to use access control list \(ACL\) rules to restrict report access. This functionality prevents unauthorized users from editing, updating, or deleting reports either through the UI or through a URL construct. See [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md) for more information.

## Available Report Fields

The following fields can be manipulated:

<table id="table_esh_ng2_s4"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Title

</td><td>

A unique and descriptive name for the report.

</td></tr><tr><td>

Table

</td><td>

The ServiceNow table against which this report is run.

</td></tr><tr><td>

Field Name

</td><td>

The name of the group-by field.

</td></tr><tr><td>

Type

</td><td>

The [report type](report-types-creation-details-rd.md) for this report.

</td></tr><tr><td>

Chart Size

</td><td>

Large, medium, or small.

</td></tr><tr><td>

Visible to

</td><td>

Select a group whose members are authorized to see the report. Select **Everyone** to give all your users access.

</td></tr><tr><td>

User

</td><td>

The user who can view the chart. Enter `GLOBAL` to make the report accessible to all.

</td></tr><tr><td>

Filter

</td><td>

The filter applied to the report data.

</td></tr><tr><td>

Roles

</td><td>

The roles required to view the report.

</td></tr><tr><td colspan="2">

If added to the form, the following fields are available

</td></tr><tr><td>

Aggregate

</td><td>

Determine how you want the data in the report aggregated. The default is **Count**, which displays the number of records selected. When you select **Average**, **Sum** or **Count Distinct**, you can select from a list of additional fields whose values you want to use to aggregate the data. Typical values to use as an average or a sum are the time measurements, such as **Business duration** \(expressed in days, hours, and minutes\) and **Resolve time** \(expressed in seconds\). Other fields, such as **Priority**, have numerical values associated with their levels and can be used as aggregators.**Note:** Averages are calculated by dividing the sum of all fields by the number of those fields that contain a value. Fields that are empty or that contain a light gray zero are not included in the field count that is used when dividing the sum.

</td></tr><tr><td>

Content

</td><td>

An HTML field for describing the content of the report. Not processed in the generation of the report.

</td></tr><tr><td>

Display grid

</td><td>

Select to display a table under the chart that contains a breakdown of the requested data. The aggregation units are **Count**, **Average**, **Sum**, or **Count Distinct**. The percentage of the total data represented by each discrete piece is displayed.

</td></tr><tr><td>

Group

</td><td>

Select a group whose members are authorized to see the report. select **Everyone** to give all your users access.

</td></tr><tr><td>

Interval

</td><td>

For [Trend](../concept/c_CreateTrendCharts.md#) or [Trendbox](../concept/c_CreatingTrendboxCharts.md#) charts, the interval of time to measure along.

</td></tr><tr><td>

No Groups

</td><td>

Use the values in this list to limit the number of bars that appear in the chart. The platform displays 12 bars by default, from high values to low values and puts the remaining data into an **Other** category. You can select to display 10, 12, 15, 20, or all bars.

</td></tr><tr><td>

Others

</td><td>

Check box to include the **Other** group in the report.

</td></tr><tr><td>

Select fields for list

</td><td>

The fields that display in a list report.

</td></tr><tr><td>

Select fields for orderBy

</td><td>

The order of fields that display in the report.

</td></tr><tr><td>

Show Empty

</td><td>

Whether to display empty categories.

</td></tr><tr><td>

Sumfield

</td><td>

The field to perform a sum on for [Trend](../concept/c_CreateTrendCharts.md#) or [Trendbox](../concept/c_CreatingTrendboxCharts.md#) Charts.

</td></tr><tr><td>

Trend Field

</td><td>

The field to track over time for [Trend](../concept/c_CreateTrendCharts.md#) or [Trendbox](../concept/c_CreatingTrendboxCharts.md#) Charts.

</td></tr></tbody>
</table>**Parent Topic:**[Administering reports](../concept/c_AdminsteringReports.md)

