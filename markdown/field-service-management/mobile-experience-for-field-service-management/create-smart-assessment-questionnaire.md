---
title: Create a Smart Assessment questionnaire
description: Create a Smart Assessment questionnaire and associate it with a Smart Assessment template to create work order task questionnaires.
locale: en-US
release: yokohama
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Smart Assessment questionnaires for Now Mobile Agent, Setting up Field Service Mobile Agent, Configuring Field Service Management, Field Service Management]
---

# Create a Smart Assessment questionnaire

Create a Smart Assessment questionnaire and associate it with a Smart Assessment template to create work order task questionnaires.

## Before you begin

Role required: questionnaire\_admin

## Procedure

1.  Navigate to **Field Service** &gt; **Administration** &gt; **Questionnaire**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the questionnaire.|
    |Active|Option to make the questionnaire record active. The administrator can attach active questionnaires to work orders and work order tasks.|
    |Description|Brief description of the questionnaire record.|
    |Table|Table that is associated with this questionnaire record.|
    |Trigger condition|Trigger condition that determines when the questionnaire is applicable. Use the condition builder to create trigger conditions. When these conditions are true for a work order task, the questionnaire is added to the work order task.|
    |Mandatory|Option to make the questionnaire mandatory. When enabled, the agent must complete the questionnaire before closing the work order or work order task.|
    |Close before|State that the work order or work order task must be in before agents can complete a mandatory questionnaire.|

4.  Select **Submit**.

5.  In the **Questionnaire templates** section, select **New**.

6.  On the form, fill in the fields.

<table id="table_omd_wjb_d2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Questionnaire

</td><td>

Name of the questionnaire.This field is auto-populated with the name of the questionnaire.

</td></tr><tr><td>

Smart assessment template

</td><td>

Smart Assessment template to associate with the questionnaire.**Note:**

You can create a Smart Assessment questionnaire only from a published template.

</td></tr><tr><td>

Active

</td><td>

Option to activate the Smart Assessment template for the questionnaire.

</td></tr></tbody>
</table>7.  Select **Submit**.


## Result

A questionnaire with the **Type** set to **Smart Assessment** is created.

