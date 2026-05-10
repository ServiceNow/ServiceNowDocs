---
title: Create a function field
description: Create a function field to be able to group and stack a report by the results of the field's calculation.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Report on function fields, Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a function field

Create a function field to be able to group and stack a report by the results of the field's calculation.

## Before you begin

Role required: admin, function\_field\_admin

Each function field requires a label, a return type, and a definition. The definition consists of the operation and one or more fields that the operation is performed on.

**Note:** It isn’t possible to change the label or the return type after you save a function field. If necessary, deactivate the function field and start again.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**.

2.  Select the report that you want to add a function field to.

    When you configure a function field on a table, it is available anywhere you use the table on the ServiceNow AI Platform, including any report on the same table. For example, a function field that calculates the age of open incidents is available for all reports on the incident table.

3.  Open the **Configure** tab and select **Configure function field**.

4.  Enter the field name in the search bar to see if someone has already created the function field.

    Hover over the search results to see the function definition.

5.  Select **Create**.

    There can be a maximum of 20 active function fields on the table the report is based on. If the table already has 20 function fields, a creator of one of the fields or a user with the admin role must deactivate or delete one.

6.  Specify the **Label**.

    The label is the name users can see when they group or stack data in a report.

7.  Select the **Return type**.

    The return type is the kind of information the function produces. For example, the `datediff()` function returns a Duration type because it calculates the duration between two dates.

    **Note:** You do not see a message if your return type is not a logical result of the function.

8.  Select the Operation.

    The **Syntax** text box shows the name of the function preceded by `glidefunction:`.

    ![Create function field window with callouts for Label, Return type, and Add Operation. The subtract operation is highlighted.](../image/create-ff-01.png)

9.  Select the fields that the function operates on.

    Some functions require only one field; some require two or three fields. See [Report on function fields](../concept/function-fields-reporting.md). Make sure that you separate the fields with commas.

10. When the syntax is correct, you can save the function field.

    When the syntax is incorrect, you see the message: `Syntax error: Invalid expression`. You may also see other messages.

    ![Create function field window with callouts for Add field and the Syntax is correct message. The Child incidents field is highlighted.](../image/create-ff-02.png)


## Result

Configured function fields appear in the **Group by** and **Additional group by** lists after you save the report.

Use the created function field it in your report or data visualization configuration. For information on using function fields elsewhere on the ServiceNow AI Platform, see [Function field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/platform-support-functions.md).

**Parent Topic:**[Report on function fields](../concept/function-fields-reporting.md)

