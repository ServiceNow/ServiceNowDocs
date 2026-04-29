---
title: Add a resource operation step to invoke a subflow
description: Invoke a subflow by adding an operation step to a resource and linking it to a new or existing subflow.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add operation steps to a resource block, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add a resource operation step to invoke a subflow

Invoke a subflow by adding an operation step to a resource and linking it to a new or existing subflow.

## Before you begin

Make sure the Orchestration application is installed.

Role required: Cloud user, designer, or admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Set the resource block to **Draft** state by toggling the publish and then select **Operations** &gt; **Steps** &gt; **Add Step**.

    The Add Operation Steps form appears.

3.  From the **Operation Type** list, select **Invoke Flow**.

4.  From the **Content Type** list, select **Subflow**.

    **Note:** You cannot invoke flows while adding a resource operation step. This is a known limitation.

5.  Select an active subflow from the **Flow/Subflow** lookup list.

6.  Specify a condition in the **Condition** field.

7.  Select **Submit**.

    The subflow operation step is attached to the resource block and appears on the page. Any input parameters associated with the subflow you selected are auto-populated on the **Input** tab.

8.  In the **Inputs** subtab, select the ![Add step parameter](../image/add-button.png) icon to add a new step parameter.

    1.  Add the following key value pair to the subflow.

        |Key|Value|
        |---|-----|
        |`flowcorrelationid`|`$(Script:CMPFlowStepHandler.generateCorrelationId)`|

9.  Select the **Response Processor** tab and then select the plus icon.

    The Add Response Processor dialog box appears.

10. In the **Script Name** list, select a script for the response processor.

    For a script to appear in the **Script Name** list, the script should already have been created in the **Resource Script** tab. For more information, see [Configure a response processor](configure-response-processor.md).

11. Select **Submit**.

12. Set the resource block to **Publish** state to incorporate your changes and publish the resource block.


## What to do next

[Create a response action for Cloud Provisioning and Governance](create-subflow-action-cloud-provision-governance.md)

**Parent Topic:**[Add operation steps to a resource block](add-operation-steps.md)

