---
title: Generate a project plan using project plan generation skill
description: Use Project plan generation skill to generate a project plan from natural language input, uploaded files, or both.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Generate a project plan using project plan generation skill

Use Project plan generation skill to generate a project plan from natural language input, uploaded files, or both.

## Before you begin

Role required: it\_project\_manager

-   Install Now Assist for Strategic Portfolio Management \(SPM\) plugin.
-   To use attachments to generate a project, activate the document intelligence skill. The default LLM is Azure OpenAI. Switching to a different model may affect accuracy.

-   The project plan generation skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure Now Assist Admin features](../concept/configuring-na-spm.md).


## About this task

Now Assist scans your project and task details to generate content. Review and edit the output before creating the project. Supported file types are word, pdf, excel, and powerpoint, with a 5 MB file size limit. Only the first five attachments are processed.

For project and task supported column configurations, see [Supported columns for project and task generation](../reference/column-configuration-project-tasks.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  Select **Generate project** to use Now Assist to generate a project.

    ![AI-generated project plan in Project Workspace.](../images/now-assist-project-plan-page.png)

    To create a project without using Now Assist, use **New project from template** or **New project** options.

3.  Provide your project input using one or more of these methods.

    -   In the text field, describe your project using natural language. If you provide only natural language input, the document intelligence skill is not required.
    -   Select Attach files and upload a word, pdf, excel, or powerpoint document. To use file attachments, activate the document intelligence skill. For more information, see Activate a Now Assist in Document Intelligence skill.
    **Note:** Attach a file or enter context as free-form text before proceeding. No input returns an error. Insufficient context may also trigger an error.

4.  Select **Next** to generate the project.

5.  Select **Create project**.

6.  Review the pre-populated project name, approved start date, approved end date, or business case.

    ![Now assist generated project plan.](../images/now-assist-generated-project.png)

    Edit the fields as needed and add a description.

    **Note:** Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.


## Result

The project is created with the generated tasks, including task hierarchy and dates derived from your input.

**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

