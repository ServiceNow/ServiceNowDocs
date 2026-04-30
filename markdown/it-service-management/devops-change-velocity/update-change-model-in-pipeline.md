---
title: Update change model in pipeline
description: Update the change model in your existing pipeline steps using the DevOps Pipeline Migration to Change Models catalog item.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [DevOps change models, Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Update change model in pipeline

Update the change model in your existing pipeline steps using the DevOps Pipeline Migration to Change Models catalog item.

## Before you begin

Role required:

-   sn\_change\_read role to read the change model from the chg\_model table.
-   sn\_devops.viewer role to read the pipelines from the sn\_devops\_pipeline table.

## About this task

If you’re an upgrading user, and you want to migrate your existing pipelines steps to change models, you must perform this procedure.

The DevOps Pipeline Migration to Change Models catalog item enables you to update the change model in each step record in your pipeline at once. For example if you have set the type compatibility `com.snc.change_management.change_model.type_compatibility`  property to false and change model input is required in multiple pipeline steps, you can use this catalog item to update the change model for all pipeline steps in one go.

## Procedure

1.  Navigate to  **All &gt; Service Catalog &gt; Catalog Definitions &gt; Maintain Items &gt; DevOps Pipeline Migration to Change Models**, and set the  **Active**  state to  **True**  to activate the  **DevOps Pipeline Migration to Change Models** maintain item.

    By default the catalog item is turned off.

2.  In the Available For related list of the catalog item, add the users to whom the catalog must be available.

3.  In the Approve By related list of the catalog item, add the users who can approve the catalog item.

    Alternatively, navigate to  **All &gt; Flow Designer &gt; Flows**, and activate the  **Request for pipeline migration** catalog flow. You can update the rule set in the  **Ask For Approval ** action of the flow to add a user or a group of users who can approve the catalog item.

4.  To add the catalog item in the Service Catalog categories in Service Portal, set the category of these items to  **DevOps**  and add the  **Service Catalog**  catalog.

    If the  DevOps  category isn’t available, you must create a new category called  **DevOps**  from the catalog item record itself and assign the  **DevOps Onboarding ** catalog to it.

5.  To add catalog item in Employee Service Center, add a new topic in the  Assigned Topics  related list with taxonomy as  **Employee**  in the  **IT &gt; IT for IT ** section.

    The Assigned Topics related list isn’t available in the Default view of the **Catalog Item** form. To add it, select  **Additional icons &gt; Configure &gt; Related Lists ** and move the ** Connected Content → Catalog item**   field to the selected section.

6.  Navigate to  **All  &gt;  Service Catalog  &gt;  Catalog Definitions  &gt;  Maintain Items**  and search for **DevOps**.

    **Note:** You can also access the service catalog from the  Employee Center  or Service portal.

7.  From the DevOps catalog items, select **DevOps Pipeline Migration to Change Models**.

    ![Catalog item to migrate DevOps pipeline to change model](../image/change-model-migration.png)

8.  In the form, fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Tool|Orchestration tool that contains the required pipelines.|
    |Pipeline|Pipelines for which you want to update the change model.|
    |Change model|Change model to which the existing models are being updated.|

9.  Select **Submit**.

    A request is created. Based on whether the request is approved or rejected, notifications are send to the requester.

    **Note:** If any of the pipelines you selected in step 8 has any data policy, which doesn’t allow the pipeline steps to be updated, the same is updated as an error in the worknotes of the corresponding request.

<table id="choicetable_vjt_yl1_yyb"><tbody><tr><td id="d129580e271">

**Approved and successful**

</td><td>

-   A comment is added in the request record specifying that migration to change model was successful. ![Migration successful comment in request record](../image/change-model-migration-success-comment.png)
-   A bell notification is sent to the requester specifying that the migration has been successful. ![Migration successful bell notification](../image/change-model-success-1.png)
-   An email notification is sent to the requester specifying that the migration request has been successful. ![Migration successful email notification](../image/change-model-migration-success-email.png)


</td></tr><tr><td id="d129580e307">

**Rejected and unsuccessful**

</td><td>

-   A comment is added in the request record specifying that migration wasn’t successful. ![Rejection comment in request record](../image/change-migration-req-reject.png)
-   A bell notification is sent to the requester specifying that the migration request has been rejected. ![Rejection bell notification](../image/change-migration-bell-notification-reject.png)
-   An email notification is sent to the requester specifying that the migration request has been rejected. ![Email notification.](../image/change-model-migration-unsuccessful-mail.png)


</td></tr></tbody>
</table>
**Parent Topic:**[DevOps change models](../concept/devops-change-multimodel.md)

