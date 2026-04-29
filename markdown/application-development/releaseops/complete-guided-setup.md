---
title: Complete ReleaseOps guided setup
description: Starting with version 1.2.1 of ReleaseOps, guided setup helps to make the initial configuration of ReleaseOps easier. Follow the steps in guided setup to begin using ReleaseOps quickly.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [large scale deployment ServiceNow, ReleaseOps guided setup]
breadcrumb: [Configure, ReleaseOps, Deploying applications, Building applications]
---

# Complete ReleaseOps guided setup

Starting with version 1.2.1 of ReleaseOps, guided setup helps to make the initial configuration of ReleaseOps easier. Follow the steps in guided setup to begin using ReleaseOps quickly.

## About this task

For more complex setup scenarios, or when making changes to your existing ReleaseOps ecosystem, use the procedure outlined in [ReleaseOps manual setup](configure-new-releaseops-ecosystem.md).

When completing guided setup, you define several kinds of instances for your ReleaseOps pipeline. To learn more about each instance, see [Instances in ReleaseOps configuration](../concept/instances-in-releaseops-configuration.md).

## Before you begin

Role required: admin or sn\_releaseops.releaseops\_pipeline\_admin

## Procedure

1.  Navigate to **All** &gt; **ReleaseOps** &gt; **ReleaseOps Guided Setup**.

2.  Select the instances that you want to participate in your ReleaseOps pipeline.

    1.  In the **Select instances to configure** card, select **Start**.

    2.  For each instance that you want to participate in your ReleaseOps pipeline, select the check box next to the instance name.

        **Important:** You must select your controller instance and at least once instance with an **Instance type** of "Test" when selecting instances for your pipeline. For more information about instances, see [Instances in ReleaseOps configuration](../concept/instances-in-releaseops-configuration.md).

        ![Select each instance that you want to participate in your ReleaseOps pipeline by selecting the check box next to the instance name.](../image/releaseops-select-instances-for-setup.png)

    3.  Select **Select these instances**.

    4.  To remove a selected instance from your pipeline, select the check box next to the instance name, then select **Deselect these instances**.

    5.  Verify that the **Instance type** for each instance is correct.

    6.  To change an instance type, double-click \(or use the keyboard shortcut\) in the **Instance type** field, select the correct instance type from the list, then select the save icon \(![](../../creator-studio/image/crs-save-check.png)\).

    7.  When finished, select **Mark as complete**.

3.  Add the instances in your ReleaseOps pipeline as managed instances.

    1.  Select **Add managed instances**.

    2.  In the **Add managed instances** modal, select the instances that you selected in step 2.

        To select more than one instance from the list, use the keyboard shortcut to select multiple instances.

    3.  Select **Send requests**.

        ![Select the instances that you want to add as managed instances, then select Send requests.](../image/releaseops-add-managed-instances.png)

        Approval requests are sent to each instance that you added as a managed instance.

    4.  Select **Mark as complete**.

        Once you have added managed instances and sent approval requests to each instance, ReleaseOps validates each instance in the background. Validation might take several minutes. Once validation is complete, you can proceed to the next step of guided setup.

4.  Approve the management requests for each managed instance in your pipeline.

    **Note:** You must be an admin to approve instance management.

    1.  Select the link to the approval request for each managed instance in your pipeline.

    2.  If you aren't logged in to your managed instance, log in with your credentials.

    3.  On the approval request record, select **Approve Manager Instance**.

    4.  Return to your guided setup window.

    5.  Select **Mark as complete**.

        Once you have approved the management requests for each managed instance in your pipeline, ReleaseOps validates the approvals in the background. Validation might take several minutes. Once validation is complete, you can proceed to the next step of guided setup.

5.  Review the deployment instances for each instance that participates in your ReleaseOps pipeline by selecting **Deployment instance records** in the side panel.

    During guided setup, ReleaseOps automatically creates deployment instances for each instance that you added in step 2.

    ![Select Deployment instance records in the side panel to see the deployments instance records that have been created.](../image/releaseops-deployment-instance-records.png)

6.  Create or verify the remote instances for each instance in your pipeline.

    **Note:** You must be an admin or an update set admin to view or create remote instance records.

    ![Create or verify remote instances to enable the transfer of update sets between instances in your pipeline.](../image/releaseops-remote-instances.png)

    -   If you already have remote instances set up, select **Check the remote instance record** for the existing remote instance. You might be prompted to log in to the instance with your credentials, if you aren't already logged in. Once logged in, the remote instance record displays.
    -   If you don’t have remote instances set up, select **Create a new remote instance record** for the remote instance that you need to create. You might be prompted to log in to the instance with your credentials, if you aren't already logged in. Once logged in, a new remote instance record appears. You must complete the fields in the record and select **Test connection** to verify that the remote instance is accessible. Select **Submit** once the remote instance test is successful.
    1.  Once you have created or verified the remote instances for each instance in your pipeline, return to your guided setup window and select **Mark as complete**.

7.  Review the pipeline instances for each instance that participates in your ReleaseOps pipeline by selecting **Pipeline instance records** in the side panel.

8.  Set the controller property on the development instance.

    **Note:** You must be an admin to edit the controller property.

    1.  Select the link to open your development instance.

    2.  If you aren't already logged in, log in with your credentials.

    3.  In the **Value** field, enter the URL for your controller instance.

        ![Set the deployment controller property on the development instance.](../image/releaseops-set-controller-property.png)

    4.  Save the record by selecting **Update**.

    5.  Return to your guided setup window.

    6.  Select **Mark as complete**.

9.  Select **Close**.


## Result

You have completed guided setup for ReleaseOps. You can start using ReleaseOps to manage your deployments. For more information, see [Using ReleaseOps to manage deployments](../concept/using-releaseops-to-manage-deployments.md).

