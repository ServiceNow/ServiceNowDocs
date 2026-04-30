---
title: Set up the Units of measure data table for environmental sensors
description: Configure the unit of measure for air quality \(Carbon dioxide and Ozone metric\) and temperature units \(degree celsius and micrograms per cubic meter\) for a workplace location. The Workplace Connectors environmental sensors checks for the air and temperature quality metrics in a workplace location.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Connectors for environmental data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Set up the Units of measure data table for environmental sensors

Configure the unit of measure for air quality \(Carbon dioxide and Ozone metric\) and temperature units \(degree celsius and micrograms per cubic meter\) for a workplace location. The Workplace Connectors environmental sensors checks for the air and temperature quality metrics in a workplace location.

## Before you begin

**Note:** The units selected in the Units of measure data table should match with the actual data that is shared by your provider or vendor using the Extension Point definition or EnvironmentDataHandler. If the data units don't match, it must be converted and then, stored in the environmental data. For more information, see [Provider Connector Configuration for Environmental sensors](wsd-env-provider-connectorconfig.md)

Seed data or out-of-the box table record is provided with the application and provides pre-filled values. If you want to create a new table record follow these steps.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Units of Measure**.

2.  Select **New**.

3.  Fill in the form fields.

<table id="table_a2s_zg1_rbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

The Environmental sensor data table \(sn\_wsd\_wc\_space\_environment\) name.

</td></tr><tr><td>

Value field

</td><td>

Parameters for which you want to have the unit of measure. For example, Carbon dioxide units, Event timestamp, Location, Ozone units, Temperature units, Relative humidity, and so on. If you select Carbon dioxide, then units for carbon dioxide are shown.

</td></tr><tr><td>

Metric

</td><td>

Air quality metrics like Carbon dioxide, Ozone, Particular Matter \(PM\), and so on. For example, if you select **Temperature** in Value field, metrics related to temperature are displayed.

</td></tr><tr><td>

Units

</td><td>

Units for the metrics selected in the Metrics filed. For example, **Parts per million** in case if you have selected Carbon dioxide in the Metric field.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Setup Workplace Connectors for environmental data](../concept/setup-environmental-data-connectors.md)

**Previous topic:**[Provider Connector Configuration for Environmental sensors](wsd-env-provider-connectorconfig.md)

**Next topic:**[Configure environmental sensor data for a workplace location](config-connectors-env-sensor.md)

