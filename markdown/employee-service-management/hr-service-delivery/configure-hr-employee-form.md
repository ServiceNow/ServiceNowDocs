---
title: Create an employee form
description: Create or modify an employee form so that you can collect employee input. Configuration of the employee form is a three-part process. First, create the employee form record. Second, use the survey designer to build one or more questions for the employee form. Third, you can map questions from the employee form to corresponding fields on a target table.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Collect employee input, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create an employee form

Create or modify an employee form so that you can collect employee input. Configuration of the employee form is a three-part process. First, create the employee form record. Second, use the survey designer to build one or more questions for the employee form. Third, you can map questions from the employee form to corresponding fields on a target table.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Employee Form**.

2.  Click **New**.

3.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the employee form.|
    |Description|Description of the employee form.|
    |Active|Option to activate the employee form for use.|

4.  Right-click the form header and click **Save**.

    The **Form Designer** button appears.

5.  Click **Form Designer** to open the survey designer in a new window.

6.  Use the survey designer to build questions for your employee form.

    **Note:** If you plan to map the question to a table field, make sure that the data types match. Mapping is supported for the following question types:

    -   Boolean
    -   Choice
    -   Date
    -   Date/Time
    -   Number
    -   String
    -   Reference
    For further details on the different question types, see [Survey designer elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyDesignerElements.md).

    **Note:** There are several limitations with native mobile screens, including custom and rating data types, validation scripts, read-only questions, and additional information fields. See this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2769842) for more details.

    The following GIF shows an example of a user building a reference question and a boolean question in the survey designer.

    **Note:** Make sure to provide each question a name so that you can more easily identify the question when creating mappings or HR criteria records.

7.  After building your questions, click **Save and Publish**.

8.  Return to and reload the employee form.

    The **Add Mappings** field appears on the employee form.

9.  If you want to map one or more questions to fields on a table, fill in the following new fields on the form.

<table id="table_rxh_3np_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Mappings

</td><td>

Option to map questions from the employee form to fields on a target table. This field appears after you save and publish at least one question in the survey designer.

</td></tr><tr><td>

Table

</td><td>

Select the table that the employee form is mapping to. This field appears when **Add Mappings** is selected.

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to identify one record on the table to access. Make sure that the result is a match to a single record. This field appears when **Add Mappings** is selected.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideFilterScopedAPI.md).

</td></tr></tbody>
</table>    For example, you can map an employee form to the HR Profile \[sn\_hr\_core\_profile\] table with the following condition:

    \[User\] \[is \(dynamic\)\] \[Me\].

    The result is that the logged-in user's HR profile record is accessed for mapping.

10. To map one or more questions from the employee form to fields on the target table.

    1.  In the **Employee Form Field Mappings** section, click **New**.

    2.  Fill in the fields on the form.

<table id="table_vbm_3zw_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee form

</td><td>

This field is automatically set to the name of the employee form.

</td></tr><tr><td>

Table name

</td><td>

This field is automatically set to the table that the employee form is associated with.

</td></tr><tr><td>

Question

</td><td>

Question from the employee form that is being mapped from.**Note:** Make sure that the data type matches that of the target field.

</td></tr><tr><td>

Field

</td><td>

Field that is being mapped to**Note:** Make sure that the data type matches that of the source question.

</td></tr><tr><td>

Read only

</td><td>

Option to make the question read-only. If selected, the user can read but not update the field value on the employee form. This field appears after you select a question in the **Question** field.

</td></tr></tbody>
</table>        For example, you can map a question for the user's manager to the corresponding field on the User \[sys\_user\] table. When the user views the employee form in an HR task, they will see their manager's name filled in for that field. Because it is marked as read-only, the user will be able to read but not update that field.

    3.  Click **Submit** or **Update**.

    4.  Repeat the process as needed.

11. Click **Update**.


## What to do next

You can use the employee form in task forms to collect employee input from users.

The following GIF shows an example of an HR agent creating a collect employee input task for an employee, Eva Seahorn, as part of an HR case.

The follow GIF shows an example of the employee, Eva Seahorn, then completing the collect employee input to-do in the Employee Center.

**Parent Topic:**[Collect employee input](../concept/employee-form-configuration.md)

