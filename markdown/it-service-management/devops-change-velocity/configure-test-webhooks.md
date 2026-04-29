---
title: Configure and test webhooks
description: Manually configure webhooks in Azure DevOps and test them.Configure webhooks in Azure DevOps to send sync notifications to the DevOps Change Velocity application.You can manually test if webhooks are configured correctly directly from Azure DevOps for each project.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure and test webhooks

Manually configure webhooks in Azure DevOps and test them.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](azure-devops-integration-dev-ops.md)

## Configure webhooks in Azure DevOps manually

Configure webhooks in Azure DevOps to send sync notifications to the DevOps Change Velocity application.

### Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity, Azure DevOps admin

### About this task

You can also access manual configuration from the Azure DevOps tool record in DevOps Change Velocity.

### Procedure

1.  In Azure DevOps, open the project for which you are configuring webhooks.

2.  Navigate to **Settings** &gt; **Service Hooks** and create a NEW SERVICE HOOKS SUBSCRIPTION, in Azure DevOps.

3.  In DevOps Change Velocity, choose **Configure manually** when configuring the tool instance to send data.

    ![Azure DevOps configuring tool](../image/azure-plybk-13.png)

4.  In DevOps Change Velocity, copy the **Webhook URL** field from the ServiceNow instance connection details for Azure DevOps.

    **Note:** Select **Copy** in the appropriate field to copy the value to your clipboard. The field label changes to **Copied**, but you can copy multiple times.

    ![Azure DevOps configure webhooks manually](../image/azure-manual-webhooks-3.png)

5.  Modify the copied Webhook URL to reflect your tool details, and paste the URL in Azure DevOps.

    For example:

    `https://myinstance.service-now.com/api/sn_devops/v2/devops/tool/{code | plan | artifact | orchestration | test | softwarequality }?toolId=23410545938c71d0db5bfe686cba1036&projectId=<project_sys_id>`

    1.  Select one of the tool capabilities `{code | plan | artifact | orchestration | test | softwarequality }` to match your tool.

        For example:

        `https://myinstance.service-now.com/api/sn_devops/v2/devops/tool/orchestration?toolId=23410545938c71d0db5bfe686cba1036&projectId=<project_sys_id>`

    2.  Replace `<project_sys_id>` with your Azure DevOps project ID in ServiceNow \(native\_id column in the sn\_devops\_project table\).

    3.  Copy the modified URL to the **URL** field of the NEW SERVICE HOOKS SUBSCRIPTION in Azure DevOps.

6.  In DevOps Change Velocity, copy the **Secret token** field from the ServiceNow instance connection details for Azure DevOps.

7.  In Azure DevOps, in **Header** field of the NEW SERVICE HOOKS SUBSCRIPTION, paste the copied **Secret token** in the correct format.

    1.  Use this format for the Azure DevOps **HTTP headers** field:

        "`token : <tokenValue>`"

    2.  Replace `<tokenValue>`, with the copied **Secret token** from the ServiceNow instance connection details for Azure DevOps.

<table id="table_ydl_d5n_dyb"><thead><tr><th>

From DevOps Change Velocity field

</th><th>

To Azure DevOps field

</th></tr></thead><tbody><tr><td>

Webhook URL \(modified\)

</td><td>

URL

</td></tr><tr><td>

Secret token

</td><td>

HTTP headers

 In the format:

 `token : <tokenValue>`

</td></tr></tbody>
</table>    ![Azure DevOps configure webhooks manually](../image/azure-manual-webhooks.png)


## Test webhooks in Azure DevOps

You can manually test if webhooks are configured correctly directly from Azure DevOps for each project.

### Before you begin

Role required: Azure DevOps admin privileges

### Procedure

1.  Navigate to Azure DevOps and select the project for which you want to test webhooks.

2.  Navigate to **Project settings** &gt; **Service hooks**.

    For each project, DevOps Change Velocity creates webhooks for these events:

    -   Build completed
    -   Code pushed
    -   Release created
    -   Release deployment completed
    -   Run stage state changed
    -   Work item created
    -   Work item deleted
    -   Work item restored
    -   Work item updated
3.  Select a webhook and select **Edit**.

4.  Select **Next** to see the URL and authentication details.

    ![Details of the configured webhook.](../image/azure-test-wh-01.png)

5.  To test the webhook, select **Test**.

    -   If the webhook is configured correctly, you’ll receive a **Succeeded** message.

        ![Success message when webhook is configured correctly.](../image/azure-test-wh-02.png)

    -   If the webhook is configured incorrectly, you’ll receive a **Failed** message.

        ![Failure message when webhook is configured correctly.](../image/azure-test-wh-03.png)

        To fix a webhook, you can try the following options:

        -   Reconfigure the webhooks by selecting **Configure** from the project record page in DevOps Change Velocity. This will reconfigure all the existing webhooks for the project.
        -   Verify if the **toolId** and **projectId** are correct in the **URL** field. You can find the correct values in the tool record page in DevOps Change Velocity.

            ![toolId and projectId in the URL.](../image/azure-test-wh-04.png)

        -   If you're using the integration user credentials for authentication, check if the credentials are correct in the **Basic authentication** username and password fields.

            ![Basic authentication fields in the webhook.](../image/azure-test-wh-05.png)

        -   If you're using the secret token for authentication, the token value is masked in the **Basic authentication password** field. You can replace the token in this field.

            ![Token in the webhook.](../image/azure-test-wh-06.png)


