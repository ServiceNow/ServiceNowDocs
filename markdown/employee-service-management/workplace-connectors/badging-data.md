---
title: Badging Data
description: The Badging Data \[sn\_wsd\_wc\_badging\_data\] is the target table that contains the employee badging data and employee access records.
locale: en-US
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-02-28"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for badging data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Badging Data

The Badging Data \[sn\_wsd\_wc\_badging\_data\] is the target table that contains the employee badging data and employee access records.

## Before you begin

The **Process Provider Data Record** scheduled job runs periodically \(every five minutes\) and loads the badging data into the Badging Data table.

**Note:** The Employee Attendance Data table has been deprecated and a new table Badging Data table has been introduced to support MetricBase integration.

Role required: sn\_wsd\_wc.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Badging Readers** &gt; **Badging Data**.

2.  On the form, review the field details for badging data.

<table id="table_jsj_52d_n2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

The user workplace profile.

</td></tr><tr><td>

Location

</td><td>

Workplace location that is assigned to the user. The location data shows the complete location hierarchy \(Region, site, campus, buildings, floors, and spaces\).In the user workplace profile, the **Location** field must be updated with the correct location and the **Workplace entity** column is mapped to the user workplace profile.

</td></tr><tr><td>

Event Data

</td><td>

Time series data. Select this value to visualize the time-series data in different transforms. For more information, see [MetricBase transforms](https://www.servicenow.com/docs/access?context=metricbase-transforms&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

</td></tr></tbody>
</table>    The Badging Data table data is loaded to the Attendance Analytics table to generate space occupancy metrics in Workplace Central. For more information, see [Attendance Analytics](attendance-analytics.md).


**Parent Topic:**[Setup Workplace Connectors for badging data](../concept/setup-workplace-connectors.md)

**Previous topic:**[Configure a webhook event](configure-webhook-restapi.md)

**Next topic:**[Attendance Analytics](attendance-analytics.md)

