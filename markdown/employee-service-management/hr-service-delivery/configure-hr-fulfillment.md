---
title: Configure HR fulfillment instructions
description: Use HR fulfillment instructions to provide focused and targeted instructions for an HR case.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HR fulfillment instructions, HR services, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure HR fulfillment instructions

Use HR fulfillment instructions to provide focused and targeted instructions for an HR case.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Fulfillment Instructions**.

2.  Click **New** or open an existing fulfillment instruction.

3.  On the form, fill in the fields.

<table id="table_i2n_jdv_bhb"><thead><tr><th>

Field

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Label of the fulfillment instructions.

</td></tr><tr><td>

Table

</td><td>

Name of the table that contains the fulfillment instructions for an HR case.

</td></tr><tr><td>

Condition

</td><td>

Conditions under which the fulfillment instructions are made available for an HR case.The conditions determine which fulfillment instructions appear for an HR case. For example, you can set conditions that an HR case has different fulfillment instructions by location.

**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

 For additional information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Active

</td><td>

Fulfillment instructions that are active and available for use.

</td></tr><tr><td>

Order

</td><td>

Order that the fulfillment instructions appear for an HR case in relation to other fulfillment instructions.

</td></tr><tr><td>

Instructions

</td><td>

Text that provides instructions on how to complete the HR case.Use the tool suite to format the instructions.

</td></tr><tr><td>

Knowledge articles

</td><td>

Knowledge articles that you want to attach to the fulfillment instructions. HR agents use knowledge articles as reference when fulfilling an HR case.**Note:** Knowledge articles are visible only to HR agents and not to employees.

</td></tr></tbody>
</table>    **Note:** Previously, Fulfillment Instructions and Checklists were configured from HR services. Checklists are still configured from HR services. For more information on checklists, see [Checklists in HR cases](../concept/c_ChecklistsInHRCasesAndTasks.md).

4.  Click **Submit** or **Update**.


**Parent Topic:**[HR fulfillment instructions](../concept/hr-fulfillment-instructions.md)

