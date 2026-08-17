---
title: Azure Monitor Issue integration
description: An Azure Issue is a unified case that aggregates related alerts and signals from Azure Monitor into a single, trackable operational problem. It preserves investigation context and serves as a durable record for incident management Incident Management, so you can resolve problems faster instead of tracking scattered alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/azure-monitor-issue-integration.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 4
breadcrumb: [Integrate Azure Monitor as an authenticated data source, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Azure Monitor Issue integration

An Azure Issue is a unified case that aggregates related alerts and signals from Azure Monitor into a single, trackable operational problem. It preserves investigation context and serves as a durable record for incident management Incident Management, so you can resolve problems faster instead of tracking scattered alerts.

## Before you begin

Verify you already have an Azure Monitor Workspace.

Role required: evt\_mgmt\_admin

## About this task

ServiceNow represents an Azure Issue as a single alert. View the alerts that Azure grouped into the Issue in the **Related Records** tab from the Express List side panel or the alert record in Service Operations Workspace. ServiceNow retains each related alert as an individual alert. This approach lets ServiceNow group and correlate alerts across multiple resources and monitoring systems. ServiceNow is not limited to the alerts that Azure grouped into the Issue. As a result, ServiceNow identifies broader incidents, reduces duplicate alerts, and provides a more comprehensive operational view. For this reason, ServiceNow represents an Azure Issue as a single alert instead of an alert group.

Note the following before you start:

-   If you already use the Azure Push Connector to send Microsoft Azure alerts to ServiceNow, use the same push connector URL to send Azure Issues.
-   If you're configuring Azure alerts/issues for the first time, use the Azure Push Connector URL to create an action group in the Azure portal. Use the following URL in the Azure action group secure webhook field:

    ```
    https://<instance_name>.service-now.com/api/sn_em_connector/em/inbound_event?source=azuremonitor
    ```

-   If you have different tenants with different Azure Service Principal credentials \(per tenant or per subscription\), create separate Azure Push Connector instances. Use them to push Azure alerts or issues into your ServiceNow instances.

You can integrate Azure Monitor issues using Integration Launchpad. For more information, see [Configure Azure Monitor Issue in Integrations Launchpad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/configure-azure-monitor-issue-integrations-launchpad.md).

## Procedure

1.  In the Azure Monitor portal, perform the following steps:

    1.  Navigate to your Azure Monitor Workspace.
    2.  Navigate to **Settings** &gt; **Action groups** and select the existing action group that you use to send Azure alerts to ServiceNow.

        This creates an alert, and in turn, the Alert Management rule creates an incident. If you're configuring Azure issues for the first time, first create an action group by following the steps in [Integrate Azure Monitor with OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/azure-events-authentication.md).

    3.  If you need related alerts and resource information for an issue in the Azure portal under the **Alerts** and **Resources** tab and for bi-directional synchronization, configure the pull connector by performing the steps as mentioned below.
2.  In the ServiceNow AI Platform instance, configure a pull connector if you have used a push connector to send Azure issues by perform the following steps:

    1.  Navigate to the push connector you're using by going to **All** &gt; **Push connectors**.
    2.  Select the Azure Monitor push connector.
    3.  Select **Configure Issue Alerts** on the push connector form.

        You're redirected to the pull connector instance form.

    4.  If the Azure Monitor pull connector is already activated, verify your credentials and that the instance is active, then select **Test Connection** to validate.
    5.  If the Azure Monitor pull connector is not activated yet, configure it as follows:
        1.  Leave the pull connector instance name as `Azure Monitor`.
        2.  In the **Credentials** field, enter your Azure Service Principal credential.
        3.  Leave the **Host** field as `1.1.1.1` as it will not be used.
        4.  Select the **Active** check box to activate the connection.
        5.  Set **fetchIssueRelatedAlerts** to control whether the system fetches related alerts for the issue.

            The default is true. Set it to false if you want to disable this behavior.

        6.  Set **fetchIssueRelatedAlertsLimit** to the maximum number of related alerts the system fetches for the issue. The default is 10.
        7.  Select **Test Connection** to validate the connection.

            If Azure bi-directional connector is enabled, when an Azure issue is closed in ServiceNow, it automatically closes in the Azure portal as well.

            When an Azure issue is closed in ServiceNow, it automatically closes in the Azure portal as well.

3.  In the ServiceNow AI Platform instance, configure a pull connector if you have used a push connector instance to send Azure issues by perform the following steps:

    1.  Navigate to the push connector instance you're using in ServiceNow by navigating to **All** &gt; **Push connector Instances**.
    2.  Select the Azure Monitor push connector instance that was used to send Azure Issues in to ServiceNow instance.
    3.  Select **Configure Issue Alerts** UI action present in the push connector form.

        You're redirected to the pull connect instance form.

    4.  In the pull connector creation form, perform the following steps:
        1.  Leave the pull connector instance name as is.

            The pull connector instance name must match with the push connector instance name.

        2.  In the **Credentials** field, enter your Azure Service Principal credential.
        3.  Leave the **Host** field as `1.1.1.1` as it will not be used.
        4.  Select the **Active** check box to activate the connection.
        5.  Set **fetchIssueRelatedAlerts** to control whether the system fetches related alerts for the issue.

            The default is true. Set it to false if you want to disable this behavior.

        6.  Set **fetchIssueRelatedAlertsLimit** to the maximum number of related alerts the system fetches for the issue. The default is 10.
        7.  Select **Test Connection** to validate the connection.

            If Azure bi-directional connector is enabled, when an Azure issue is closed in ServiceNow, it automatically closes in the Azure portal as well.


**Parent Topic:**[Integrate Azure Monitor as an authenticated data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/azure-integration.md)

