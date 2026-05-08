---
title: Configure Datadog metric pull connector
description: Configure OAuth-based integration between your Datadog instance and ServiceNow Event Management to securely ingest metric from the Datadog Instance. This setup enables authenticated metric delivery using client credentials, maps discovered server CIs, and allows anomaly alerts to create actionable events in ServiceNow through standard webhooks.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Integrations Launchpad in Service Operations Workspace for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Configure Datadog metric pull connector

Configure OAuth-based integration between your Datadog instance and ServiceNow Event Management to securely ingest metric from the Datadog Instance. This setup enables authenticated metric delivery using client credentials, maps discovered server CIs, and allows anomaly alerts to create actionable events in ServiceNow through standard webhooks.

## Before you begin

Role required: evt\_mgmt\_admin

Configure the Datadog API Key credential from **All** &gt; **Connections and Credentials** &gt; **Credentials**. For more information on how to configure Datadog API Key credential, see API key credentials.

Ensure you have the application key configured in the Datadog. For more information, see [https://docs.datadoghq.com/account\_management/api-app-keys/](https://docs.datadoghq.com/account_management/api-app-keys/).

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../../health-log-analytics-admin/image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the **Setup** &gt; **Integrations** section, select **Manage Installed integrations**.

4.  In the **Browse Integrations** tab, select the **All integrations** drop-down list and select **Metrics** &gt; **Pull**.

    ![Metric pull integrations.](../image/sow-metricintegration-pull.png)

    Only metric pull connector tiles are displayed.

5.  Select the **Datadog Metrics** connector tile.

6.  In the **Provide details** section, enter the following information and select **Next**.

    -   In the **Name** field, enter a unique name for the connector type.
    -   In the **Data source** field, the external source for retrieving metrics is auto-populated based on the tile type you select.

        In this case, select **Datadog**.

    -   In the **Description** field, enter brief information about this connector.
7.  In the **Set data retrieval method** section, enter the following information:

    -   In the **Hostname/Host IP** field, enter the IP address that is related to the Datadog server.
    -   From the **Credentials** drop-down list, select the valid credentials to access the metrics source host.

        Select the credential.

    -   In the **Metric collection schedule \(in seconds\)** field, enter the time interval \(in seconds\) at which the connector retrieves metrics from the source host.

        The default value is 60 seconds.

    -   In the **MID Server** field, select a MID Server that collects metric data from external tools and securely sends it to ServiceNow.

        If none are available, ensure one is installed, running, and has the required capabilities. If none are available, ensure one is installed, running, and has the required capabilities. For example, the **Metric Intelligence Context** must be running on the same MID Server that you are configuring.

        **Note:** You can select multiple MID Server. The system randomly assigns one as the primary and uses the others as backups.

    -   in the **Application key** field, enter the application key that is associated with the user account.
8.  If you want to customize configurations to meet specific requirements, select **Advanced settings** and fill in the form.

    For more information on fields, see [Datadog advanced settings fields](../reference/datadog-advanced-settings-fields.md).

9.  Test the connector before activating it by selecting **Test and Save**.

10. To save the connector, select **Save**.

11. To activate the pull connector, select **Activate**.

    The metric pull connector is activated and its tile is displayed in the **Installed Integrations** tab. When you open the tile, you can find the **Overview**, **Details**, and **Data retrieval method** tabs.

    The **Overview** tab allows you to verify that the connector is running and collecting data. It also offers options to improve system settings, such as refining alert definitions or enhancing binding configurations.

    The **Details** tab allows you to update the connector's general information \(such as name or description\) and displays any errors encountered during its operation.

    The **Data Retrieval Method** tab contains the connector settings \(such as host, port, and credentials\) and may provide additional details for issues like MID Server errors.


