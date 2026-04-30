---
title: Create Smart Assessment template for Workplace Case and Task
description: Smart assessment templates define the structure, questions, and sections that workplace agents complete when working on cases and tasks. Case managers create templates to standardize data collection and ensure consistent quality checks across workplace cases and tasks. These assessments automatically attach to cases and tasks based on configurable trigger conditions.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-01-27"
reading_time_minutes: 2
breadcrumb: [Smart Assessment for Workplace Case and Task, Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create Smart Assessment template for Workplace Case and Task

Smart assessment templates define the structure, questions, and sections that workplace agents complete when working on cases and tasks. Case managers create templates to standardize data collection and ensure consistent quality checks across workplace cases and tasks. These assessments automatically attach to cases and tasks based on configurable trigger conditions.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

**Note:** Make sure that the Smart Assessment plugin is enabled before creating assessment templates.

## Procedure

1.  Navigate to **Workspaces** &gt; **Workplace Central** &gt; **Case Management**.

2.  Select **Create Smart Assessments**.

3.  On the Assessment Workspace page, select **New template**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Template name|Name of the template. If you want to add a separate assessment name, select the ![](../../workplace-service-delivery/images/new_assessment_temp.png) icon and add a name for the assessment.|
    |Description|Description of the template.|
    |Purpose|The assessment template category for the new template. For example, Workplace services.|
    |Assessment targets|Select the table that assessments will access. For example, Workplace case \[sn\_wsd\_case\_workplace\_case\]. Select only one table from the list.|

5.  Select **Create**.

    The Assessment Workspace page displays where you can specify the template details.

6.  Under the General tab, do the following:

    1.  Select **Details** and modify the assessment details if required.
    2.  Select **Settings** and specify the **Duration \(number of days\)** and **Assessment reader role** details.
    3.  Select **Save**.
7.  Start building a template by adding instructions, sections, and questions under the Questions tab.

    1.  Select **+ Add instructions** and define clear guidance for Workplace Agents explaining the purpose and expectations for completing the assessment.
    2.  Select **+ Add section** and enter the **Name** and **Description** details.
    3.  Select **+ Add question** and enter the question.

        **Note:** You must select an existing section or create a section to add a question.

        -   Toggle the Required configurable option to make the question conditionally visible.
        -   Select the response input type from the available options. For example, select Radio button and enter the Choices.
        -   Select **Add choice** to add multiple choices.
        -   Select **Add additional content** drop-down and select **Question description** or **Guidance** to add the additional details.
        -   Select **Save**.
        ![](../../workplace-service-delivery/images/wsd-input-types.png)

    4.  Select **+ Add assessment reference** and Add reference data to appear the card details under the Smart Assessments tab in a workplace case.

        -   In the **Card description** field, provide a description for the assessment reference card.
        -   Select the required columns and select **Add**.
        ![](../../workplace-service-delivery/images/addreference_card.png)

8.  Select **Publish** to publish the assessment template.

    **Note:** Templates must be published before they can be attached to triggers and used in workplace cases.


**Parent Topic:**[Smart Assessment for Workplace Case and Task](smart-assessment-for-workplace-case-and-task.md)

