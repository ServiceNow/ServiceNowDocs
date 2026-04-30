---
title: Set up triggers for the Microsoft Azure DevOps Boards spoke
description: Set up triggers for the Microsoft Azure DevOps spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.Configure endpoint for webhooks in Microsoft Azure DevOps that support the token authentication.Create and configure a service webhook in Microsoft Azure Devops for Microsoft Azure DevOps Boards spoke.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-09-03"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure DevOps Boards Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up triggers for the Microsoft Azure DevOps Boards spoke

Set up triggers for the Microsoft Azure DevOps spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.

## Before you begin

Role required: admin

## Configure triggers in ServiceNow instance

Configure endpoint for webhooks in Microsoft Azure DevOps that support the token authentication.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Toggle and enable the **Inbound** connections.

4.  Locate the **Microsoft Azure DevOps Boards Spoke** endpoint and click **View Details**.![Microsoft Azure Devops Board spoke inbound connection for external triggers.](../image/ms-azure-devops-boards-inbound-conn.jpg)

5.  For the **Microsoft Azure DevOps Boards External Trigger** end point, click **Configure**.![Configure Microsoft Azure Devops Boards External Trigger connection.](../image/ms-azure-devops-board-ext-trigr-config.jpg)

6.  Select the user who can trigger the endpoint and click **Activate**.![Configure endpoint for Microsoft Azure Devops Boards External Trigger.](../image/ms-azure-devops-boards-ext-trgr-actvt.jpg)

    Copy and store the generated token, URL, and header parameter name for further use.![Copy the generated token,URL, and header parameter name for external trigger.](../image/ms-azure-devops-board-token-url-header.jpg)


## Create a service hook subscription for Microsoft Azure DevOps Boards spoke

Create and configure a service webhook in Microsoft Azure Devops for Microsoft Azure DevOps Boards spoke.

### Before you begin

-   Role required: admin
-   [Configure triggers in ServiceNow instance](setup-external-trigger-ms-azure-devops-board-spoke.md#)

### Procedure

1.  In your Azure DevOps project, navigate to **Project settings** &gt; **Service hooks** at https://&lt;organization-name&gt;/&lt;project-name&gt;/\_settings/serviceHooks.

2.  On the Service Hooks page, select the **+** icon or **Create subscription**.

3.  On the Service screen, select **Web Hooks** and then select **Next**.![Creating a service webhook for external triggers.](../image/ms-azure-devops-board-config-azure-webhook.jpg)

4.  From the **Trigger on this type of event** list, select a supported Azure Devops event and click **Next**.

    For example, select **Work item restored**.![Configuring a trigger in the webhook.](../image/ms-azure-devops-board-webhook-trigger.jpg)

5.  On the NEW SERVICE HOOKS SUBSCRIPTION form, fill in the fields for an action.

<table id="table_d4h_4yt_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

URL

</td><td>

URL generated while configuring triggers in ServiceNow instance in the URL field.

</td></tr><tr><td>

HTTP headers

</td><td>

Key-value pair of header parameter and token generated in this format: `azure-devops-board-token: <token-value>`

</td></tr><tr><td>

RESOURCE VERSION

</td><td>

Select \[Latest\].

</td></tr></tbody>
</table>    ![Configuring settings in the webhook for external triggers.](../image/ms-azure-devops-boards-webhook-action.jpg)

6.  Click **Finish**.

7.  Repeat the steps 2 through step 6 for the following supported event triggers:

    -   Work item commented on
    -   Work item created
    -   Work item deleted
    -   Work item restored
    -   Work item updated

### Result

Now you can create a flow and start using the supported trigger events in the flow.

