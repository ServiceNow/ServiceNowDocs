---
title: Connector Configurations
description: Configure the Connector Configurations table for loading the occupancy data in the target Space Occupancy Data table \(sn-wsd\_wc\_space\_occupancy\). Connector configuration table retrieves the sensor data from different occupancy data providers.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Connector Configurations

Configure the Connector Configurations table for loading the occupancy data in the target Space Occupancy Data table \(sn-wsd\_wc\_space\_occupancy\). Connector configuration table retrieves the sensor data from different occupancy data providers.

## Before you begin

Ensure that you have the sensor data providers to retrieve and fetch data from an occupancy data provider vendor. For more information, see [Configure sensor data providers](providers-occupancy.md)

**Note:** If you’re using demo data or product data \(seed data\), some fields are pre-filled. In case, if you aren’t using the base system product data, you can configure the connector data. The seed data is available as part of the Metrikus Spoke integration.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Connector Configuration**.

2.  Select **New**.

3.  Fill in the form fields:

<table id="table_cgv_4ln_vbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target Table

</td><td>

Option to indicate the target or destination table to store the occupancy data.Select Space Occupancy Data \(sn\_wsd\_wc\_space\_occupancy\) table. For more information, see [Retrieving Space Occupancy Data](space-occupancy-data.md).

</td></tr><tr><td>

Type

</td><td>

Option to select the type of sensor data. Select **Occupancy**.

</td></tr><tr><td>

Extension Point Definition

</td><td>

Option to search for extension point definition for the Occupancy data. Select the lookup list icon \(![Look up list icon to search for required extension point definition.](../images/wsd-lookup-list-icon.png)\) to search for an extension point definition, select the **OccupancyDataHandler** as the extension point for integration.

**Note:** Extension point definition defines how the data is transformed from third-party occupancy sensor data providers. The occupancy data is loaded into the target or final table \(Space Occupancy Data table\). The external IDs provided by Metrikus or other occupancy data providers are processed and transformed. Each occupancy data provider must have a separate implementation or integration spoke framework.

</td></tr><tr><td>

Stale time \(in minutes\)

</td><td>

Option to indicate the time \(in minutes\) beyond which occupancy data is considered stale.Beyond this time, fresh data is fetched from the Occupancy data provider table. When you select a floor on the map and if that space has occupancy data sensor, then, fresh occupancy data is fetched for only those spaces that have stale occupancy data.

</td></tr></tbody>
</table>4.  Select **Submit** to save the connector configuration.


**Parent Topic:**[Setup Workplace Connectors for occupancy data](../concept/setup-occupancy-connectors.md)

**Previous topic:**[Integrate Metrikus spoke](../concept/integrate-metrikus-flowdesigner.md)

**Next topic:**[Provider Connector Configuration](provider-connector-config-occupancy.md)

