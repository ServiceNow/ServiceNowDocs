---
title: Configure Solarwinds metric pull connector
description: Configure a metric pull connectors that require a script, connector definition, and connector instance to pull metrics from external sources. These connectors automate the data retrieval process, ensuring the seamless integration of external metrics into your system for efficient monitoring and performance analysis.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrations Launchpad in Service Operations Workspace for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Configure Solarwinds metric pull connector

Configure a metric pull connectors that require a script, connector definition, and connector instance to pull metrics from external sources. These connectors automate the data retrieval process, ensuring the seamless integration of external metrics into your system for efficient monitoring and performance analysis.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

**Note:** The new UI for configuring metric pull connector is currently available only for the SolarWinds Metric Connector. For all other metric connectors, the configuration continues to use the Platform Table UI.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../../health-log-analytics-admin/image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the **Setup** &gt; **Integrations** section, select **Add integrations**.

4.  In the **Browse Integrations** tab, select the **All integrations** drop-down list and select **Metrics** &gt; **Pull**.

    ![Metric pull integrations.](../image/sow-metricintegration-pull.png)

    Only metric pull connector tiles are displayed.

5.  Select a pull connector tile.

    If a pop-up menu opens, select the data to track from that connector and select **Continue**.

    ![Solarwinds metric connector details page.](../image/sow-solarwinds-metric-integration-details.png)

6.  In the **Provide details** section, enter the following information and select **Next**.

    -   In the **Name** field, enter a unique name for the connector type.
    -   In the **Data source** field, the external source for retrieving metrics is auto-populated based on the tile type you select.
    -   In the **Description** field, enter brief information about this connector.
7.  In the **Set data retrieval method** section, enter the following information:

    -   In the **Hostname/Host IP** field, enter the IP address that is related to the Solarwinds server.
    -   From the **Credentials** drop-down list, select the valid credentials to access the event source host.
    -   In the **Metrics collection schedule \(seconds\)** field, enter the time interval \(in seconds\) at which the connector retrieves metrics from the source host.
    -   In the **MID Server** field, select a MID Server that collects metric data from external tools and securely sends it to ServiceNow.

        If none are available, ensure one is installed, running, and has the required capabilities.

        **Note:** You can select multiple MID Servers. The system randomly assigns one as the primary and uses the others as backups.

8.  If you want to customize configurations to meet specific requirements, select **Advanced settings** and fill in the form.

<table id="table_cwg_vzv_mbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max rows per query

</td><td>

Frequency in seconds that indicates how often the system should check for new metrics from the external event source. The value can’t be lower than the minimum schedule property, which by default is 120 seconds.

</td></tr><tr><td>

Max fetch interval \(in minutes\)

</td><td>

Limits the maximum interval between event fetch operations.

</td></tr><tr><td>

Offset \(in minutes\)

</td><td>

Sets the time offset for event retrieval to ensure accurate synchronization.

</td></tr><tr><td>

Port

</td><td>

Specifies the port number used for communication with external devices.Verify the default values for your connector type such as port details or time formats and modify them as necessary. Default values from your connector are filled-in.

</td></tr><tr><td>

Protocol

</td><td>

Defines the communication protocol used for retrieving events from external devices.

</td></tr><tr><td>

Debugging

</td><td>

-   Debug: Provides detailed logs for troubleshooting.
-   Log payload: Displays raw log data. Use only for debugging, as it can quickly fill the MID Server logs.


</td></tr></tbody>
</table>9.  Test the connector before activating it by selecting **Test and Save**.

10. To save the connector, select **Save**.

11. To activate the pull connector, select **Activate**.

    The metric pull connector is activated and its tile is displayed in the **Installed Integrations** tab. When you open the tile, you can find the **Overview**, **Details**, and **Data retrieval method** tabs.

    The **Overview** tab allows you to verify that the connector is running and collecting data. It also offers options to improve system settings, such as refining alert definitions or enhancing binding configurations.

    ![Connector is active with three tabs: Overview, Details, Data retrieval method.](../image/sow-solarwinds-metric-integration-activated.png)

    The **Details** tab allows you to update the connector's general information \(such as name or description\) and displays any errors encountered during its operation.

    ![Details page in solarwinds metrics connector.](../image/sow-solarwinds-metric-integration-details-1.png)

    The **Data Retrieval Method** tab contains the connector settings \(such as host, port, and credentials\) and may provide additional details for issues like MID Server errors.

    ![Data retrieval method page in solarwinds metrics connector.](../image/sow-solarwinds-metric-integration-data-retrieval.png)


