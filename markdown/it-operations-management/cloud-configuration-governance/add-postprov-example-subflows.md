---
title: Add pre- or post-provisioning operations to a template-based catalog item
description: Create a post-provisioning operation using subflows on a template-based catalog item.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add pre- or post-provisioning operations to a template-based catalog item

Create a post-provisioning operation using subflows on a template-based catalog item.

## Before you begin

Verify that the Orchestration application is installed.

Role required: Cloud user, designer, admin, sn\_cmp.cloud\_service\_designer

## Procedure

1.  In the Cloud Admin portal, navigate to **Design** &gt; **Cloud Catalog Items**.

2.  Open a catalog item.

3.  Select the **Pre Provisioning Operation** or **Post Provisioning Operation** tab.

4.  Select **New**.

5.  From the **Step Type** list, select **Flow**.

6.  Select the Search icon on the **Flow** field.

7.  From the **Subflow** look-up list, select an active subflow.

    The look-up table lists all active flows and subflows in the instance.

    **Note:** You cannot invoke flows while adding a resource operation step. This is a known limitation.

8.  In the **Order** field, specify an order for this operation.

9.  Enable the operations by selecting the **Enabled** check box.

10. Select **Submit**.

    The subflow operation step is attached to the catalog item and appears on the Pre-Provision Operation or Post-provision Operation related list.

11. Select the subflow operation step from the relevant related list to add or modify input parameters.

    **Note:**

    When creating a post-provision action, include **CMPTfeReturnAction** as the final step in the flow.

    Verify the following steps:

    -   Verify that control returns to the main order so that data and responses flow back correctly and the process closes successfully.
    -   Configure parameters to indicate whether the step resulted in an error.
    -   Send an error from this action if the step is designed to fail.
    -   Include the correlation ID. The flow will not function without it.
    Any input parameters associated with the subflow you selected are auto-populated on the Key Values related list.


## What to do next

-   Verify that the `flowcorrelationid` input parameter is created in the subflow with the following expression string:

    |Key|Value|
    |---|-----|
    |`flowcorrelationid`|`$(Script:CMPFlowStepHandler.generateCorrelationId)`|

-   To check whether the flow completes successfully, see [Create a response action for Cloud Provisioning and Governance.](create-subflow-action-cloud-provision-governance.md)

