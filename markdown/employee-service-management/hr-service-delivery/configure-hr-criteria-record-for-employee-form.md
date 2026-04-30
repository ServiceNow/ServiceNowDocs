---
title: Create an HR criteria record for an employee form
description: Create an HR criteria record for an employee form based on the employee answers stored in the Metric Result \[asmt\_metric\_result\] table.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Collect employee input, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create an HR criteria record for an employee form

Create an HR criteria record for an employee form based on the employee answers stored in the Metric Result \[asmt\_metric\_result\] table.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

Answers from the employee form are stored in the Metric Results \]asmt\_metric\_result\] table. You can query the answers using HR criteria. For example, if on an invention disclosure form, the new hire answers yes, then you can use that answer to trigger the creation of another task to collect details on the invention.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Criteria**.

2.  Click **New**.

3.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the HR criteria record.|
    |Description|Description of the HR criteria record.|
    |Active|Option to activate the HR criteria record for use.|

4.  Right-click the former header and click **Save**.

    The **Conditions** section appears.

5.  In the **Conditions** section, click **New**.

6.  On the HR Condition form, enter the following field values.

<table id="table_r5b_dzt_thb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

&lt;Name for the HR condition&gt;

</td></tr><tr><td>

Table

</td><td>

Metric Result \[asmt\_metric\_result\] table

</td></tr><tr><td>

Employee form

</td><td>

Select the employee form you want to query. This field appears when the Metric Result table is selected in the **Table** field.

</td></tr><tr><td>

Condition

</td><td>

Select the question and answer from the employee form you want to query.For the question, provide the following condition:

 \[Metric\] \[is\] \[&lt;Question&gt;\]

 For the answer, provide the following condition based on the value type:

 -   **\[String value\] \[is\] \[&lt;Answer&gt;\]**
-   **\[Reference value\] \[is\] \[&lt;Answer&gt;\]**
-   **\[Actual value\] \[is\] \[&lt;Answer&gt;\]**
 **Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](../concept/hr-criteria.md#).

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr><tr><td>

User column

</td><td>

Assigned to

</td></tr></tbody>
</table>7.  Click **Submit**.

8.  On the HR Criteria form, click **Update**.


## What to do next

Depending on the case type, the HR criteria record will use the following survey instance:

-   If you are using the HR criteria record with a lifecycle event, it will use the survey instance that is associated with the lifecycle event case.
-   If you are using the HR criteria record with any other HR case, it will use the latest survey instance.

**Parent Topic:**[Collect employee input](../concept/employee-form-configuration.md)

