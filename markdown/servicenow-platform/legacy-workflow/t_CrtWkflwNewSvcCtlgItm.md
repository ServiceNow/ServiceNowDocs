---
title: Create a workflow for a new service catalog item
description: When you create a new service catalog item, you can create a new corresponding workflow at the same time.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a workflow, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a workflow for a new service catalog item

When you create a new service catalog item, you can create a new corresponding workflow at the same time.

## Before you begin

-   If you are designing the workflow as part of an update set process, see [Workflow movement with update sets](../concept/c_WorkflowMovementWithUpdateSets.md#) before creating the workflow.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

2.  At the top of the form, next to **Catalog Items**, click **New** ![](../image/NewCatalogItemButton.png).

    The Catalog Item form opens.

3.  Add a **Name**.

4.  Select the **Process Engine** tab.

5.  Next to the **Workflow** field, click the lookup icon .

6.  Next to Workflow at the top, click **New**.

    ![Create a workflow from a Service Catalog item.](../../workflow/image/CreateWorkflowFromServiceCatalog.png) The Workflow version dialog opens in the New Workflow View. The **Table** field is set to **Requested Item \(sc\_req\_item\)** and is read-only.

7.  Add a **Name**.

8.  \[Optional\]Add a **Description**.

9.  \[Optional\] Change the stage information as necessary.

10. Click **Submit**.

    The new workflow is created with the **Begin** and **End**activities connected by a single transition. ![New workflow](../image/WorkflowNew.png)

11. Finish creating the workflow by adding activities, validating, and publishing so the workflow is available to other users.

    For more information, see [Work on workflows](work-on-workflows.md#).

12. To change advanced settings for the workflow, click the **Properties** icon.

13. Click **Update**.

    If you close the Workflow Editor, you can see the Catalog Item record. Note that the workflow is added to the Workflow field. The Show Workflow and Information icons appear next to the **Workflow** field. Hover over the information icon to view a read-only summary of the workflow.


**Parent Topic:**[Create a workflow](t_CreateAWorkflow.md)

