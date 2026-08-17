---
title: Configure Azure Monitor Issue in Integrations Launchpad
description: An Azure Issue is a unified case that aggregates related alerts and signals from Azure Monitor into a single, trackable operational problem. It preserves investigation context and serves as a durable record for incident management, so you can resolve problems faster instead of tracking scattered alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/configure-azure-monitor-issue-integrations-launchpad.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 5
breadcrumb: [Integrations Launchpad in SOW for ITOM, ITOM AIOps, IT Operations Management]
---

# Configure Azure Monitor Issue in Integrations Launchpad

An Azure Issue is a unified case that aggregates related alerts and signals from Azure Monitor into a single, trackable operational problem. It preserves investigation context and serves as a durable record for incident management, so you can resolve problems faster instead of tracking scattered alerts.

## Before you begin

Verify you already have an Azure Monitor Workspace.

Role required: evt\_mgmt\_admin

## About this task

ServiceNow represents an Azure Issue as a single alert. View the alerts that Azure grouped into the Issue in the **Related Records** tab from the Express List side panel or the alert record in Service Operations Workspace. ServiceNow retains each related alert as an individual alert. This approach lets ServiceNow group and correlate alerts across multiple resources and monitoring systems. ServiceNow is not limited to the alerts that Azure grouped into the Issue. As a result, ServiceNow identifies broader incidents, reduces duplicate alerts, and provides a more comprehensive operational view. For this reason, ServiceNow represents an Azure Issue as a single alert instead of an alert group.

Note the following before you start:

-   If you already use the Azure push connector to send Microsoft Azure alerts to ServiceNow, use the same push connector URL to send Azure Issues.
-   If you have different tenants with different Azure Service Principal credentials \(per tenant or per subscription\), create separate Azure push connector instances. Use them to push Azure alerts or issues into your ServiceNow instances.

## Procedure

1.  If you don't already have a Azure monitor alert integration then create a push connector instance by perform the following steps:

    1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.
    2.  From the bottom of the navigation pane, select the AIOps Configuration Center icon \[Omitted image "icon-itom-aiops-config.png"\] Alt text: ITOM AIOps configuration center icon.

        The ITOM AIOps Configuration Center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

    3.  On the ITOM AIOps Configuration Center page, under the Setup Integrations section, select **Add integrations**.

        The Integrations Launchpad page opens.

    4.  Search for **Microsoft Azure to instance** and create a push connector instance by providing the following details:
        1.  In the Provide details page, provide the connector name and description for the connector in the **Connector name** and **Description** field.
        2.  Select **Next**.

            The Set-up push connector page opens.

        3.  From the **URL parameter value** field, copy the URL by selecting the **Copy link to clipboard**.

            The URL can be used in the Microsoft Azure Action group Securewebhook URL to send Azure alerts and Azure Issues into ServiceNow instance. The URL must be in the following format:

            ```
            https://<instance_name>.service-now.com/api/sn_em_connector/em/inbound_event?source=azuremonitor&sys_id=<sys_id_push_connector_instance>
            ```

        4.  Select **Activate** to activate the push connector instance.
2.  In the Azure Monitor portal, perform the following steps:

    1.  Navigate to your Azure Monitor Workspace.
    2.  Navigate to **Settings** &gt; **Action groups** and select the existing action group that you use to send Azure alerts to ServiceNow.

        This creates an alert, and in turn, the Alert Management rule creates an incident. If you're configuring Azure issues or alerts for the first time, first create an action group by using the above URL you have copied. Then follow the steps in [Integrate Azure Monitor with OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/azure-events-authentication.md).

        If you're configuring Azure issues or alerts for the first time, first create an action group by using the above URL you have copied. Then follow the steps in Integrate Azure Monitor with OAuth authentication.

    3.  The pull connector shows related alerts and resource information for an issue in the Azure portal under the **Alerts** and **Resources** tab, and enables bi-directional synchronization. To configure it, perform the steps below.
3.  Verify that the pull connector instance is active by performing the following step:

    **Note:** If you used the push connector to bring Azure alerts or issues into ServiceNow, the pull connector instance may already be active.

    In Integration Launchpad, on the **Installed Integrations** tab, search for `Azure Monitor` and confirm that it is already active.

    **Note:** If you have already configured a pull connector instance for Azure Alerts bi-directional sync, it also works for Azure Issues bi-directional sync and for fetching Azure Issue-related alerts.

4.  If you used the push connector to bring Azure alerts or issues into ServiceNow but the Azure Monitor pull connector is not yet active, perform the following steps:

    1.  On the **Installed Integrations** tab, search for `Microsoft Azure` and select the **Microsoft Azure \(Events – pull\)** tile to open the pull connector instance.
    2.  In the **Credentials** field, enter your Azure Service Principal credential.
    3.  Leave the **Host** field as `1.1.1.1`, because it is not used.
    4.  To use a specific MID Server, go to **Advanced Settings** and select the mid server in the **Connected mid server** field.
    5.  Select **Test and Save**.

        If the test connection succeeds, activate the connector.

        If Azure bi-directional connector is enabled, when an Azure issue is closed in ServiceNow, it automatically closes in the Azure portal as well.

5.  If you used the push connector to bring Azure alerts or issues into ServiceNow, configure a pull connector instance by performing the following steps:

    1.  On the **Browse Integrations** tab, search for `Microsoft Azure` and select the **Microsoft Azure \(Events – pull\)** tile to create a new pull connector instance.
    2.  On the **Details** tab, provide the following information:
        1.  In the **Connector name** field, enter a name for the pull connector instance.

            **Note:** The pull connector instance name must match with the push connector instance name.

        2.  In the **Credentials** field, enter your Azure Service Principal credential.
        3.  Leave the **Host** field as `1.1.1.1`, because it is not used.
        4.  To use a specific MID Server, go to **Advanced Settings** and enter the mid server name in the **Connected mid server** field.
        5.  Configure the following parameters to control how the system fetches related alerts for an issue:
            -   Set **fetchIssueRelatedAlerts** to control whether the system fetches related alerts for the issue.

                The default is true. Set it to false if you want to disable this behavior.

            -   Set **fetchIssueRelatedAlertsLimit** to the maximum number of related alerts the system fetches for the issue. The default is 10.
        6.  Select **Test and Save**.

            If the test connection succeeds, activate the connector.


