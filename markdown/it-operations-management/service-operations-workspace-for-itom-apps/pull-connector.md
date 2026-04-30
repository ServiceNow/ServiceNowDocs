---
title: Configure a pull connector
description: Configure pull connectors that require a script, connector definition, and connector instance to pull events from external devices. These connectors automate the data retrieval process, ensuring the seamless integration of external events into your system for efficient monitoring and management.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrations Launchpad in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Configure a pull connector

Configure pull connectors that require a script, connector definition, and connector instance to pull events from external devices. These connectors automate the data retrieval process, ensuring the seamless integration of external events into your system for efficient monitoring and management.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../image/integrations-launchpad.png)\)

3.  In the **Browse Integrations** tab, select the **All integrations** drop-down list and select **Pull**.

    Only pull connector tiles are displayed.

    ![Filtering with Pull connectors](../image/pull-connectors-page.png "Pull connectors")

4.  Select a pull connector tile.

    If a pop-up menu opens, select the data to track from that connector and select **Continue**.

    ![Pull connectors details page](../image/pull-connectors-details.png "Pull connectors details page")

5.  In the **Details** tab, in the **Connector name** field, enter a unique name for the connector type.

6.  In the **Tags** field, enter tags to help locate and identify connectors of this type on the Express List.

    To add additional tags, select the plus icon \(![Plus sign to add more tags.](../image/icon-plus-sign.png)\) next to the **Tags** field. The Add tags window opens.

    1.  In the **Key** field, enter a tag key.
    2.  In the **Value** field, enter a tag value.
    3.  Select **Add**.
7.  In the **Description** field, enter brief information about this connector.

8.  From the **Assignment group** drop-down list, select the group or team that is responsible for managing and maintaining the connector.

9.  In the **Host IP** field, enter the IP address that is used to select the appropriate MID Server for communicating with the event source host.

    You can use the host name instead of the host IP.

10. From the **Credentials** drop-down list, select the valid credentials to access the event source host.

    To create a new credential, select **Create new credentials** and continue with the process.

11. If you want to customize configurations to meet specific requirements, select **Advanced settings** and fill in the form.

<table id="table_cwg_vzv_mbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connected MID Server

</td><td>

Determine whether you want to have the system choose the optimal MID Server or choose a specific MID Server yourself.Perform only if you must make modifications to the MID Server otherwise leave it empty and let the system choose the optimal MID Server.

</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

Enter the frequency in seconds that indicates how often the system should check for new events from the external event source. The value can’t be lower than the minimum schedule property, which by default is 120 seconds.

</td></tr><tr><td>

Protocol

</td><td>

Defines the communication protocol used for retrieving events from external devices.

</td></tr><tr><td>

severity\_by\_state\_type

</td><td>

Determines the severity level assigned to events based on their state type.

</td></tr><tr><td>

time\_zone

</td><td>

Specifies the time zone used for recording and displaying event timestamps.

</td></tr><tr><td>

offset\_min

</td><td>

Sets the time offset for event retrieval to ensure accurate synchronization.

</td></tr><tr><td>

Port

</td><td>

Verify the default values for your connector type such as port details or time formats and modify them as necessary. Default values from your connector are filled-in. Specifies the port number used for communication with external devices.

</td></tr><tr><td>

max\_fetch\_interval\_min

</td><td>

Limits the maximum interval between event fetch operations.

</td></tr><tr><td>

initial\_sync\_in\_days

</td><td>

Sets the duration for the initial synchronization process when retrieving historical data.

</td></tr></tbody>
</table>12. Test the connector before activating it by selecting **Test and Save**.

13. To save the connector, select **Save**.

14. To activate the pull connector, select **Activate**.

    The pull connector is activated and its tile is displayed in the **Installed Integrations** tab.


## What to do next

To confirm the successful configuration of the pull connector and the flow of events into the system, select the **Related events** tab. If the setup is successful, proceed to **Add automation** to establish an alert automation. For details on **Related events** tab, see [Review integration and configuration health](review-integration-config-health.md) and for information on alert automation, see [Alert automation in Service Operations Workspace for ITOM](../concept/sow-itom-alert-automation.md).

