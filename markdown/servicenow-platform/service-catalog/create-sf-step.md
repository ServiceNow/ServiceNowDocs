---
title: Define a service fulfillment step
description: Define how a catalog item request should be fulfilled by creating simple service fulfillment steps.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create a catalog item using a template, Creating or editing catalog item template, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a service fulfillment step

Define how a catalog item request should be fulfilled by creating simple service fulfillment steps.

## Before you begin

Role required: catalog\_builder\_editor or catalog\_admin or admin

## About this task

To configure fulfillment steps while creating a catalog item, associate it with a Workflow Studio flow that supports service fulfillment steps.

Fulfillment process can contain multiple steps. These steps can run sequentially or can be grouped to run in parallel.

The following video demonstrates how business owners can define the fulfillment process of catalog items using service fulfillment steps.

Demonstrates how business owners can define the fulfillment process of catalog items using service fulfillment steps.

## Procedure

1.  In the **Fulfillment** step of creating a catalog item, for the **Selected flow** field, select a flow that supports service fulfillment steps.

2.  In the **Steps** region, perform one of the following:

    1.  To create a task, click **Add task**.

        1.  On the form, fill in the fields.

<table id="table_zrr_czd_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Task

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task. It appears in the **Steps** region.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Assignment group

</td><td>

User group that the task should be assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User for which the task is assigned.

</td></tr><tr><td>

Priority

</td><td>

Priority of the task.

</td></tr><tr><td colspan="2">

When to run

</td></tr><tr><td>

Sequence

</td><td>

Sequence of this step relative to the previous step. Possible options are:

-   With previous step: This step is grouped with the previous step or group. All grouped steps run simultaneously.
-   After previous step: This step is placed after the previous step
**Note:** This field is not editable if it is the first step.

</td></tr><tr><td>

Condition

</td><td>

Condition that defines whether the step must run. The options on which a condition can be applied are the questions that are available on the catalog item for which you’re creating the service fulfillment steps. For information on questions, see the [Create a catalog item using a template](create-item-cat-builder.md) topic.

</td></tr></tbody>
</table>        2.  Click **Add**.
    2.  To create a custom approval and define who can approve the step, perform the following:

        1.  From the list beside **Add task**, click **Custom approval**.
        2.  On the form, fill in the fields.

<table id="table_bcx_4yd_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Custom approval

</td></tr><tr><td>

Users

</td><td>

Users that can approve this step.

</td></tr><tr><td>

Groups

</td><td>

User groups that can approve this step.

</td></tr><tr><td>

Approval type

</td><td>

Type of the required approval.-   All approve: The step is approved only when all assigned users and user groups approve.
-   Anyone approves: The step is approved when any of the assigned users or any user from the assigned user groups approve.


</td></tr><tr><td colspan="2">

When to run

</td></tr><tr><td>

Sequence

</td><td>

Sequence of this step relative to the previous step. Possible options are:

-   With previous step: This step is grouped with the previous step or group. All grouped steps run simultaneously.
-   After previous step: This step is placed after the previous step
**Note:** This field is not editable if it is the first step.

</td></tr><tr><td>

Condition

</td><td>

Condition that defines whether the step must run. The options on which a condition can be applied are the questions that are available on the catalog item for which you’re creating the service fulfillment steps. For information on questions, see the [Create a catalog item using a template](create-item-cat-builder.md) topic.

</td></tr></tbody>
</table>        3.  Click **Add**.
    3.  To create a manager approval and define who can approve this step, perform the following:

        1.  From the list beside **Add task**, click **Manager approval**.
        2.  On the form, fill in the fields.

<table id="table_sls_g4r_xqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

When to run

</td></tr><tr><td>

Sequence

</td><td>

Sequence of this step relative to the previous step. Possible options are:

-   With previous step: This step is grouped with the previous step or group. All grouped steps run simultaneously.
-   After previous step: This step is placed after the previous step
**Note:** This field is not editable if it is the first step.

</td></tr><tr><td>

Condition

</td><td>

Condition that defines whether the step must run. The options on which a condition can be applied are the questions that are available on the catalog item for which you’re creating the service fulfillment steps. For information on questions, see the [Create a catalog item using a template](create-item-cat-builder.md) topic.

</td></tr></tbody>
</table>        3.  Click **Add**.
    ![Service fulfillment steps.](../image/sfs-steps.png "Service fulfillment steps")

3.  In the **Estimated time to deliver** region, for the **Days** field, specify the time by which the RITM should be fulfilled.

    The due date is calculated based on when the service fulfillment flow is triggered.

4.  To edit a step, click the edit icon \(![Edit icon.](../image/edit-quest-builder.png)\).

5.  To delete a step, click the delete icon \(![Delete icon.](../image/deactivate-quest.png)\).

6.  To rearrange steps, drag the steps.

7.  To group steps together, perform one of the following tasks.

    -   Drag a step and drop it on another step or group of steps.
    -   To group this step with the previous step or group, click the merge icon \(![Merge icon.](../image/merge.png)\).
    ![Merged service fulfillment steps.](../image/merge-steps.png "Merged service fulfillment steps")

8.  To separate a step from a group of steps, perform one of the following tasks.

    -   Click the separate icon \(![Separate icon.](../image/separate.png)\). The step is placed after the group.
    -   Drag a step out of the group and drop it at a location of your choice.

**Parent Topic:**[Create a catalog item using a template](create-item-cat-builder.md)

