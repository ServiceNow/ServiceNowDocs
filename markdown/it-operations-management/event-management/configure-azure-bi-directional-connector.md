---
title: Configure Azure Monitor Bi-directional connector
description: The Azure Monitor Pull connector sends information from ServiceNow Event Management to the Azure Portal. The pull connector sends the alert state changes from the ServiceNow environment to the Azure Portal.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrate Azure Monitor as an authenticated data source, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure Azure Monitor Bi-directional connector

The Azure Monitor Pull connector sends information from ServiceNow Event Management to the Azure Portal. The pull connector sends the alert state changes from the ServiceNow environment to the Azure Portal.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

When an alert is triggered in the Azure Portal a Secure Webhook is created to send the alert notifications into ServiceNow. The [Azure Monitor Connector](../concept/azure-integration.md) will receive the alert notification as an event in the ServiceNow instance.

The Azure Monitor Bi-directional connector is supported in the following ServiceNow AI Platform versions:

-   Quebec Patch 9 or later.
-   Rome Patch 3 or later.

Role required: evt\_mgmt\_admin

## About this task

When you configure the Azure Monitor Bi-directional Connector, the bi-directional exchange of values to and from the external event source is enabled, When an alert is **Acknowledged**/**Closed**/**Reopened** on the ServiceNow instance, the state changes in the Azure Portal alert using the bi-directional connector.

These scenarios describe the default bi-directional functionality for the Azure Monitor connector:

-   When an alert is closed in the Azure Portal, it is automatically closed in ServiceNow. However, it is updated irrespective of the bi-directional feature because closing the event received from the Azure Portal will close the alert.
-   When an alert is manually closed in ServiceNow, all the associated Azure alerts will be closed in the Azure Portal.
-   If the alert state is changed to **Reopen** in ServiceNow, all the associated Azure alerts will be opened in the Azure Portal.
-   When an alert is **Acknowledged** in ServiceNow, all the associated Azure alerts will be acknowledged in the Azure Portal.

**Note:** For changing the alert state on the Azure Portal, Mid Server gets access token connecting to [https://login.microsoftonline.com/](https://login.microsoftonline.com/) and to change the alert state on the Azure portal Mid Server calls changestate API on URL [https://management.azure.com/](https://management.azure.com/) as described in [https://learn.microsoft.com/en-us/rest/api/monitor/alertsmanagement/alerts/change-state?view=rest-monitor-alertsmanagement-2023-07-12-preview&amp;tabs=HTTP](https://learn.microsoft.com/en-us/rest/api/monitor/alertsmanagement/alerts/change-state?view=rest-monitor-alertsmanagement-2023-07-12-preview&tabs=HTTP).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **Azure Monitor**.

3.  Select the **Active** check box.

    **Note:** For this configuration, the **Host IP** field has no functional impact, so a dummy IP address \(1.1.1.1\) is provided.

4.  In the **Credential** field, add the Azure Service Principal credentials that has authorization to perform actions.

    To change the alert state, the service principal must have the [Microsoft.AlertsManagement](https://learn.microsoft.com/en-us/azure/role-based-access-control/permissions/monitor#microsoftalertsmanagement) permissions and the [Monitoring Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/monitor#monitoring-contributor) role.

5.  Select or add the MID Server to be used for this connector.

    If alerts on the MS Azure portal are not updating as expected, check the MID Server logs for errors.


## What to do next

Multiple alerts from the Azure Portal may be mapped to a single ServiceNow alert by de duplication. The mapping between the ServiceNow alert and Azure alerts will be maintained in the sn\_em\_connector\_event\_data table. The retention of records will depend on the alert's state:

-   If the Azure Bi-directional Connector is not active, the records will be deleted in 2 days.
-   When the Azure Bi-directional Connector is active:
    -   If the alert is in a closed state, then it will retain the data for 7 days. This duration can be customized by the sn\_em\_connector.eventdata\_closedevent\_interval system property.
        -   If the closed alert is re-opened in 7 days then it will reopen the corresponding closed alerts from the Azure Portal.
        -   If the closed alert is re-opened after 7 days then it will not reopen the corresponding closed alerts from the Azure Portal.
    -   If the alert is in an open state, then it will retain the data for 30 days. . This duration can be customized by the sn\_em\_connector.eventdata\_openevent\_interval.
        -   If you want to close or acknowledge an open ServiceNow alert in 30 days, you will be able to close or acknowledge all corresponding Azure alerts on the Azure Portal.
        -   If you want to close or acknowledge an open ServiceNow alert after 30 days, you will not be able to close or acknowledge all corresponding Azure alerts on the Azure Portal.

**Parent Topic:**[Integrate Azure Monitor as an authenticated data source](../concept/azure-integration.md)

