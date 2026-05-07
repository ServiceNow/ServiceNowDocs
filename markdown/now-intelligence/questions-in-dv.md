---
title: Questions in data visualizations
description: You can group or filter table data in data visualizations by questions. The table must support questions.In visualizations of data from the Task \[task\] hierarchy of tables, you can use questions defined for the table to filter or group the data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Questions in data visualizations

You can group or filter table data in data visualizations by questions. The table must support questions.

Creating data visualizations grouped by questions is helpful to:

-   Determine whether questions that customers ask are getting answered.
-   Gain more information from customers during the request process.

The data source must be a non-service catalog table that has questions associated with it. You can filter or group by questions on a table extended from the Task \[task\] table, for example the Incident \[incident\] or Problem \[problem\] tables, or from the Record Producer table \[sc\_cat\_item\_producer\].

You can use questions when you create custom conditions to filter the data source. You can also use questions in any Group by or Alternative group by fields that the type of data visualization supports.

**Note:**

If there is a Record Producer associated with the table, variables defined in that Record Producer are available as Questions in the condition builder for filtering the data source, except for the following question types:

-   Label
-   Rich text label
-   Macro
-   Container

You cannot group by Record Producer variables. For more information, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Configure data visualizations](../../performance-analytics/concept/configure-data-visualizations.md)

## Use questions in data visualizations

In visualizations of data from the Task \[task\] hierarchy of tables, you can use questions defined for the table to filter or group the data.

### Before you begin

Role required: viz\_creator or higher, including itil. To see the data, you need a role permitted by a report\_view access control on the data source table

### About this task

Use a question as a filter, a group by, or an alternative group by.

**Note:** Box, and Trendbox visualizations can’t use questions as a group by or alternative group by. Single Score, Calendar Report, and Geomap visualizations don’t support grouping on any fields. Pivot Table visualizations can group by questions only as columns or rows.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and open the visualization to add the question to.

2.  Select one of the following options.

<table id="choicetable_p2g_2qf_v5"><tbody><tr><td id="d225252e182">

**Use the question as a filter**

</td><td>

Add or edit a data source and select **Add custom conditions**. If any custom conditions have already been defined, select **+ Add**. Then select **Questions** at the bottom of the field list.

</td></tr><tr><td id="d225252e200">

**Add the question as a __group by__**

</td><td>

Under **Group by**, select **+ Add**. Then select **Questions** at the bottom of the field list.

</td></tr><tr><td id="d225252e221">

**Add the question as an alternative group by**

</td><td>

Under **Group by**, select **Add alternative group by**. Then select **Questions**.

</td></tr><tr><td id="d225252e239">

**Add the question as a column or row in a pivot table**

</td><td>

Under **Group by**, select **+Add** for Columns or Rows, then select **Questions** at the bottom of the field list.**Note:**

-   If you create the report with the question as the main Group By, the question behaves as an inner join.
-   If you create the report with a regular field for primary grouping, and a secondary grouping on the question, the question works as an outer join.


</td></tr></tbody>
</table>    The available questions appear. Not all questions that are available as group by values are also available as alternative group by values.

3.  Select the question you want.

4.  If you are using the question in a custom condition, select the operator and the value.

5.  Select **Apply**.


### Question as a filter

Here you have opened the Edit data source page for a data visualization. No custom conditions have been defined for this data visualization, so you select **Add custom condition**.

![The Add custom conditions link on the Add or Edit data source page.](../../par-for-workspace/image/dv-data-source-custom-conditions.png)

Next, you scroll down the Select field list to question, select that, and select a question.

![Selecting a question for the custom filter.](../../par-for-workspace/image/add-custom-filter-questions.png)

Finally you select the operator and the value, such as Is \| A4, and select **Apply**.

### Question as a group by

In this case, you have a horizontal bar visualization of data in the Incident table. In the Group by section, you edit the group by. You scroll to the bottom of the list of fields and replace the Active field with questions, and select your question.

![Selecting a Question in a Group by field.](../../par-for-workspace/image/question-dv-groupby.png)

If you want to add a question as a row or column on a Pivot Table, the experience is almost identical.

### Question as an alternative group by

You want a different question as an alternative group by. You select **Add alternative group by** and scroll to **Questions**. Unlike other menus, its position is alphabetical instead of at the bottom. You expand **Questions**, and the list changes to a selection of questions. Not all questions that were available as a group by are available as an alternative group by. Anyway, you select some questions and press **Apply all**.

![Additional group by selector for questions.](../../par-for-workspace/image/dv-alternative-group-by-questions.png)

