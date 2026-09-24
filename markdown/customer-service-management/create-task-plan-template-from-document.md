---
title: Create a task plan template from a document
description: Create a draft task plan template by uploading a process document or diagram. An Agentic workflow extracts the tasks and dependencies and generates the template for you to review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-task-plan-template-from-document.html
release: brazil
topic_type: task
last_updated: "2026-09-04"
reading_time_minutes: 1
keywords: [task plan template, AI agent, document upload, Now Assist]
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a task plan template from a document

Create a draft task plan template by uploading a process document or diagram. An Agentic workflow extracts the tasks and dependencies and generates the template for you to review.

## Before you begin

Role required: sn\_task\_plan.creator

## About this task

Instead of building a task plan template manually, upload a process document \(such as an SOP or process diagram\). The Agentic workflow identifies the tasks and dependencies and generates a draft template for you to review before publishing.

The workflow supports image, PDF, and DOCX files. You can create a template in one of two ways, described in the following step.

## Procedure

1.  Do one of the following.

    -   On any Task Plan Templates list, select **Create Template**. Because this request is tied directly to the workflow, the panel opens and prompts you to upload a document.
    -   Open the ServiceNow Otto panel from the top navigation, available on any page. Because this panel isn't tied to a specific workflow, describe what you want — for example, "create a template from a document" — and ServiceNow Otto suggests the matching workflow.

        The agent prompts you to upload a document that describes the process.

2.  Select **Click here to upload a file** and select an image, PDF, or DOCX file that describes the process.

    The Agentic workflow processes the uploaded file, extracts the tasks, and identifies the dependencies between them.

3.  If the workflow finds similar task plan templates, review them before continuing.

    Make sure the Task Plan Template table is indexed for AI Search. If it isn't indexed, the workflow doesn't detect or display similar templates.

    -   Select `No` to use one of the existing templates instead. The workflow ends the request.
    -   Select `Yes` to continue creating a new template.
4.  Review the draft template summary that the agent returns.

    The summary shows the template created, along with its template items and dependencies.


## Result

The task plan template is created in the Draft state. You can edit the template items, template item conditions, and dependencies before you publish the template.

## What to do next

Review and edit the draft template as needed. For more information about the actions available in the Draft state, see [Task plan templates states and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/task-plan-templates-states.md).

