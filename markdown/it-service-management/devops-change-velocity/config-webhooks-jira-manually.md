---
title: Configure webhooks in Jira manually
description: Configure webhooks in your Jira Server or Jira Cloud instance to send sync notifications to the DevOps Change Velocity application.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Jira, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks in Jira manually

Configure webhooks in your Jira Server or Jira Cloud instance to send sync notifications to the DevOps Change Velocity application.

## Before you begin

Role required:

-   sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity.
-   Jira admin role in your Jira Server or Jira Cloud instance.

## About this task

If you have connected your Jira tool using OAuth 2.0 based authentication, the webhooks are created for the OAuth 2.0 integration app in Jira when you configure automatically, whereas if you have connected using basic authentication, the webhooks are created for all your projects in Jira. If you choose to configure the webhooks manually for a Jira tool created using OAuth 2.0 based authentication, a duplicate webhook may get created.

## Procedure

1.  In DevOps Change Velocity, in the Configure to send data playbook activity, select **Configure manually** when configuring the tool instance to send data.

    ![Jira webhook configuration.](../image/jira-plybk-05.png)

    **Note:** You can also access manual configuration from the Jira tool record in DevOps Change Velocity. From the tool record, select **Configure** &gt; **Configure manually**.

2.  Copy the **Webhook URL** field from the ServiceNow instance connection details for Jira.

    **Note:** Select **Copy** in the appropriate field to copy the value to your clipboard. The field label changes to **Copied**, but you can copy multiple times.

    ![Jira configure webhooks manually.](../image/jira-manual-webhooks-2.png)

3.  Navigate to:

    -   For Jira Server navigate to **Administration** &gt; **System** &gt; **WebHooks**.
    -   For Jira Cloud instance, navigate to **Settings** &gt; **System** &gt; **WebHooks**.
4.  Select **Create a WebHook**.

5.  Enter the details for the webhook.

<table id="table_hlj_qrk_w1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the webhook.

</td></tr><tr><td>

Status

</td><td>

Select **Enabled**.

</td></tr><tr><td>

URL

</td><td>

Paste the Webhook URL copied from DevOps Change Velocity.-   Modify the copied webhook URL to reflect the code capability. For example, `https://<your_instance>.service-now.com/api/sn_devops/v2/devops/tool/code?toolId=<your_toolID>?ni.nolog.token=<Secure Token>`
-   Append the token to the end of the webhook URL.


</td></tr><tr><td>

Events

</td><td>

Select the events to be tracked.For example:

![Events for tracking.](../image/jira-manual-webhooks-1.png)

</td></tr></tbody>
</table>6.  Select **Create**.

    If you want to test the webhook, see the section on Jira in [Test webhooks manually](../reference/test-wehooks-manually.md).


**Parent Topic:**[Jira integration with DevOps Change Velocity](../concept/jira-integration-dev-ops.md)

