---
title: Add a resource operation step to invoke a subflow
description: Invoke a subflow by adding an operations step to a resource and then associating the resource to a new or existing subflow.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add operation steps to a resource block, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add a resource operation step to invoke a subflow

Invoke a subflow by adding an operations step to a resource and then associating the resource to a new or existing subflow.

## Before you begin

-   The Orchestration application is installed.

Role required: Cloud user, designer, or admin

## About this task

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Click the resource block to add an operations step to.

3.  Set the resource block to **Draft** state and then click **Operations** &gt; **Steps** &gt; **Add Step**.

    The Operation Step form appears.

4.  Select **Invoke Flow**, from the **Operation Type** list.

5.  Select **Subflow** from the **Flow Type** list.

    **Note:** You cannot invoke flows while adding a resource operation step. This is a known limitation.

6.  Select an active subflow from the **Flow/Subflow** lookup list.

7.  Specify a condition in the **Condition** field.

8.  Click **Submit**.

    The subflow operation step is attached to the resource block and appears on the page. Any input parameters associated with the subflow you selected are auto-populated on the **Input** tab.

9.  In the **Inputs** subtab, click the ![Add step parameter](../image/add-button.png) icon to add a new step parameter.

    1.  Add the following key value pair to the subflow.

        |Key|Value|
        |---|-----|
        |`flowcorrelationid`|`$(Script:CMPFlowStepHandler.generateCorrelationId)`|

10. Click the **Response Processor** tab and then click the plus icon.

    The Add Response Processor dialog box appears.

11. In the **Script Name** list, select a script for the response processor.

    For a script to appear in the **Script Name** list, the script should already have been created in the **Resource Script** tab. For more information, see [Configure a response processor](configure-response-processor.md).

12. Click **Submit**.

13. Set the resource block to **Publish** state to incorporate your changes and publish the resource block.


## What to do next

[Create a response action for Cloud Provisioning and Governance](create-subflow-action-cloud-provision-governance.md)

**Parent Topic:**[Add operation steps to a resource block](add-operation-steps.md)

