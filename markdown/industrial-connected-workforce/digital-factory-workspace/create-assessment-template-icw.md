---
title: Create an assessment template
description: Create an assessment template for creating standards from templates in the Digital Factory Workspace.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using templates to create standards, Industrial Guided Tasks, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create an assessment template

Create an assessment template for creating standards from templates in the Digital Factory Workspace.

## Before you begin

Role required: sn\_icw\_igt.standard author

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Select **New template**.

3.  One the Assessment template form, fill in the fields.

    For a description of the field values, see [Create assessment template form](https://www.servicenow.com/docs/access?context=create-assessment-template-form&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US). The Purpose field lets you select from the list of assessment template categories.

    **Note:**

    -   Don’t select the Industrial Guided Task category because it’s reserved for creating standards without the use of templates.
    -   Make sure that the selected category is linked to the ICW User \[sn\_icw.user\] or one of its extended roles.

        To check categories and their roles, navigate to **All** &gt; **Smart Assessment Engine** &gt; **Template Categories**.

    -   Don’t set the Assessment target, as setting this field breaks the execution.
4.  Select **Create**.

    The template is now created and available in the list of assessment templates in the Assessment Workspace.

5.  In the **Questions** tab, fill in the template.

    For a description of the field values, see [Add instructions and questions to an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-populate&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

    **Note:** The following controls are to be kept as is:

    -   Don’t set **General** &gt; **Details** &gt; **Assessment targets**.
    -   Don’t set or change **General** &gt; **Settings** &gt; **Assessment reader role**.
6.  Select **Publish**.


## Result

The template is now available when creating standards in the Standards hub.

**Parent Topic:**[Using templates to create standards](../concept/creating-standards-from-templates.md)

