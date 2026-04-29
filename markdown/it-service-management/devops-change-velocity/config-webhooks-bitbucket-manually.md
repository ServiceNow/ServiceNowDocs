---
title: Configure webhooks in Bitbucket manually
description: Configure webhooks in Bitbucket to send sync notifications to the DevOps Change Velocity application.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Bitbucket, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks in Bitbucket manually

Configure webhooks in Bitbucket to send sync notifications to the DevOps Change Velocity application.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity, Bitbucket admin

## About this task

You can also access manual configuration from the Bitbucket tool record in DevOps Change Velocity.

## Procedure

1.  In Bitbucket, navigate to **Settings** &gt; **Webhooks** for the specified repo, and add a webhook.

2.  In DevOps Change Velocity, choose **Configure manually** when configuring the tool instance to send data.

    ![Bitbucket configure manually](../image/bitbucket-workspace-connect-4.png)

3.  In DevOps Change Velocity, copy the **Webhook URL** field from the ServiceNow instance connection details for Bitbucket.

    **Note:** Select **Copy** in the appropriate field to copy the value to your clipboard. The field label changes to **Copied**, but you can copy multiple times.

    ![Bitbucket configure webhooks manually](../image/bitbucket-manual-webhooks-2.png)

4.  In Bitbucket, navigate to **Repository settings &gt; Webhooks &gt; Edit webhook**, and paste the copied Webhook URL in the **URL** field.

5.  Select the following triggers.

    -   Repository: Push
    -   Pull request: Created, Updated, Approved, Approval removed, Changes Request created, Changes Request removed,Merged, Declined, Comment created, Comment updated, Comment deleted, Comment resolved, Comment reopened.
    ![Configure webhooks manually in Bitbucket Cloud](../image/bitbucket-manual-webhook-4.png)

6.  Select **Save**.


**Parent Topic:**[Bitbucket integration with DevOps Change Velocity](../concept/bitbucket-integration-dev-ops.md)

