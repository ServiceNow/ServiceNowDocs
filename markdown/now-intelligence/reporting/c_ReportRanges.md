---
title: Report ranges
description: Use a report range to define data intervals that are used in bar, donut, and pie charts in Platform Analytics data visualizations and Core UI reports.Report ranges work with elements that hold only dates, lists, or integers.To view all currently configured report ranges, navigate to Reports Administration Report Ranges or Platform Analytics Administration Color Settings Report Ranges .Create a report range to define data intervals that are used in bar, donut, and pie charts in reports and data visualizations.To use report ranges in your bar and pie charts, you must enable the report range module.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report ranges

Use a report range to define data intervals that are used in bar, donut, and pie charts in Platform Analytics data visualizations and Core UI reports.

Sometimes it can be helpful to group results into ranges or buckets rather than viewing every result as an individual score. Think of a bar or pie chart which shows the date of creation of incidents. By default, each individual value would be a separate data point, creating an unnecessarily crowded-looking visual. However, segmenting the results into logical groups of dates can add context and help the audience understand which ranges are good, bad, or concerning.

Example use case: There is a significant cost involved to a business each time a SLA is breached at a company. A Service Manager can see how many tasks were completed well within the SLA versus how many elapsed during the SLA. This information helps them identify which SLAs may need to be adjusted.

**Note:** Reports only show historical data. It is not possible to set report ranges for dates in the future.

![Vertical bar report with configured report ranges highlighted](../image/IncidentsCreatedDateWRanges06032013.png "Incidents created date with ranges")

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

## How report ranges work

Report ranges work with elements that hold only dates, lists, or integers.

|Type|Examples|
|----|--------|
|Dates|Using the Created field in the Incident table: Same Day, 2 Days, 2–5 Days, 5–7 Days, 1–2 Weeks, 2–4 Weeks, 1–2 Months, &gt; 2 Months|
|Lists|Using the Priority field in the Incident table: Low, Moderate, High, Critical, Planning|
|Integers|Using the Count field in the Incident table: Overloaded, Optimized, Under Utilized|

Report ranges can be globally applied to all date type fields \(date, due date, duration, date/time, date time\), or you can limit report ranges to a specific table.

## View all report ranges

To view all currently configured report ranges, navigate to **Reports** &gt; **Administration** &gt; **Report Ranges** or **Platform Analytics Administration** &gt; **Color Settings** &gt; **Report Ranges**.

![](../image/ReportRangesK-L.png "Report ranges list")

The following are important columns and their associated data types:

|Field|Corresponding data type|
|-----|-----------------------|
|Upper value duration|Date - works with elements that store dates.|
|Upper value int|Integer - works with elements that store numbers.|
|Value list|List - works with elements that store a list item.|

## Create a report range

Create a report range to define data intervals that are used in bar, donut, and pie charts in reports and data visualizations.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Report Ranges**.

    If you have fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Color Settings** &gt; **Report Ranges**.

2.  Select **New**.

3.  Fill in the form \(see table\):

    ![New report ranges form](../image/NewReportRangesFormFuji.png)

    Use the following fields to refine the data displayed in the report and to design the appearance of your report visualization:

<table id="table_uxv_g2c_zp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="drrName"><td>

Name

</td><td>

The name of the table to draw the values from. **Note:** This field is required before you can select from the **Element** list.

</td></tr><tr id="drrElement"><td>

Element

</td><td>

The table field to draw the values from.

</td></tr><tr id="drrLabel"><td>

Label

</td><td>

The name for the report range that is displayed in reports.

</td></tr><tr id="drrValList"><td>

Value list

</td><td>

For list elements, this field defines which values are within the range. After the range is saved, the value list is populated with the choices of the element.

</td></tr><tr id="drrColName"><td>

Color name

</td><td>

The color from the Color Definitions table to display this report range in. The color appears in the **Display** field. If you enter a color name, you do not need to enter a color value.

**Note:** When creating reports, colors may not display as specified for ranges on Group by report fields selected via dot-walking. For this feature to work appropriately, select applicable Group by fields from the base table only.

</td></tr><tr id="drrUVI"><td>

Upper value int

</td><td>

For integer-type elements, this field defines the upper limit of the range. The upper value of the report range with nearest lower **Order** defines the lower limit of this range. If no range with a lower **Order** exists, the lower limit is zero.

 Example: One report range has an upper limit of 10 and an **Order** of 20. A second report range has an upper limit of 5 and the **Order** of 19. The first report shows values from 6 to 10 in the formatting specified by this range. The second report shows values of 5 or less.

</td></tr><tr id="drrUVD"><td id="UVD">

Upper value duration

</td><td>

For duration-type elements, this field defines the upper limit of the range. The upper value of the report range with nearest lower **Order** defines the lower limit of this range. If no range with a lower **Order** exists, the lower limit is zero.

 Example: One report range has an upper limit of 10 and an **Order** of 20. A second report range has an upper limit of 5 and the **Order** of 19. Values from 5 to 10 display the formatting specified by this range.

</td></tr><tr id="drrDisplay"><td>

Display

</td><td>

Read-only. Shows the color that is used for the specific report range.

</td></tr><tr id="drrOrder"><td>

Order

</td><td>

The order in which the report ranges are used. If a value is defined within more than one label, it is reported under the report range with the lowest order.

</td></tr></tbody>
</table>    **Note:** Once configured, a report range will show as empty if there's no data available in your report. Context fields such as data labels or legend related to the configured report range will still show and be highlighted.


## Enable the report range module

To use report ranges in your bar and pie charts, you must enable the report range module.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Menus**.

2.  Open the **Reports** application menu.

3.  In the **Modules** related list, enable the Report Ranges module.![Application menu form showing the Modules related list and the Report Ranges module highlighted.](../image/rep-range-mod.png)

    The Modules related list may have over 100 entries. Filter it on the word range to shorten your search.


### Result

You can define report ranges for your pie and bar charts.

