---
title: Components installed with Workplace Connectors
description: Several types of components are installed with the installation of the Workplace Connectors application, including user roles and tables.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Workplace Connectors references, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Connectors

Several types of components are installed with the installation of the Workplace Connectors application, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application.

## Roles installed with Workplace Connectors

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_wsd\_wc.manager|Provides read access to all data including Occupancy Dashboard and other dashboards.|sn\_wsd\_wc.user|
|sn\_wsd\_wc.admin|Provides admin access to configure and set up the Workplace Connectors application.|sn\_wsd\_wc.manager|
|sn\_wsd\_wc.user|Provides read access to only a few columns and fields. The read access is set up by administrators.|None|

## Tables installed with Workplace Connectors

<table id="table_x31_wb4_wvb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Providers \[sn\_wsd\_wc\_provider\]

</td><td>

Stores Space Occupancy sensor data provided by occupancy data providers.

</td></tr><tr><td>

Connector Configuration\[sn\_wsd\_wc\_connector\_config\]

</td><td>

Configures a connector to connect with the integration framework. This configuration fetches the data from the integration to workplace applications.This table holds information about the workplace connectors that are defined in the application. For example, Badging data, Occupancy sensors, and so on. This table can also process data for each of the connectors through extension points.

</td></tr><tr><td>

Provider Execution\[sn\_wsd\_wc\_provider\_execution\]

</td><td>

Stores all the scheduled job execution timestamps. Every time the scheduled job **Process Provider data** record runs, this table has an entry for the last query time. The time taken to import data from the source table \(Badging data\) to the target table \(Employee attendance data\) table is updated in the **Last query time**.

t

</td></tr><tr><td>

Provider connector configuration\[sn\_wsd\_wc\_provider\_config\]

</td><td>

Stores provider data \(Occupancy or badging\). Imports data from the source table to the target table.

</td></tr><tr><td>

Connector Events\[sn\_wsd\_wc\_connector\_events\]

</td><td>

The Connector Events table \(sn\_wsd\_wc\_connector\_events\) loads the badging data shared by badging vendors.The Scheduled Job **Process webhook provider data records** runs every minute to load the badging data from the Connector Events table \(data with State **New**\) to the Employee Attendance Data table. For more information, see [Configure a webhook event](../task/configure-webhook-restapi.md).

</td></tr><tr><td>

Provider Space Type Mapping \[sn\_wsd\_wc\_provider\_space\_type\_mapping\]

</td><td>

Stores mapping between Workplace Core space or location records and sensor provider data records for occupancy data.

</td></tr><tr><td>

Provider Space Mapping \[sn\_wsd\_wc\_provider\_space\_mapping\]

</td><td>

Stores external Ids shared by a sensor provider, for example, Metrikus. The external Ids from sensors providers are mapped with spaces shared by Workplace Connectors.

</td></tr><tr><td>

Action Configuration \[sn\_wsd\_wc\_action\_config\]

</td><td>

Stores actions, subflows, and transform definitions from Metrikus Spoke.

</td></tr><tr><td>

Badging Data \[sn\_wsd\_wc\_badging\_data\]

</td><td>

Stores employee badging data details.

</td></tr><tr><td>

Badging Data Choices \[sn\_wsd\_wc\_badging\_data\_choice\]

</td><td>

Stores the badging status details for Swipe-in and Swipe-out event types.

</td></tr><tr><td>

Occupancy and Environment Data \[sn\_wsd\_wc\_occ\_env\_data\]

</td><td>

Stores occupancy and environment data such as carbon dioxide value, ozone, sound, light, temperature, pressure, and humidity levels for a workplace location.

</td></tr><tr><td>

Wi-fi Data \[sn\_wsd\_wc\_wifi\_data\]

</td><td>

Stores Wi-Fi data.

</td></tr><tr><td>

Unit of Measure \[sn\_wsd\_wc\_unit\_of\_measure\]

</td><td>

Unit of measure for air, temperature, VOC, and so on. For more information, see [Set up the Units of measure data table for environmental sensors](../task/wsd-enviromental-unit-measure.md).

</td></tr><tr><td>

Space Occupancy Daily Summary Data \[sn\_wsd\_wc\_space\_occupancy\_daily\_summary\_data\]

</td><td>

Stores space occupancy daily summary data.

</td></tr><tr><td>

Wi-Fi Daily Summary Data \[sn\_wsd\_wc\_wifi\_daily\_summary\_data\]

</td><td>

Stores Wi-Fi daily summary data.

</td></tr><tr><td>

Environmental Daily Summary Data \[sn\_wsd\_wc\_environmental\_daily\_summary\_data\]

</td><td>

Stores environmental daily summary data.

</td></tr><tr><td>

Environmental Hourly Summary Data \[sn\_wsd\_wc\_environmental\_hourly\_summary\_data\]

</td><td>

Stores environmental hourly summary data.

</td></tr></tbody>
</table>## Scheduled job

Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**. Search for Workplace Connectors in the Application column.

-   **Process webhook provider data records**: Runs every minute to process webhook event provider data records. For more information, see [Configure a webhook event](../task/configure-webhook-restapi.md).
-   **Process provider data records**; Runs every 5 minutes to process provider data records in Workplace Connectors.
-   **Refresh Provider Space Mapping records**: Runs daily runs daily and executes the space filter condition on the Provider Connector configuration table for the active records where the Auto-refresh field is set to True. For more information, see [Provider Connector Configuration](../task/provider-connector-config-occupancy.md).

**Parent Topic:**[Workplace Connectors references](../concept/workplace-connectors-references.md)

**Previous topic:**[Workplace Connectors references](../concept/workplace-connectors-references.md)

**Next topic:**[Environmental data form for Workplace Connectors](wsd-environmental-data-form-fields.md)

