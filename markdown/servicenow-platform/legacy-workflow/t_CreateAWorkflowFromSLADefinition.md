---
title: Create a workflow for an SLA Definition
description: Automate a multi-step process by creating a workflow from an SLA definition.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a workflow, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a workflow for an SLA Definition

Automate a multi-step process by creating a workflow from an SLA definition.

## Before you begin

-   If you’re designing the workflow as part of an update set process, see [Workflow movement with update sets](../concept/c_WorkflowMovementWithUpdateSets.md#) before creating the workflow.

## Procedure

1.  Open a list of SLA definitions.

    For example **Facilities &gt; SLA Definitions** or **Service Level Management &gt; SLA Definitions**.

2.  At the top of the form, next to **SLA Definitions**, click the new icon \(![New icon.](../image/NewCatalogItemButton.png)\).

3.  Select **Contract SLA** or **Service Offering SLA**.

4.  Next to the **Workflow** field, click the lookup icon.

5.  Next to **Workflow** at the top, click **New**.

    ![Create a workflow from an SLA definition.](../../workflow/image/CreateWorkflowFromSLADefinition.png)

    The Workflow Version dialog shows in the New Workflow view. The **Table** field is set to **SLA Definition \(contract\_sla\)** or **Service Offering SLA \(service\_offering\_sla\)** and is read-only.

6.  Enter a **Name**.

7.  \[Optional\] Enter a **Description**.

8.  \[Optional\] Edit the conditions fields as necessary.

9.  Click **Submit**.

    The new workflow is created with the **Begin** and **End** activities connected by a single transition.

    ![New workflow.](../image/WorkflowNew.png)

10. Finish creating the workflow by adding activities, validating, and publishing so the workflow is available to other users.

    For more information, see [Work on workflows](work-on-workflows.md#).

11. \[Optional\] Change the advanced settings for the workflow by clicking the properties icon \(![Properties icon.](../../workflow/image/PropIcon.png)\).

    If you make changes, click **Update**.


**Parent Topic:**[Create a workflow](t_CreateAWorkflow.md)

