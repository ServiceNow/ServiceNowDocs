---
title: Configure webhooks in GitLab manually
description: Configure webhooks in GitLab manually to send job, push, and issues notifications to the DevOps application.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks in GitLab manually

Configure webhooks in GitLab manually to send job, push, and issues notifications to the DevOps application.

## Before you begin

Role required:

-   sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity
-   Maintainer \(or higher\) for the GitLab projects.

## About this task

Create webhooks for the following two triggers in GitLab for every project you want to track.

-   Push events \(code capability\)
-   Job events \(orchestration capability\)
-   Issues events \(planning capability\)

You can also access manual configuration from the GitLab tool record in DevOps Change Velocity.

## Procedure

1.  In GitLab, navigate to **Project** &gt; **Settings** &gt; **Webhooks** and add a webhook.

2.  In DevOps Change Velocity, choose **Configure manually** when configuring the tool instance to send data.

    ![GitLab configure webhooks manually.](../image/gitlab-connect-workspace-4.png)

    **Note:** You can also access manual configuration from the GitLab tool record in DevOps Change Velocity. From the tool record, select **Configure** &gt; **Configure manually**.

3.  Copy the **Webhook URL** field from DevOps Change Velocity connection details for GitLab.

    **Note:** Select **Copy** in the appropriate field to copy the value to your clipboard. The field label changes to **Copied**, but you can copy multiple times.

    ![Copy webhook details.](../image/gitlab-manual-webhooks-4.png)

4.  Modify the copied Webhook URL to reflect your tool details, and paste the URL in GitLab.

    For example:

    `https://<your instance>.service-now.com/api/sn_devops/v2/devops/tool/{code | plan | artifact | orchestration | test | softwarequality }?toolId=<your ToolId>`

    1.  Select one of the tool capabilities `{code | plan | artifact | orchestration | test | softwarequality }` to match your tool.

        For example:

        `https://<your instance>.service-now.com/api/sn_devops/v2/devops/tool/code?toolId=<your ToolId>`

    2.  Copy the modified Webhook URL to the **URL** field of the new webhook in your GitLab instance.

5.  Copy the **Secret token** field from the ServiceNow instance connection details for GitLab, and paste in the **Secret Token** field of the new webhook in your GitLab instance.

    |From DevOps Change Velocity|To GitLab|
    |---------------------------|---------|
    |Webhook URL \(modified\)|URL|
    |Secret token|Secret Token|

6.  Select the check boxes for **Push events**, **Tag push events**, **Comments**, and **Merge request events** for coding capability events.

    ![GitLab push events for code capability.](../image/gitlab-manual-webhooks-5.png)

7.  Select **Add webhook**.

8.  Repeat the procedure to create webhooks for planning and orchestration capability events in GitLab.

    -   For orchestration: Select the check boxes for **Job events** and **Pipeline events**. ![GitLab Job events.](../image/gitlab-manual-webhooks-6.png)
    -   For planning: Select the check boxes for **Issues events** and **Confidential issues events**. ![GitLab Issues events](../image/gitlab-issues-events.png)
9.  Select **Add webhook**.

    GitLab webhooks for DevOps Change Velocity integration:

    ![Webhooks configured in GitLab.](../image/gitlab-manual-webhooks-3.png)


**Parent Topic:**[GitLab integration with DevOps Change Velocity](../concept/gitlab-integration-dev-ops.md)

