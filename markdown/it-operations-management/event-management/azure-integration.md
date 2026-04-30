---
title: Integrate Azure Monitor as an authenticated data source
description: Integrate Microsoft Azure with Event Management by adding the Azure Monitor as an authenticated data source.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Integrate Azure Monitor as an authenticated data source

Integrate Microsoft Azure with Event Management by adding the Azure Monitor as an authenticated data source.

You can configure the Event Management environment for the collection of events from Azure Monitor by setting your ServiceNow AI Platform instance as the rest endpoint.

Once the endpoint is configured, when an Azure Monitor alert message arrives, Event Management:

-   Authenticates the Azure Monitor alert message with the relevant ServiceNow user, using OAuth configuration or a standard webhook.
-   Extracts information from the original Azure Monitor alert message to populate required event fields and inserts the event into the ServiceNow AI Platform database.
-   Captures specified content in the **Additional Information** field of the event form.

## What authentication is used

There are two methods of authentication:

-   OAuth authentication: Provides enterprise-grade authentication to keep your enterprise environment safe. Authentication is performed using Azure Monitor V1 or V2 access tokens. For more information, see [Integrate Azure Monitor with OAuth authentication](../task/azure-events-authentication.md).
-   Basic webhook authentication: Provides a basic standard of authentication, without the need for Azure Active Directory. This authentication can be especially useful for distributed small teams, such as SRE or DevOps teams. For more information, see [Integrate Azure Monitor with basic authentication](../task/azure-events-webhook.md).

## What to know before you begin

You can use your integrated Azure Monitor as a data source only after you have verified the following:

-   For both methods of authentication, the relevant ServiceNow sys\_user is assigned the evt\_mgmt\_integration role.
-   The Event Management Connectors plugin is installed in the ServiceNow AI Platform instance. You can download the plugin from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.
-   Azure Cloud Discovery must be performed to ensure that the created alerts are bound to the configuration items in the ServiceNow AI Platform. For more information, see [Azure Cloud Discovery](../../discovery/concept/azure-cloud-discovery.md).

## Event Rules and Event Field mappings

These event rules and event field mappings are provided with the base system:

|Module|Description|
|------|-----------|
|Event Rules|**Azure Monitor**: A general event rule to handle all Azure Monitor events.|
|Event Field Mappings|**Azure Monitor - ci\_type**: To map ci\_type of events based on resourceType field. A base set of mapping pairs are provided.|

These are the mappings provided with the base system in **Azure Monitor - ci\_type**:

![Azure Mapping Pairs](../image/Azure-base-mapping.png "Transform Value Pairs")

**Note:** You can add new mapping pairs to the Event Field Mapping - **Azure Monitor - ci\_type** as per the requirement, to map events to the respective ci\_type based on resourceType.

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

If you want to send alert state changes on the ServiceNow instance from the ServiceNow alerts to the Azure Portal, you need to enable the Azure Monitor Bi-directional connector. For more information, see [Configure Azure Monitor Bi-directional connector](../task/configure-azure-bi-directional-connector.md).

## Severity mapping from Azure severity to ServiceNow event severity

|Azure severity condition|ServiceNow event severity|
|------------------------|-------------------------|
|When an Azure alert monitorCondition is Fired|
|Azure Sev0|ServiceNow Critical \(severity "1"\)|
|Azure Sev1|ServiceNow Major \(severity "2"\)|
|Azure Sev2 and Sev3|ServiceNow Warning \(severity "4"\)|
|Azure Sev4|ServiceNow OK \(severity "5"\)|
|When an Azure alert monitorCondition is resolved|
|Any Azure severity|ServiceNow CLEAR \(severity "0"\)|

-   **[Integrate Azure Monitor with basic authentication](../task/azure-events-webhook.md)**  
Integrate Microsoft Azure with Event Management by adding a standard webhook in Azure Monitor.
-   **[Integrate Azure with REST API key token](../task/integrate-azure-api-key.md)**  
Integrate using an API key to establish secure communication and automate data exchange via REST API. This simplifies integration, enabling seamless access to services and enhancing operational efficiency.
-   **[Integrate Azure Monitor with OAuth authentication](../task/azure-events-authentication.md)**  
Integrate Microsoft Azure with Event Management by authenticating Azure V1 or V2 tokens in the Azure Monitor.
-   **[Configure Azure Monitor Bi-directional connector](../task/configure-azure-bi-directional-connector.md)**  
The Azure Monitor Pull connector sends information from ServiceNow Event Management to the Azure Portal. The pull connector sends the alert state changes from the ServiceNow environment to the Azure Portal.

**Parent Topic:**[Integrate with push connectors](../task/configure-listener-transform-script.md)

