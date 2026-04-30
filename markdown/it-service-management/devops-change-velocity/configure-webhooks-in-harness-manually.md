---
title: Configure webhooks in Harness manually
description: Configure webhooks manually in Harness to send pipeline notifications to DevOps Change Velocity.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Harness, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks in Harness manually

Configure webhooks manually in Harness to send pipeline notifications to DevOps Change Velocity.

## Before you begin

Role required:

-   sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity
-   Harness admin

## Procedure

1.  In DevOps Change Velocity, choose **Configure manually** when configuring the tool instance to send data.

    **Note:** You can also access manual configuration from the Harness tool record in DevOps Change Velocity. From the tool record, select **Configure manually**.

2.  Copy the **Webhook URL** and the other field values from DevOps Change Velocity connection details for Harness.

    **Note:** Select **Copy** in the appropriate field to copy the value to your clipboard. The field label changes to **Copied**, but you can copy multiple times.

    ![Configure webhooks manually screen](../image/harness-workspace-3.png)

3.  Modify the copied Webhook URL to reflect your tool details.

    `https://<your instance>.service-now.com/api/sn_devops/v2/devops/tool/{code | plan | artifact | orchestration | test | softwarequality }?toolId=<your ToolId>`

    1.  In &lt;your instance&gt;, enter the copied ServiceNow instance URL.

    2.  Select one of the tool capabilities `{code | plan | artifact | orchestration | test | softwarequality }` to match your tool.

        For example:

        `https://demoinstance.service-now.com/api/sn_devops/v2/devops/tool/orchestration?toolId=<your ToolId>`

    3.  In &lt;your ToolId&gt;, enter the copied tool ID.

        For example:

        `https://demoinstance.service-now.com/api/sn_devops/v2/devops/tool/orchestration?toolId=ac0cif1a1b7696107940a864gjhgbcb58`

    4.  Add the "&amp;ni.nolog.token=&lt;copied secret token&gt;" parameter in the URL to pass the secret token.

        For example:

        `https://demoinstance.service-now.com/api/sn_devops/v2/devops/tool/orchestration?toolId=ac0cdf1a1b7696107940a864gjhgbcb58&ni.nolog.token=brl1jhab63nn56`

    5.  Add "&amp;projectId=&lt;project\_sys\_id&gt;" in the URL to add the account identifier.

        **Note:** Project Id or Account Id is the unique identifier for your account in the Harness platform. Copy it from Account Settings of your Harness account.

        For example:

        `https://demoinstance.service-now.com/api/sn_devops/v2/devops/tool/orchestration?toolId=ac0cdf1a1b7696107940a864gjhgbcb58&ni.nolog.token=brl1jhab63nn56&projectId=vH2s1ghNKNy6sEVSeTIK3w`

4.  In your Harness tool, select your pipeline, and then select the **Notify** option. ![Notify option in Harness pipeline](../image/harness-configure-1.png)

5.  Select **+Notifications** to create a new notification record.

6.  Enter a name for the notification, and select **Continue**. ![Create new notification in Harness](../image/harness-configure-2.png)

7.  Select the following pipeline events, and then select **Continue**. ![Select events for Harness notification](../image/harness-configure-3.png)

    -   Pipeline End
    -   Stage Failed
    -   Stage Success
    -   Stage Start
    -   Step Failed
8.  Select the channel type as **Webhook**, and enter the URL to be configured \(created in step3\). ![Select channel type and URL to be configured](../image/harness-configure-4.png)

9.  Select **Finish**.


**Parent Topic:**[Harness integration with DevOps Change Velocity](../concept/harness-integration-with-devops-change-velocity.md)

