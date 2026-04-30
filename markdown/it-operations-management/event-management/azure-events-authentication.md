---
title: Integrate Azure Monitor with OAuth authentication
description: Integrate Microsoft Azure with Event Management by authenticating Azure V1 or V2 tokens in the Azure Monitor.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integrate Azure Monitor as an authenticated data source, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Integrate Azure Monitor with OAuth authentication

Integrate Microsoft Azure with Event Management by authenticating Azure V1 or V2 tokens in the Azure Monitor.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

On the Azure portal, alert correlation rules are defined through the **Correlate alerts** setting within Alert Processing Rules. When **Correlate alerts** is assigned on the Azure portal, the Azure Monitor alerts received on the ServiceNow® instance within 60 minutes are grouped using tag based alert clustering.

Roles required: evt\_mgmt\_admin, web\_service\_admin, and oauth\_admin

## About this task

Configure the Event Management environment for the collection of events from Azure Monitor. In your Azure Monitor portal, set your ServiceNow AI Platform instance as the rest endpoint using V1 or V2 tokens.

## Procedure

1.  In the Azure Monitor portal:

    1.  Perform app registration and expose an API.

        For more information about registering an app and exposing an API in Azure, see [https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-expose-web-apis](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-expose-web-apis).

    2.  Create an action group with a secure webhook, and provide the rest endpoint as `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=azuremonitor`.

        **Note:** For servicenowservices.com instances, the rest endpoint has to be `https://<instance-name>.servicenowservices.com/api/sn_em_connector/em/inbound_event?source=azuremonitor`

        For more information about adding a secure webhook to an action group, see [https://docs.microsoft.com/en-us/azure/azure-monitor/platform/action-groups](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/action-groups).

    3.  Navigate to **Alerts** &gt; **Manage Alert Rules**.

    4.  In the Secure Webhook section, make sure that **Yes** is selected for the **Enable the common alert schema** option.

    5.  Add the action group with the secure webhook to an alert rule.

2.  In the Azure Monitor portal, verify which Azure token is in use by your registered application.

    1.  Navigate to **App Registration**, and select the registered application.

    2.  In the Manage section, click **Manifest**.

    3.  In the editor screen, select the **Microsoft Graph App Manifest** tab and locate the **requestedAccessTokenVersion** parameter or select the **AAD Graph App Manifest** tab and locate the **accessTokenAcceptedVersion** parameter.

        If the value of **requestedAccessTokenVersion** or **accessTokenAcceptedVersion** is **2**, the integration must use V2 tokens.

        If the value of **requestedAccessTokenVersion** or **accessTokenAcceptedVersion** is **1** or **null**, the integration must use V1 tokens.

3.  In your ServiceNow AI Platform instance, ensure that the ServiceNow user is assigned with the correct Application \(client\) ID or Application ID URI.

    Also ensure the relevant ServiceNow sys\_user is assigned the evt\_mgmt\_integration role.

    1.  Navigate to **System Security** &gt; **Users and groups** &gt; **Users**.

        **Note:** To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    2.  Verify that the **Source** field for the ServiceNow sys\_user is populated with the correct Application \(client\) ID or Application ID URI, as defined in the Azure Monitor portal.

        If the application is using an Azure V1 token, the **Source** field must be populated with the Application ID URI of the registered application. If the application is using an Azure V2 token, the **Source** field must be populated with the Application \(client\) ID of the registered application.

        If the **Source** field is not displayed, change the form layout to display this field. Click the context menu icon \(![Context menu icon](../image/context-menu-icon.png)\) and select **Configure &gt; Form Layout**. Move **Source** to the Selected list.

        **Note:** If your ServiceNow AI Platform instance version is earlier than Paris Patch 2 or Orlando Patch 9, the **Source** field value must be enclosed in square brackets. For example, `[api://azuretest]`.

4.  In your ServiceNow AI Platform instance, navigate to **Event Management** &gt; **Integrations** &gt; **Azure OAuth Config**.

5.  Click **Azure OAuth OIDC Entry** and enter the `Client ID`.

    If the registered application is using an Azure V2 token, the `Client ID` should be the same as the `Application (client) ID` of the app registrations defined in your Azure Monitor portal.

    If the registered application is using an Azure V1 token, the `Client ID` should be the same as the `Application ID URI` of the app registrations defined in your Azure Monitor portal \(the exposed API\).

6.  In the **OAuth OIDC Provider Configuration** field, click the info icon \(![Info icon](../image/info.png)\).

7.  In the OIDC Provider Configuration window, click **Open Record**.

    ![OIDC Provider Configuration window](../image/em-azure-authentication.png)

8.  Enter the `OIDC Metadata URL` according to the Azure token used by the registered application, as shown in the following table.

<table id="choicetable_rbx_wgs_ymb"><thead><tr><th align="left" id="d139803e469">

Azure token

</th><th align="left" id="d139803e472">

OIDC Metadata URL

</th></tr></thead><tbody><tr><td id="d139803e478">

**V2**

</td><td>

In the OIDC Provider Configuration form, add the following URL to the **OIDC Metadata URL** field:`https://login.microsoftonline.com/<tenant-id>/v2.0/.well-known/openid-configuration`

 Ensure that `<tenant-id>` is replaced with the correct Azure Tenant ID.

 **Note:** If attempting to integrate Azure Gov Cloud with the ServiceNow Azure Monitor Connector, remember to change the claim value to `f1f34126-d4ef-40e1-ad4b-bf5d47b4860d`.

</td></tr><tr><td id="d139803e505">

**V1**

</td><td>

In the OIDC Provider Configuration form:-   In the Claim Name column, change `azp` to `appid`.

![Change AZP to APPID](../image/em-azp.png)

**Note:** If attempting to integrate Azure Gov Cloud with the ServiceNow Azure Monitor Connector, remember to change the claim value to `f1f34126-d4ef-40e1-ad4b-bf5d47b4860d`.

-   In the **OIDC Metadata URL** field, add the following URL: `https://login.microsoftonline.com/<tenant-id>/.well-known/openid-configuration`

Ensure that `<tenant-id>` is replaced with the correct Azure Tenant ID.

</td></tr></tbody>
</table>
## Result

When an alert is created in Azure Monitor as part of the alert rule, the notification is sent to the ServiceNow AI Platform using the secure webhook endpoint. In your ServiceNow AI Platform instance, navigate to **All Events** to see the events. If you want to send alert state changes on the ServiceNow instance from the ServiceNow alerts to the Azure Portal, you need to enable the Azure Monitor Bi-directional connector. For more information, see [Configure Azure Monitor Bi-directional connector](configure-azure-bi-directional-connector.md).

**Parent Topic:**[Integrate Azure Monitor as an authenticated data source](../concept/azure-integration.md)

