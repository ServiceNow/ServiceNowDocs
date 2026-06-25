---
title: Configure how calendar entries look
description: To configure how calendar entries appear for a table, add calendar\_elements attributes to the System Dictionary entry for that table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/reporting/t\_ConfigureACalendarAttribute.html
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize calendar reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Configure how calendar entries look

To configure how calendar entries appear for a table, add calendar\_elements attributes to the System Dictionary entry for that table.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## Procedure

1.  Navigate to the table your report is based on, for example incident.list.

2.  Open a form for any record in the table.

3.  Select the Additional actions menu \(\[Omitted image "additional-actions.png"\] Alt text: Additional actions menu icon\) and choose **Configure** &gt; **Dictionary**.

4.  In the record list that appears, select the first record that does not have a value in the **Column name** field.

    \[Omitted image "reports-calendar-attributes01.png"\] Alt text: Reports calendar attributes

5.  Switch the **Dictionary Entry** form to the **Advanced** view.

6.  In the **Attributes** field, add **calendar\_elements=&lt;field name&gt;;&lt;field name&gt;**, listing the fields you want to appear in each entry of your calendar report separated by semi-colons.

    **Note:** When you define attributes for calendar elements, you replace the default display elements of **number** and **short\_description** with the attributes that you list in this field. To add any additional attributes to the calendar entry and retain the number and short description of the change, include the **number** and **short\_description** fields in your attributes. For example, to add state information to your task calendar, add the following attribute to the Task table:

    ```
    calendar_elements=number;short_description;state
    ```

    \[Omitted image "reports-calendar-attributes02.png"\] Alt text: Reports calendar attributes

7.  If the table already has an attribute, separate it from the attribute you are adding with a comma, for example:

    ```
    reference_index_include=active,calendar_elements=number;short_description;state
    ```

8.  Select **Update**.


## Result

The calendar entries display the attributes you have added for the selected table.

\[Omitted image "calendar-attribute-change-result-rd.png"\] Alt text: Calendar entry with number, short description, and added state attribute

**Parent Topic:**[Customize calendar reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_CustomizeCalendarReports.md)

**Related topics**  


[Modifying and adding calendar report system properties]()

[Change highlighting of calendar report events]()

[Customize start and end dates]()

