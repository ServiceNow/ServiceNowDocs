---
title: Report sources
description: Report sources are predefined data sets for creating reports.Create a custom set of data that you can use to create reports. In the Report Designer, report sources are called Data Sources.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report sources

Report sources are predefined data sets for creating reports.

Use report sources for reports containing the same conditions, so you do not have to define the conditions more than once. You can also use report sources to implement the same definitions across your organization.

In the Visualization Designer, your report sources are available when you filter a table on predefined conditions.

A report source always consists of a table and a number of conditions. When you create a new report, you can either use a report source or select a table. Some examples of report sources are open incidents, closed problems, and so on.

Creating report sources; using report data from fields in related tables; using related lists.

Use the option to create a report source based on the conditions of an existing report, or see the following steps for creating a source based on new conditions you add.

For more tips on using report sources, see [How to save time with Report Sources](https://community.servicenow.com/community?id=community_article&sys_id=2aed2beddbd377404819fb243996193f).

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

## Create a report source

Create a custom set of data that you can use to create reports.In the Report Designer, report sources are called Data Sources.

### Before you begin

Role required: report\_admin.

### About this task

If you update the conditions in a report source, these conditions are automatically propagated to all reports based on that report source.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Report Sources**.

    To create a report source from an existing report, open the report, and select `Save as data source` from the **Save** menu. The table and task conditions are populated in the report source record.

2.  Select **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_ayt_2b1_3r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the report source. For example, `Open incidents`

</td></tr><tr><td>

Table

</td><td>

The table on which the report source is based. For example, **Incident \[incident\]**.

</td></tr><tr><td>

Description

</td><td>

A more detailed description of what the report source does and its purpose.

</td></tr><tr><td>

Filter

</td><td>

Conditions for which table records to include in the report source. For example, to include open incidents, select **\[State\] \[is\] \[Active\]** for the Incident table.**Note:**

Sorting on data fields is accessible from within reports for some report types. For information on how to access, search for the **Add Sort** field description in a [Report types](../reference/report-types-creation-details-rd.md) topic for the report type to sort the data on.

-   If the report source is used for a report that includes OR conditions, only records that match both the report and the report source conditions are included.
-   If a report source specifies a [related list condition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-related-list-query.md), a report that is based on the report source ignores any additional related list conditions specified from within the report.
-   A report generates errors if it’s based on a report source that specifies a [related list condition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-related-list-query.md), and also includes additional related list conditions with dot-walk conditions.


</td></tr></tbody>
</table>4.  To view reports based on a report source, select the **Reports using this report source** related link in the report source record.

5.  Select **Submit**.


### What to do next

Use the report source to create a report.

**Note:** While a report source is used by active reports, you can’t delete it.

