---
title: Pull connector fields
description: Populate the pull connector advanced settings fields to optimize event retrieval and synchronization based on specific requirements such as connection preferences, event frequency, and time zone settings.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Pull connector fields

Populate the pull connector advanced settings fields to optimize event retrieval and synchronization based on specific requirements such as connection preferences, event frequency, and time zone settings.

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
</table>To return to the main topic, see [Configure a pull connector](../task/pull-connector.md).

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

