---
title: Customize the task plan template AI workflow for your table
description: The out-of-the-box Task Plan Template Creation workflow creates task plan template items in the Task \[task\] table. To create items in a different table, such as the Case \[sn\_customerservice\_case\] table or a telecom order table, clone the workflow use case and update its base plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customize-task-plan-template-ai-workflow.html
release: brazil
topic_type: task
last_updated: "2026-09-04"
reading_time_minutes: 2
keywords: [task plan template, AI workflow, use case, target record]
breadcrumb: [Create a task plan template from a document, Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Customize the task plan template AI workflow for your table

The out-of-the-box Task Plan Template Creation workflow creates task plan template items in the Task \[task\] table. To create items in a different table, such as the Case `[sn_customerservice_case]` table or a telecom order table, clone the workflow use case and update its base plan.

## Before you begin

Role required: admin

## About this task

The out-of-the-box **Task Plan Template Creation** workflow is configured with the following target values:

-   **target\_record**: `task`
-   **table** for template items: `task`
-   **parent\_field\_identifier** for each task: `parent`

To generate template items in a different table, clone the use case and update these values in the cloned copy. Some example target tables for different domains:

-   Customer service case management: the Case \[sn\_customerservice\_case\] table or the Case Task \[sn\_customerservice\_task\] table
-   Telecommunications order management: telecom order tables
-   Retail service management: retail case tables

**Note:** Clone the workflow rather than editing the base one. Editing the base use case can cause your changes to be lost during upgrades.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Use Cases** &gt; **Create and manage** &gt; **Agentic workflows**.

2.  Open the **Task Plan Template Creation** workflow.

    The record is in the **Task Plan Template AI Agents** application scope.

3.  To clone the workflow, select **Duplicate**.

    The cloned workflow is created as a copy that you can edit without affecting the base configuration.

4.  In the cloned workflow, update the **Base plan** field to point to your target table.

    1.  Change `Use target_record "task"` to your target table name.

        For example, `Use target_record "sn_customerservice_case"`.

    2.  Change `Set "table" field for the template items as "task"` to the table where each template item must be created.

        The out-of-the-box workflow maps everything to the Task \[task\] table for simplicity. You can instead define multiple rules, mapping different item categories to different tables. For example, map order items to an order table and change items to a change table.

    3.  Change `Set "parent_field_identifier" for each task as "parent"` to the parent field name on your target table.

5.  Save the cloned workflow.


## Result

When users run the task plan template AI workflow, the agent creates template items in the table specified in the cloned use case.

## What to do next

Test the customized workflow by uploading a sample document. For more information about running the workflow, see [Create a task plan template from a document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/create-task-plan-template-from-document.md).

