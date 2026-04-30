---
title: Environmental data form for Workplace Connectors
description: Environmental sensor data form has pre-filled environmental data values and units of measure.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Environmental data form for Workplace Connectors

Environmental sensor data form has pre-filled environmental data values and units of measure.

<table id="table_ryt_klt_qbc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Units

</th></tr></thead><tbody><tr><td>

Provider connector configuration

</td><td>

Environmental data provider sensor.For example, **Metrikus- Environment**.

</td><td>

NA.

</td></tr><tr><td>

Carbon dioxide

</td><td>

Carbon dioxide \(CO2\) concentration level in a workplace location.

</td><td>

Carbon dioxide units.

</td></tr><tr><td>

Ozone

</td><td>

Ozone level unit in a workplace location.

</td><td>

Ozone units.

</td></tr><tr><td>

Temperature

</td><td>

Temperature levels to measure extreme heat or cold in a workplace location.

</td><td>

Temperature units.

</td></tr><tr><td>

Total volatile organic compounds \(TVOCs\)

</td><td>

Unit for Volatile organic compounds \(VOCs\) in a location. Helps in analyzing the air quality and identifying the sources of pollution to reduce environmental exposure.

</td><td>

Total volatile organic compounds \(TVOCs\) units.

</td></tr><tr><td>

Relative humidity

</td><td>

Humidity levels in a workplace location. High humidity promotes growth of mold that can cause respiratory issues.

</td><td>

Relative humidity units.

</td></tr><tr><td>

Particulate matter 2.5

</td><td>

Particulate matter \(PM\) for fine air particles measuring PM 2.5.microns or less in diameter.

</td><td>

Particulate matter 2.5 units.

</td></tr><tr><td>

Particulate matter 10

</td><td>

Particulate matter \(PM\) for microscopic matter suspended in air measuring PM 10 mu or micro in diameter.

</td><td>

Particulate matter 10 units.

</td></tr><tr><td>

Event timestamp

</td><td>

Date and time for the event timestamp.Stale time sn\_wsd\_wc\_stale\_time checks if the **Event Timestamp** data has the latest timestamp. This property checks for the time beyond which the data is considered stale. Beyond the stale time, latest or current data is fetched from the data provider \(for example, Metrikus Spoke\).

</td><td>

NA

</td></tr><tr><td>

Location

</td><td>

Workplace location where the environmental data sensor is installed.

</td><td>

NA

</td></tr><tr><td>

Query status

</td><td>

**Note:** This is an internal field and is used by the Workplace Connectors framework to optimize the Provider queries. This field should not be manually updated.

</td><td>

NA

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Connectors references](../concept/workplace-connectors-references.md)

**Previous topic:**[Components installed with Workplace Connectors](component-workplace-connectors.md)

**Next topic:**[Data summarization](data-summarization-workplace-connectors.md)

