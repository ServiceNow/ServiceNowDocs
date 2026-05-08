---
title: Author and publish a Smart Assessment template
description: Author and publish Smart Assessment template, and associate it with Work Order Task tables to create Smart Assessment questionnaires for work order tasks using this template.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Smart Assessment from new templates, Set up Smart Assessment questionnaires, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Author and publish a Smart Assessment template

Author and publish Smart Assessment template, and associate it with Work Order Task tables to create Smart Assessment questionnaires for work order tasks using this template.

## Before you begin

Role required: questionnaire\_admin

## About this task

Author a new Smart Assessment template to configure Smart Assessment questionnaire from new template.

To configure Smart Assessment questionnaires by migrating from survey-based questionnaires, review the template and publish it.

**Note:**

-   You can create a smart assessment questionnaire only from a published template.

-   You can update a published template only if no active assessment is associated with the template.


## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Perform one of the following actions:

    -   Select **New template** to create a new template.
    -   Select the name of an existing template to review and author an update an existing template.
3.  On the form, modify or fill in the fields.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template name

</td><td>

Unique name for the template.

</td></tr><tr><td>

Assessment name

</td><td>

An optional alternative name for generated assessment that will display to respondents rather than the template name.

</td></tr><tr><td>

Description

</td><td>

Purpose of the template.

</td></tr><tr><td>

Purpose

</td><td>

Category of the assessment template. This value should be **Field Service**.

 **Note:**

-   **Field Service** is the only **Purpose** available in Field Service Management for smart assessments. However, you can create and customize additional purposes, as required. For more information, see Create an assessment template category.
-   To view and use any template from the newly created purpose, ensure that you have access to the correct role associated with it.


</td></tr><tr><td>

Assessment target

</td><td>

Table to be assessed. Selecting multiple tables makes the scope a combination of records from each table.Select **Work Order Task** to create the template to assess work order tasks.

</td></tr></tbody>
</table>4.  Select **Create**.

5.  Fill in the template with overall instructions, questions, optional guidance for responding to a question, and sections that group the related questions.

    For more information, see Add instructions and questions to an assessment template.

6.  Select **Save**.

7.  Select **Publish** to publish the new template.


