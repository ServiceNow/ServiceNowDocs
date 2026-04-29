---
title: Retrieving Space Occupancy Data
description: Retrieve the Space Occupancy Data table for loading workplace occupancy data and space occupancy data insights for a selected workplace location.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Retrieving Space Occupancy Data

Retrieve the Space Occupancy Data table for loading workplace occupancy data and space occupancy data insights for a selected workplace location.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Occupancy Sensors** &gt; **Space Occupancy Data**.

    Fill in the form fields.

<table id="table_j5j_wct_s1c"><thead><tr><th>

Field

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Provider Connector Configuration

</td><td>

Option to select the occupancy data provider and occupancy sensor.For example, **Metrikus - Occupancy**.

</td></tr><tr><td>

Count

</td><td>

Option to specify the count of users in a workplace location or space. Takes integer value. For example, 0, 1, and so on.

</td></tr><tr><td>

Event timestamp

</td><td>

Option to check for the stale time of the data. Stale time sn\_wsd\_wc\_stale\_time checks if the **Event Timestamp** field in the Space Occupancy data table has the latest timestamp. This property checks for the time beyond which the occupancy data is considered stale. Beyond the stale time, the fresh data is fetched from the Occupancy data provider \(for example, Metrikus Spoke\). If the **sn\_wsd\_wc\_stale\_time** property value is set to 30 minutes, application queries the Space Occupancy table and fetches the fresh data for a location or space from Metrikus every 30 minutes.

</td></tr><tr><td>

Location

</td><td>

Option to select a location for which you want the occupancy data.

</td></tr><tr><td>

State

</td><td>

Option to select the space or location Occupancy status \(occupied, unoccupied, currently unoccupied, invalid, and so on.\) for a selected location.

</td></tr><tr><td>

Query Status

</td><td>

Indicates the **Requested** or **Received** status for Occupancy sensor data.-   **Requested**: Indicates a null or no response from Metrikus when there’s an error or when the workplace spaces aren’t mapped with Metrikus external Ids.
-   **Received**: Indicates a successful response from Metrikus for occupied or unoccupied workplace locations.
To check for occupancy status of a space in the location directory \(Card view and Map view\), confirm that your Query status is in the **Received** status. If a workplace location or space is mapped with occupancy sensor data, the location directory space records also get updated \(Occupied, unoccupied, not currently occupied, and so on\).

</td></tr></tbody>
</table>2.  Select **Submit** after making edits or any updates.

    The retrieved space occupancy data can be used to verify the following use cases:

    -   Showing the occupancy data in the Location Directory. For more information, see [Manage workplace activities and services with Location directory](../../workplace-service-delivery/concept/location-directory.md).
    -   Automatic reservation check-in. For more information, see [Configure automatic check-in for reserved spaces](../../wsd-reservation-management/concept/configure-rsv-check-in.md).

**Parent Topic:**[Setup Workplace Connectors for occupancy data](../concept/setup-occupancy-connectors.md)

**Previous topic:**[Retrieving Action Configurations data](actions-configurations-occupancy.md)

**Next topic:**[Archive and Purge space occupancy data](archive-purge-occupancy-data.md)

