---
title: Generate tasks for a project using project plan generation skill
description: Use project plan generation skill to populate an empty project with tasks by providing text input, uploading files, or both.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/generate-tasks-using-ai-pw.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-04-18"
reading_time_minutes: 1
breadcrumb: [Managing projects with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Generate tasks for a project using project plan generation skill

Use project plan generation skill to populate an empty project with tasks by providing text input, uploading files, or both.

## Before you begin

Role required: it\_project\_manager

-   Install Now Assist for Strategic Portfolio Management \(SPM\) plugin.
-   To use attachments to generate a project, activate the document intelligence skill. The default LLM is Azure OpenAI. Switching to a different model may affect accuracy.

-   The project plan generation skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/configuring-na-spm.md).


## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  Create a project or open any project without tasks.

3.  Select **Generate tasks** to use Now Assist to generate tasks.

    To create a project task without using Now Assist, use **Add Task** option.

    \[Omitted image "generate-tasks-now-assist-spm.png"\] Alt text: Generate tasks using Now assist.

4.  Provide your project task input using one or more of these methods.

    -   In the text field, describe your project tasks using natural language. If you provide only natural language input, the document intelligence skill is not required.
    -   Select Attach files and upload a word, pdf, excel, or powerpoint document. A preview of the attachment appears before you proceed. To use file attachments, activate the document intelligence skill. For more information, see [Activate a Now Assist in Document Intelligence skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/activate-now-assist-in-document-intelligence-skill.md).
    **Note:** Attach a file or enter context as free-form text before proceeding. No input returns an error. Insufficient context may also trigger an error.

5.  Select **Submit** to generate the project.

6.  Review the task details for a project on the planning page.

    \[Omitted image "generated-tasks-page-na-spm.png"\] Alt text: AI-generated tasks for a project in Project Workspace.

    **Note:** Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.


## Result

The project is created with the generated tasks, including task hierarchy and dates derived from your input.

**Parent Topic:**[Managing projects with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/use-projects-pw.md)

