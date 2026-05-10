---
title: Create a questionnaire for a work order or task
description: Create a questionnaire record and then associate it with Work Order Task table.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Survey-based questionnaires, Questionnaires, Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Create a questionnaire for a work order or task

Create a questionnaire record and then associate it with Work Order Task table.

## Before you begin

Role required: admin

## About this task

The administrator can view questionnaire records from the Questionnaire list and questionnaires by navigating to **Surveys** &gt; **View Surveys**.

## Procedure

1.  Navigate to **Field Service** &gt; **Administration** &gt; **Questionnaire**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the questionnaire.|
    |Active|Option to make the questionnaire record active. The administrator can attach active questionnaires to work orders and work order tasks.|
    |Description|Brief description of the questionnaire record.|
    |Introduction|Text that appears at the beginning of the questionnaire.|
    |End note|Text that appears at the end of the questionnaire.|
    |Table|Table that is associated with this questionnaire record.|
    |Trigger condition|Trigger condition that determines when the questionnaire is applicable. Use the condition builder to create trigger conditions. When these conditions are true for a work order or work order task, the questionnaire is added to the work order.|
    |Mandatory|Option to make the questionnaire mandatory. When enabled, the agent must complete the questionnaire before closing the work order or work order task.|
    |Close before|State that the work order or work order task must be in before the agents can complete a mandatory questionnaire.|

4.  Select **Submit**.

    ![questionnaire form](../image/create-questionnaire.png)

    The system creates the record, displays the Questionnaire form, and adds the **Questionnaire Designer** button.

5.  To create the text of the questionnaire, select **Questionnaire Designer**.

    The Survey Designer tool opens in a new window.

6.  To create the questions or checklist items that appear on the questionnaire, use the [Survey designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyDesigner.md) tool.

7.  Select **Save** and close the Survey Designer window.


## Result

The questionnaire is created.

## What to do next

To view questionnaire records from the Questionnaire list and questionnaires, go to **Surveys** &gt; **View Surveys**.

To edit a questionnaire, open the form, make your changes, and select **Update**.

**Related topics**  


[Complete a questionnaire for a work order or task](complete-wo-or-task-questionnaire.md)

