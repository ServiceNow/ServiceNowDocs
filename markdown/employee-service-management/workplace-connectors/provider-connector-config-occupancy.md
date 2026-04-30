---
title: Provider Connector Configuration
description: Register details for the occupancy data provider, the data source type, and connector configuration \(sensor\) details. Filter spaces using a condition builder, and retrieve occupancy data for a workplace location.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Provider Connector Configuration

Register details for the occupancy data provider, the data source type, and connector configuration \(sensor\) details. Filter spaces using a condition builder, and retrieve occupancy data for a workplace location.

## Before you begin

**Note:** If you’re using demo data or product data \(seed data\), some fields are pre-filled. In case, if you aren’t using the base system product data, you can configure the provider connector data table. The seed data is available as part of the Metrikus Spoke integration.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Administration** &gt; **Provider Connector Configuration**.

    ![Provider connector configuration.](../images/wsd-provider-connector-configuration.png)

2.  Select **New**.

    On the form, fill in the fields:

<table id="table_gnt_qhf_t1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Name of the occupancy data provider. This field is auto-filled when the Metrikus Spoke is installed and configured with the Flow Designer Integration Hub.

</td></tr><tr><td>

Connector Configuration

</td><td>

Option to select required sensor items from the Connector Configuration table. For example, Occupancy And Environment.

</td></tr><tr><td>

Source Type

</td><td>

Option to specify the endpoint using which Workplace Connectors retrieves data from Metrikus or other occupancy data spoke providers.Select **RestApi-pull**

</td></tr><tr><td>

Active

</td><td>

Option to select active provider connector configuration data. Only active records from the Provider Connector Configuration table are added or updated in the Provider Space Mapping table.By default, this option is set to **false**. Select the check box to set to **true**.

</td></tr><tr><td>

Auto-refresh locations

</td><td>

Option to auto-refresh locations when spaces are added or when some spaces are removed from a selected location.

The scheduled Job **Refresh Provider Space Mapping records** runs daily and reads the **Auto Refresh Location** field in the Provider Connector Configuration table. It reads all records in the Provider Connector Configuration records and updates the Provider Space Mapping table with the latest data.

If this option is selected, then spaces that are added to a location are synchronized with the Provider Space Mapping table. If spaces are removed, the occupancy sensor data record is removed from the connector list of the Provider Space Mapping table.

For example, if a floor or a space is added to a location, then they're automatically added to a selected location.

</td></tr><tr><td>

Metrics

</td><td>

Option to select the Space Occupancy metric value.

</td></tr></tbody>
</table>3.  Filter spaces using the **Space Filter Condition**.

    Select **Preview** to see the results that your filter condition query returns. Select the link to view the matched space records in Workplace Connectors.

    For example, select **\[Space\]** from the list. Select the filter condition as **\[is\]** and manually enter the spaces **\[A1.001, A1.002, A1.003\]**.

    When a row is created or updated in the space filter conditions, the space records that meet the condition are loaded in the Provider Space Mapping table. A business rule runs in the background to fill the selected space records in the Provider Space Mappings table. For more information, see [Configure Provider Space Mapping for occupancy data](provider-space-mappings-occupancy.md).

4.  Select **Submit**.

    When a records are updated in the Provider Connector Configuration table, the selected spaces or location records are updated in the Provider Space Mapping table. The location records are updated with the location hierarchy \(Region, Campus, Building, floor, and space records\).


**Parent Topic:**[Setup Workplace Connectors for occupancy data](../concept/setup-occupancy-connectors.md)

**Previous topic:**[Connector Configurations](connector-configuration-occupancy.md)

**Next topic:**[Provider Space Type Mappings](provider-space-type-mapping.md)

