---
title: Set up Connector Configuration for Environmental sensor data
description: Configure the Connector Configurations table for loading the Environmental data. Connector configuration table retrieves the sensor data from different environmental sensor data providers.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setup Workplace Connectors for environmental data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Set up Connector Configuration for Environmental sensor data

Configure the Connector Configurations table for loading the Environmental data. Connector configuration table retrieves the sensor data from different environmental sensor data providers.

## Before you begin

Make sure that vendor or provider is selected for fetching environmental sensor data. For more information, see [Configure sensor data providers](providers-occupancy.md).

**Note:** Seed data or out-of-the box table record is provided with the application and provides pre-filled values. If you want to create a new table record follow these steps.

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

Target or destination table to store the environmental sensor data.Select Environmental data \(sn\_wsd\_wc\_space\_environment\) table. For more information, see [Configure environmental sensor data for a workplace location](config-connectors-env-sensor.md).

</td></tr><tr><td>

Type

</td><td>

Type of sensor data. Select **Environment** from the list.

</td></tr><tr><td>

Extension Point Definition

</td><td>

Search for extension point definition for the environmental data. Search using the lookup list icon \(![Look up list icon to search for required extension point definition.](../images/wsd-lookup-list-icon.png)\) to locate the extension point definition **EnvironmentDataHandler**.

**Note:** Extension point definition defines how the data is transformed from third-party environmental sensor data providers. The data is loaded after transformation into the target environmental data table . The external IDs provided by Metrikus or other data providers are processed and transformed. Environmental data providers or vendors should have a separate implementation framework for these extension points.

For example, if you have two different vendors providing environmental data records, you are expected to create two different implementations for the extension point \(EnvironmentDataHandler, provided out-of-the-box\).

Make sure that you are storing the environmental data in the units as per the units configured in the Units of measure table. The units should match.

For example, If the environmental data provider or vendor is sharing Temperature sensor data records in Fahrenheit and the temperature unit in the Units of measure table is in Celsius, the Fahrenheit units should be converted to Celsius. The conversion can be done using the Extension point definition. For more information, see [Set up the Units of measure data table for environmental sensors](wsd-enviromental-unit-measure.md).

</td></tr><tr><td>

Stale time \(in minutes\)

</td><td>

Time \(in minutes\) beyond which data is considered stale.Beyond this time, fresh data is fetched from the data provider table. For example, 5 minutes. The application will fetch data every 5 minutes.

</td></tr></tbody>
</table>4.  Select **Submit** to save the connector configuration.


**Parent Topic:**[Setup Workplace Connectors for environmental data](../concept/setup-environmental-data-connectors.md)

**Previous topic:**[Setup Workplace Connectors for environmental data](../concept/setup-environmental-data-connectors.md)

**Next topic:**[Provider Connector Configuration for Environmental sensors](wsd-env-provider-connectorconfig.md)

