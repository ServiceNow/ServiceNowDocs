---
title: Execute response processor for subflow
description: Execute a response processor for a subflow to get the subflow data back into a configuration item \(CI\). The response processor picks up the data, sends the data to the CMDB, which in turn puts the data in a CI.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure a response processor, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Execute response processor for subflow

Execute a response processor for a subflow to get the subflow data back into a configuration item \(CI\). The response processor picks up the data, sends the data to the CMDB, which in turn puts the data in a CI.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## About this task

Before you execute a response processor for a subflow, you must create a subflow, attach the subflow to a resource block operation step, and then generate the catalog. To return a response from the subflow to the Cloud Provisioning and Governance application, the subflow must create a record in the sn\_cmp\_flow\_result table with the appropriate details as follows.

```

 flow_type           : 'sys_flow_context'
 flow_correlation_id : flowcorrelationid (This variable must be present in the Resource Block as mentioned here [Add a resource operation step to invoke a subflow](add-resource-op-step-subflow.md).
 flow_output         : String that will be processed by Response Processor
 flow_error          : Error string if there is any error
 error_detail        : Error detail string if there is any error
```

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Open a resource block that is in a draft state and navigate to **Operations** **Steps**.

3.  Select **Add Step**.

    The Add Operation Steps dialog box appears.

4.  Add a workflow operation step.

    See [Add operation steps to a resource block](add-operation-steps.md).

    The workflow operation step gets attached to the resource block and appears on the page. Any input parameters associated with the workflow appear on the **Input** tab.

5.  Select **Generate Catalog**.

    The workflow appears in the Cloud User Portal as an operation. Select the workflow from the **Select Operation** picker to execute the operation. The status of the operation is visible in the Track operation subtab.

6.  Select the **Response Processor** tab and then select the plus icon.

    The Add Response Processor dialog box appears.

    ![Adding a response processor with a workflow.](../image/add-response-processor.png)

7.  In the **Script Name** list, select a script for the response processor.

    For a script to appear in the **Script Name** list, the script should already have been created in the **Resource Script** tab.

8.  Select **Submit**.

    The script appears in the **Response Processor** tab. You can open the script and modify the script.


**Parent Topic:**[Configure a response processor](configure-response-processor.md)

