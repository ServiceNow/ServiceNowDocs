---
title: Configure how calendar entries look
description: To configure how calendar entries appear for a table, add calendar\_elements attributes to the System Dictionary entry for that table.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customize calendar reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Configure how calendar entries look

To configure how calendar entries appear for a table, add calendar\_elements attributes to the System Dictionary entry for that table.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Procedure

1.  Open a form for any record in that table.

2.  Right-click the form header and select **Configure** &gt; **Dictionary**.

3.  In the record list that appears, select the first record that does not have a value in the **Column name** field.

    ![Reports calendar attributes](../image/reports-calendar-attributes01.png)

4.  Switch the **Dictionary Entry** form to the **Advanced** view.

5.  In the **Attributes** field, add **calendar\_elements=&lt;field name&gt;;&lt;field name&gt;**, listing the fields you want to appear in each entry of your calendar report separated by semi-colons.

    **Note:** When you define attributes for calendar elements, you replace the default display elements of **number** and **short\_description** with the attributes that you list in this field. To add any additional attributes to the calendar entry and retain the number and short description of the change, include the **number** and **short\_description** fields in your attributes. For example, to add state information to your task calendar, add the following attribute to the Task table:

    ```
    calendar_elements=number;short_description;state
    ```

    ![Reports calendar attributes](../image/reports-calendar-attributes02.png)

6.  If the table already has an attribute, separate it from the attribute you are adding with a comma, for example:

    ```
    reference_index_include=active,calendar_elements=number;short_description;state
    ```

7.  Select **Update**.


## Result

The calendar entries display the attributes you have added for the selected table.

![Calendar entry with number, short description, and added state attribute](../image/calendar-attribute-change-result-rd.png)

**Parent Topic:**[Customize calendar reports](../concept/c_CustomizeCalendarReports.md)

**Related topics**  


[Modifying and adding calendar report system properties](modify-add-calendar-sys-props.md#)

[Change highlighting of calendar report events](t_HighlightACalendarEntry.md)

[Customize start and end dates](t_CustomizeAStartAndEndDate.md)

