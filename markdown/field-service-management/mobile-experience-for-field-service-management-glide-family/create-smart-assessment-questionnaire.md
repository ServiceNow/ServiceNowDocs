---
title: Create Smart Assessment questionnaires from new templates
description: Create a Smart Assessment questionnaire from a new Smart Assessment template and associate them to work order tasks to gather information about the tasks.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Smart Assessment from new templates, Set up Smart Assessment questionnaires, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Create Smart Assessment questionnaires from new templates

Create a Smart Assessment questionnaire from a new Smart Assessment template and associate them to work order tasks to gather information about the tasks.

## Before you begin

Role required: questionnaire\_admin

Ensure you have authored and published Smart Assessment template.

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

You can create a smart assessment questionnaire only from a published template.

</td></tr><tr><td>

Active

</td><td>

Option to activate the Smart Assessment template for the questionnaire.

</td></tr><tr><td>

Inherited

</td><td>

You can enable the inherit functionality for a questionnaire template. For example, if a questionnaire is set at the base work order task level, its configurations are automatically inherited by all the tasks created through work order extension.

</td></tr></tbody>
</table>7.  Select **Submit**.


## Result

A questionnaire with the **Type** set to **Smart Assessment** is created.

