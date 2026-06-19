---
title: Create a workflow from a table
description: Automate a multi-step process by creating a workflow from the list view of any table that supports workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/legacy-workflow/t\_CreateAWorkflowFromATable.html
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a workflow, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a workflow from a table

Automate a multi-step process by creating a workflow from the list view of any table that supports workflows.

## Before you begin

-   If you are designing the workflow as part of an update set process, see [Workflow movement with update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_WorkflowMovementWithUpdateSets.md) before creating the workflow.

## Procedure

1.  Open a table, such as Incident or Problem, in list view. For example, navigate to **Incident &gt; Open**.

2.  Right-click in the column header and select **Configure &gt; Workflows**.

    \[Omitted image "ConfigureWorkflowsHeader.png"\] Alt text:

    The **Workflow Versions** on that table appear in a list.

3.  Click**New**.

    The **Workflow Version** opens in **New Workflow** view. The **Table** field is filled in with the table you selected in step 1 and is read-only.

4.  Enter **Name**.

5.  Enter **Description**.

6.  Edit conditions fields as necessary.

7.  Click **Submit**.

    The new workflow is added to the **Workflow Versions** list.

8.  Click the workflow **Name**.

    The new workflow is created with the **Begin** and **End**activities connected by a single transition.

    \[Omitted image "WorkflowNew.png"\] Alt text: New workflow

9.  Finish creating the workflow by adding activities, validating, and publishing so the workflow is available to other users.

    For more information, see [Work on workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/work-on-workflows.md).

10. To change advanced settings for the workflow, click the **Properties** icon \[Omitted image "PropIcon.png"\] Alt text: Properties icon. If you make changes, click **Update**.


**Parent Topic:**[Create a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/t_CreateAWorkflow.md)

