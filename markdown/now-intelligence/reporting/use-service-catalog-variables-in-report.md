---
title: Use service catalog variables in a report
description: In reports on service catalog data, stack and group by variables, use variables as columns in list reports, and as columns and rows in multilevel pivot tables.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Report on service catalog variables, Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Use service catalog variables in a report

In reports on service catalog data, stack and group by variables, use variables as columns in list reports, and as columns and rows in multilevel pivot tables.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

Users with the report\_admin role can report on service catalog variables. Add the report\_admin role to the ACLs for the Options \[sc\_item\_option\], Variable Ownership \[sc\_item\_option\_mtom\], and Variables \[item\_option\_new\] tables.

**Note:**

-   The report you want to use the variable for must be based on the Requested Items table \[sc\_req\_item\] or the Catalog Task table \[sc\_task\]. Using other types of variables causes an error when generating the report.
-   The Oracle Database CLOB field does not have the functionality to retrieve the variables data in reports. For a column string field of less than 4000 bytes, you can change the column type to varchar2. To compare the CLOB columns of a smaller size, use the to\_char\(\) function. For a larger size CLOB, you must get a substring for comparison using the dbms\_lob.substr functions.

## About this task

For primary **Group by** and **Stack by**, these steps are intuitive.

![Service catalog variable use in Group by and Stack by fields.](../image/VariableGroupByStackBy.png "Variable use in Group by and Stack by fields")

**Note:** List, Box, Trendbox, and Pivot reports cannot use service catalog variables as a primary or secondary **Group by**. Single Score, Calendar, Control, and Map reports do not support **Group by** on any fields. List reports can use service catalog variables as columns.

Use a variable as an extra **Group by**, as a column in a list report, or as a column or row in a multilevel pivot table.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Create** and open the report to add the variable to.

2.  Do one of the following.

<table id="choicetable_p2g_2qf_v5"><tbody><tr><td id="d206574e123">

**Add as a column in a list report**

</td><td>

On the **Configure** tab, move **Variables+** to the **Selected** column.

</td></tr><tr><td id="d206574e141">

**Add as an extra __Group by__**

</td><td>

On the **Configure** tab, click **Additional group by**, then move **Variables+** at the bottom of the **Selected** of the **Additional group by** list.

</td></tr><tr><td id="d206574e168">

**Add as a column or row in a multilevel pivot table**

</td><td>

Click **Select columns** or **Select rows**, then select **Variables+** at the bottom of the list.**Note:**

-   If you first create the report with the variable as the main Group By first, it will always behave as an inner join.
-   If you first create the report with a regular field for primary grouping, and a secondary grouping on the variable, it will work as an outer join.


</td></tr></tbody>
</table>3.  Click the structure icon \(![Report structure icon](../image/Form_ShowReportStructureIcon.png)\) and then the plus sign that appears.

    A list of service catalog items appears.

4.  Select a catalog item with the variable.

    The variables for that item appear in the **Available** list.

5.  Move the variable that you want to use to the **Selected** column.

6.  **Save** the report.


**Parent Topic:**[Report on service catalog variables](../concept/rep-service-catalog-variables.md)

