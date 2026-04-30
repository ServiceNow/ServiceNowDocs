---
title: Provider Connector Configuration for Environmental sensors
description: Configure the provider connector configuration for setting up environmental sensors in workplace locations.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setup Workplace Connectors for environmental data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Provider Connector Configuration for Environmental sensors

Configure the provider connector configuration for setting up environmental sensors in workplace locations.

## Before you begin

Make sure that you have configured the sensor data providers for fetching environmental data from enviromental sensor providers or vendors. For more information, see [Configure sensor data providers](providers-occupancy.md).

**Note:** Seed data or out-of-the box table record is provided with the application and provides pre-filled values. If you want to create a new table record follow these steps.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Provider Connector Configuration**.

2.  Select **New**.

    On the form, fill in the fields:

<table id="table_gnt_qhf_t1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Name of the environmental sensor data provider. This field is auto-filled when the provider \(for example, Metrikus Spoke\).

</td></tr><tr><td>

Source Type

</td><td>

Option to specify the endpoint using which Workplace Connectors retrieves data from Metrikus or other environmental sensor data providers. Following options are available:-   Table
-   Webhook
-   External
-   RestAPI-Pull
For example, select **RestApi-pull**

</td></tr><tr><td>

Active

</td><td>

Option to select active provider connector configuration data. Only active records from the Provider Connector Configuration table are added or updated in the Provider Space Mapping table.By default, this option is set to **false**. Set this value to **true**.

</td></tr><tr><td>

Connector Configuration

</td><td>

Option to select required sensor items from the Connector Configuration table. For example, environmental.

</td></tr><tr><td>

Auto-refresh locations

</td><td>

Option to auto-refresh locations when spaces are added or when some spaces are removed from a selected location.

The scheduled Job **Refresh Provider Space Mapping records** runs daily and reads the **Auto Refresh Location** field in the Provider Connector Configuration table. It reads all records in the Provider Connector Configuration records and updates the Provider Space Mapping table with the latest data.

For example, if a new floor or a space is added to a location, then they're automatically added to a selected location.

</td></tr></tbody>
</table>3.  Filter spaces using the **Space Filter Condition**.

    Select **Preview** to see the results that your filter condition query returns. Select the link to view the matched space records in Workplace Connectors.

    For example, select **\[Space\]** from the list. Select the filter condition as **\[is\]** and manually enter the spaces **\[A1.001, A1.002, A1.003\]**.

    When a row is created or updated in the space filter conditions, the space records that meet the condition are loaded in the Provider Space Mapping table. A business rule runs in the background to fill the selected space records in the Provider Space Mappings table. For more information, see [Configure Provider Space Mapping for occupancy data](provider-space-mappings-occupancy.md).

4.  Select **Submit**.

    When a records are updated in the Provider Connector Configuration table, the selected spaces or location records are updated in the Provider Space Mapping table. The location records are updated with the location hierarchy \(Region, Campus, Building, floor, and space records\).


**Parent Topic:**[Setup Workplace Connectors for environmental data](../concept/setup-environmental-data-connectors.md)

**Previous topic:**[Set up Connector Configuration for Environmental sensor data](wsd-connectorconfiguration-environment.md)

**Next topic:**[Set up the Units of measure data table for environmental sensors](wsd-enviromental-unit-measure.md)

