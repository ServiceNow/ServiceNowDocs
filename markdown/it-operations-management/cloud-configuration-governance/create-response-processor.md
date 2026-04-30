---
title: Execute response processor for workflow
description: Execute a response processor for a workflow to get the workflow data back into a configuration item \(CI\). The response processor picks up the data, sends the data to the CMDB which in turn puts the data in a CI.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure a response processor, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Execute response processor for workflow

Execute a response processor for a workflow to get the workflow data back into a configuration item \(CI\). The response processor picks up the data, sends the data to the CMDB which in turn puts the data in a CI.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer.

## About this task

Before you execute a response processor for a workflow, you need to create a workflow, attach the workflow to a resource block operation step, and then generate the catalog. To return the response from the workflow to the Cloud Provisioning and Governance application, the workflow designer needs to add the **Cloud Return Response** activity to the workflow. A variable needs to be mentioned inside the **Cloud Return Response** activity for the response. See [Worflow](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Open a resource block that is in a draft state and navigate to **Operations** **Steps**.

3.  Click **Add Step**.

    The Add Operation Steps dialog box appears.

4.  Add a workflow operation step.

    See [Add operation steps to a resource block](add-operation-steps.md).

    The workflow operation step gets attached to the resource block and appears on the page. Any input parameters associated with the workflow appear on the **Input** tab.

5.  Click **Generate Catalog**.

    The workflow appears in the Cloud User Portal as an operation. Select the workflow from the **Select Operation** picker to execute the operation. The status of the operation is visible in the Track operation sub tab.

6.  Click the **Response Processor** tab and then click the plus icon.

    The Add Response Processor dialog box appears.

    ![Adding a response processor with a workflow.](../image/add-response-processor.png)

7.  In the **Script Name** list, select a script for the response processor.

    For a script to appear in the **Script Name** list, the script should already have been created in the **Resource Script** tab.

8.  Click **Submit**.

    The script appears in the **Response Processor** tab. You can open the script and make modifications to the script.


**Parent Topic:**[Configure a response processor](configure-response-processor.md)

