---
title: Setup Connector Configuration Wi-Fi data
description: Configure the Connector Configurations table for loading the Wi-Fi data in the target Wi-Fi Access Data table \(sn\_wsd\_wc\_wifi\_access\_data\). The connector configuration table retrieves the data from different Wi-Fi data providers.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-09-02"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for Wi-Fi data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Setup Connector Configuration Wi-Fi data

Configure the Connector Configurations table for loading the Wi-Fi data in the target Wi-Fi Access Data table \(sn\_wsd\_wc\_wifi\_access\_data\). The connector configuration table retrieves the data from different Wi-Fi data providers.

## Before you begin

Make sure that a table data record exists for the Wi-Fi data.

**Note:** The application comes with seed data, or base system table records, that include pre-filled values for Wi-Fi data.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Connector Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_w14_z4w_tcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target Table

</td><td>

Target or destination table to store the Wi-Fi data.Select the Wi-Fi Data \(sn\_wsd\_wc\_wifi\_access\_data\) table.

</td></tr><tr><td>

Type

</td><td>

Type of sensor data. Select Wi-Fi from the list.

</td></tr><tr><td>

Extension Point Definition

</td><td>

Extension point definition for the Wi-Fi data. Search using the lookup list icon \(![Lookup list icon.](../images/wsd-lookup-list-icon.png)\) to locate the extension point definition **WifiAccessLogDataHandler**.

</td></tr><tr><td>

Stale time \(in minutes\)

</td><td>

Time \(in minutes\) beyond which data is considered stale.Beyond this time, fresh data is fetched from the data provider table. For example, 5 minutes. The application fetches data every 5 minutes.

</td></tr><tr><td>

Supported Metrics

</td><td>

Target record for supported metrics. Select Event Data.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Setup Workplace Connectors for Wi-Fi data](setup-workplace-connectors-for-wi-fi-data.md)

