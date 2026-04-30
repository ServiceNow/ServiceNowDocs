---
title: Provider Connector Configuration for Wi-Fi data
description: Configure the Provider Connector Configurations table for setting up Wi-Fi data in workplace locations.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-09-02"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Connectors for Wi-Fi data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Provider Connector Configuration for Wi-Fi data

Configure the Provider Connector Configurations table for setting up Wi-Fi data in workplace locations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Provider Connector Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_mfl_mqw_tcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Name of the Wi-Fi data provider \(for example, Genetec\).

</td></tr><tr><td>

Source Type

</td><td>

Option to specify the endpoint using which Workplace Connectors retrieves data from Genetec or other Wi-Fi data providers. For example, select **RestApi-pull**.

</td></tr><tr><td>

Active

</td><td>

Option to select active provider connector configuration data. Only active records from the Provider Connector Configuration table are added or updated in the Provider Space Mapping table.By default, this value is set to **false**. Set this value to **true**.

</td></tr><tr><td>

Connector Configuration

</td><td>

Option to select required sensor items from the Connector Configuration table. For example, Wifi.

</td></tr><tr><td>

Callback URL

</td><td>

This applies only when the Source Type is Webhook.

</td></tr><tr><td>

Auto-refresh locations

</td><td>

Option to auto-refresh locations when spaces are added or when some spaces are removed from a selected location.The scheduled Job **Refresh Provider Space Mapping records** runs daily and reads the **Auto Refresh Location** field in the Provider Connector Configuration table. It reads all records in the Provider Connector Configuration records and updates the Provider Space Mapping table with the latest data. For example, if a new floor or a space is added to a location, then they're automatically added to a selected location.

</td></tr><tr><td>

Token Param Name

</td><td>

Token parameter name.

</td></tr><tr><td>

Token Value

</td><td>

Token value.

</td></tr><tr><td>

Metrics

</td><td>

Metric table.

</td></tr></tbody>
</table>4.  Filter spaces using the **Space Filter Condition**.

    Select **Preview** to see the results that your filter condition query returns. Select the link to view the matched space records in Workplace Connectors.

    For example, select **Space** from the list. Select the filter condition as **\[is\]** and manually enter the spaces **A1.001, A1.002, A1.003**.

    When a row is created or updated in the space filter conditions, the space records that meet the condition are loaded in the Provider Space Mapping table. A business rule runs in the background to fill the selected space records in the Provider Space Mappings table.

5.  Select **Submit**.

    When records are updated in the Provider Connector Configuration table, the selected spaces or location records are updated in the Provider Space Mapping table. The location records are updated with the location hierarchy \(Region, Campus, Building, floor, and space records\).


**Parent Topic:**[Setup Workplace Connectors for Wi-Fi data](setup-workplace-connectors-for-wi-fi-data.md)

