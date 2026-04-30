---
title: Create a multi-asset onboarding process
description: Onboard multiple assets at one go by creating a multi-asset onboarding playbook.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a multi-asset onboarding process

Onboard multiple assets at one go by creating a multi-asset onboarding playbook.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

An enterprise asset technician submits an onboarding order. As an enterprise asset manager, you can work on the Multi-asset onboarding task associated with the onboarding order using the Onboarding playbook.

You can perform inline editing directly in the playbook. This capability enables you to change a value in a record directly instead of opening the record and updating the values on the form.

To close an onboarding task, you should either complete or skip all the activities in the playbook.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Asset operations**.

2.  From the **Onboarding** list, select **Onboarding tasks**.

3.  Select the onboarding task record for which you want to create a multi-asset onboarding process.

4.  Select the **Onboarding playbook** tab.

    The Muti-asset onboarding playbook is displayed.

5.  Review or enter details in the **Review model details** lane.

6.  Select **Mark as complete** to proceed to the next lane.

    After you complete entering details in the Review model lane, all other review assets activities are unlocked.

7.  Continue to review or enter details in all the lanes until you reach the last lane \(Deployment\).

8.  Review and then complete or skip the **Deployment** activity.

    -   Create a deploy task.

        1.  In the **Location** field, select the location where you want to deploy the asset.

            **Note:** This field is required to deploy the asset.

        2.  In the **Assigned to** field, select the person to whom the asset should be assigned.

            **Note:** By default, this field is auto-populated with the value that you selected in the **Reserved for** field when you performed the **Review assets assignment** activity.

        3.  In the **Create deploy task** field, select **true**.
        4.  Select **Mark as complete**.
        Based on the value of the **com.sn\_eam.default\_deployment\_task** asset property set by your enterprise administrator, either of the following deploy tasks are created:

        -   If the value is set to **sn\_eam\_deploy\_asset\_task**, an Enterprise Deploy Asset task is created for each asset that should be deployed. The deploy tasks are listed in the **Deploy Asset task** tab.
        -   If the value is set to **wm\_task**, a Work order task is created for each asset that should be deployed. The deploy tasks are listed in the **Work Order Task** tab.
        In the deploy task that's created, the **Assignment group** and the **Assigned to** fields are auto-populated with the values that you selected in the **Support group** and **Supported by** fields when you performed the **Review assets management** activity.

        **Note:** You can assign a work order task only to the Enterprise Field Technicians support group.

    -   Skip the Deployment activity by selecting **Skip**.
    The asset technicians complete the deploy tasks assigned to them. For more information, see [Complete and close the Pick Up task for an enterprise asset](complete-pickup-task-work-order.md) and [Complete and close a work order for an enterprise asset](complete-eam-work-order.md).

9.  After all the lanes show a status of skipped or complete, select **Close Task** to complete the multi-asset onboarding process.

    Your assets are successfully onboarded. The onboarding task is completed and the request and requested item's state changes to **Closed Complete**.


