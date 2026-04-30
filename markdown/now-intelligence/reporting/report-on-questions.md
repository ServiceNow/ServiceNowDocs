---
title: Report on questions
description: Report on selected questions by grouping or filtering on them.You can create reports grouped or stacked by questions, as well as create filters on the same questions. For example, you can create a report that shows customer responses of their reasons for requesting help, or descriptions of their issues.Create reports additionally grouped by selected questions. You can also create filters on the same questions. For example, you can create a report that shows customer responses of their reasons for requesting help, or descriptions of their issues.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report on questions

Report on selected questions by grouping or filtering on them.

Creating reports grouped by questions is helpful to:

-   Determine whether questions that customers ask are getting answered.
-   Gain more information from customers during the request process.

To use questions in a report, the data source or non-service catalog table must have questions associated with it. You can group or filter by questions from a table extended from the Task \[task\] table, for example the \[incident\] or \[problem\] tables.

You can use questions in conditions you apply to the data source. You can also use questions in the following fields:

-   Group by
-   Stack by
-   Additional group by
-   Select columns
-   Select rows

**Note:**

If there is a Record Producer associated with the table, variables defined in that Record Producer are available as Questions in the condition builder for filtering the data source, except for the following question types:

-   Label
-   Rich text label
-   Macro
-   Container

You cannot group by Record Producer variables. For more information, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Advanced Core UI reporting topics](c_AdvancedReporting.md)

## Group or stack a report by questions

You can create reports grouped or stacked by questions, as well as create filters on the same questions. For example, you can create a report that shows customer responses of their reasons for requesting help, or descriptions of their issues.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### About this task

You can apply these steps to any report type as long as the report source has questions associated with it. If the report source does not have questions, the **Questions** option does not display in the **Group by** and **Stack by** fields.

**Note:** List, Box, Trendbox, and Pivot reports cannot use questions as a primary or secondary **Group by**. Single Score, Calendar, Control, Histogram, and Map reports do not support **Group by** on any fields. List reports can use questions as columns. Multilevel Pivot reports can use questions as columns and rows.

### Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select a report source that has questions associated with it and click **Next**.

4.  On the **Type** tab, select the report type and click **Next**.

5.  On the **Configure** tab, select **Questions** from the **Group by** or **Stack by** filters.

    ![Configure tab > group by or stack by questions](../image/group-by-questions.png)

6.  Search for and select questions associated with the category to group or stack by.

7.  Continue to configure and style the report according to its report type.

    See [Report types](../reference/report-types-creation-details-rd.md).


## Add additional group by questions to a report

Create reports additionally grouped by selected questions. You can also create filters on the same questions. For example, you can create a report that shows customer responses of their reasons for requesting help, or descriptions of their issues.

### Before you begin

Roles required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### About this task

You can apply these steps to any report type as long as the report source has questions associated with it. If the report source does not have questions, the **Questions** option does not display in the **Additional group by** filter.

### Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select a report source that has questions associated with it and click **Next**.

4.  On the **Type** tab, select the report type and click **Next**.

5.  On the **Configure** tab, select a **Group by** filter.

6.  Click **Additional group by**.

7.  Select **Questions \[+\]** and click the structure icon \(![](../image/Form_ShowReportStructureIcon.png)\) to choose an item.

    ![Additional group by slushbucket](../image/additional-group-by-question.png)

8.  Select a question category.

    The variable questions associated with the category appear in the **Additional group by** window.![Additional group by questions](../image/additional-group-by-selected-questions.png)

9.  Add the desired questions to the **Selected** column and click **OK**.

10. Continue to configure and style the report according to its report type.

    See [Creating reports](../reference/report-types-creation-details-rd.md).


