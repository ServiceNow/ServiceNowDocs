---
title: Setup Workplace Connectors for badging data
description: As a Workplace Connectors administrator, configure Workplace Connectors to import data from workplace badging data records. For example, badging data from badging spokes.
locale: en-US
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Setup Workplace Connectors for badging data

As a Workplace Connectors administrator, configure Workplace Connectors to import data from workplace badging data records. For example, badging data from badging spokes.

The badging vendor Spoke is designed to handle badging data from a specific vendor. It utilizes a badging data table as the source for retrieving the data. It also allows for importing CSV data files through the SFTP method. A scheduled import set is used to transform the file and populate the Badging Data table.

Workplace Connector provides analytics capabilities to analyze employee attendance data. The scheduled job **Process Provider Data Record** runs every 5 minutes to fetch data and populate the Employee Attendance table.

## Badging data analytics requirement

-   Ensure that employees have an employee workplace profile.
-   Workplace locations are assigned to employee workplace profile.

**Note:** For more information about how to implement the Workplace Connectors framework and badging sensor data, see Workplace Connectors Implementation Guide V1.0 Aug 2023 on the ServiceNow Community.

1.  [Create a badging data provider](../task/wsd-connector-badging-providers.md)  
Configure and add a new provider to fetch the badging data.
2.  [Configure connector configuration for badging data](../task/workplace-connector-configuration.md)  
Configure the connector configuration table \[sn\_wsd\_wc\_connector\_config\] to fetch the badging spoke data records.
3.  [Provider connector configuration](provider-configuration-ovw.md)  
To register details for a new provider, configure a provider to import data from a badging table or use the web hook APIs. The badging data is shared with Workplace Connectors by badging vendors. The badging data is processed and transformed to derive space occupancy metrics in your organization.
4.  [Badging Data](../task/badging-data.md)  
The Badging Data \[sn\_wsd\_wc\_badging\_data\] is the target table that contains the employee badging data and employee access records.
5.  [Attendance Analytics](../task/attendance-analytics.md)  
The Attendance analytics table computes badging data based on the employee head count at the region, site, campus, and building level. It derives occupancy data from the Badging Data table.
6.  [Extension point for badging data](../task/extension-point-for-badging-data.md)  
Create a scripted extension point to process badging data from the provider and convert it into a standard format. Confirm that each provider implements this extension.

**Parent Topic:**[Configure Workplace Connectors](configure-workplace-connectors.md)

**Previous topic:**[Configure badging data choices](../task/configure-badging-data-choices.md)

**Next topic:**[Create a badging data provider](../task/wsd-connector-badging-providers.md)

