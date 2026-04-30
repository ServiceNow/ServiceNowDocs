---
title: Add a resource operation step to invoke a workflow
description: You can invoke a workflow by adding an operations step to a resource and then associating the resource to a workflow.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Add operation steps to a resource block, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add a resource operation step to invoke a workflow

You can invoke a workflow by adding an operations step to a resource and then associating the resource to a workflow.

## Before you begin

-   The Orchestration application is installed.
-   Role required: Cloud user, designer, or admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Click the resource block to add an operations step to.

3.  Set the resource block to **Draft** state and then click **Operations** &gt; **Steps** &gt; **Add Step**.

    To enable the workflow to be exported as part of the update sets, you must create an extension interface and add the new operation. See [Extend Cloud Provisioning and Governance resource blocks with an override operation](extend-cloud-management-entities.md) for details.

4.  On the Add Operation Steps popup, select **Invoke Workflow**for **Operation Type**.

5.  Select the **Workflow** from the list of workflows that you created.

    The system can filter the list using tags. To add a tag:

    1.  Navigate to **System Properties**.
    2.  Locate and select the system property **sn\_cmp.workflow\_tag\_filter**.
    3.  Edit the property. Add a tag or comma-separated list of tags.
    4.  Click **Save**.
6.  Filter the workflows.

    1.  On the workflow table, open the workflow.

    2.  Click **Add Tag**.

    3.  Enter the value that you provided earlier in the property **sn\_cmp.workflow\_tag\_filter**

    4.  Click **Enter**.

        The value is added as a tag to the workflow.

    The new step appears after the software generates the new Day 2 Operation Catalog.

7.  Add a workflow.

    1.  After you create the step, the system adds the workflow inputs to the operation input parameters.

    2.  Provide the mapping for these parameters, if needed.

    3.  Click the **Generate Catalog** button to create the catalog item for the operation.

    4.  After the catalog generates, you can add from the load and field change rules to the catalog items.

    Workflows can exist that are created on tables other than global. You can add a workflow created on such a table. To execute operations on this type of workflow, you need the sys\_id of the record in which the workflow is executing to create the current record. So when the designer adds a workflow that is on table other than global, the system creates a **wf\_current** parameter in the operation input parameter. You can then write an expression to map the sys\_id of the resource in which the operation is executing. Once this is completed, the designer can use the ‘current’ key word in workflow scripts.

8.  Set the resource block to the **Published** state to make the workflow available in the Cloud User Portal.


**Parent Topic:**[Add operation steps to a resource block](add-operation-steps.md)

