---
title: Setup Workplace Connectors for Wi-Fi data
description: Configure workplace Wi-Fi data sensors to capture the data from Wi-Fi providers to optimize space usage and efficiently manage workplace operations. You can use Wi-Fi data to determine the occupancy of spaces and attendance of employees in the office.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Setup Workplace Connectors for Wi-Fi data

Configure workplace Wi-Fi data sensors to capture the data from Wi-Fi providers to optimize space usage and efficiently manage workplace operations. You can use Wi-Fi data to determine the occupancy of spaces and attendance of employees in the office.

Wi-Fi data integrate with access points, enabling the tracking of device connectivity and disconnection events. For example, laptops, and mobile devices.

**Note:** Workplace Connectors customers are expected to build their own business use cases for using Wi-Fi data records.

-   **[Setup Connector Configuration Wi-Fi data](setup-connector-configuration-wi-fi-data.md)**  
Configure the Connector Configurations table for loading the Wi-Fi data in the target Wi-Fi Access Data table \(sn\_wsd\_wc\_wifi\_access\_data\). The connector configuration table retrieves the data from different Wi-Fi data providers.
-   **[Provider Connector Configuration for Wi-Fi data](provider-connector-config-for-wi-fi-data.md)**  
Configure the Provider Connector Configurations table for setting up Wi-Fi data in workplace locations.
-   **[Wi-Fi data table](wsd-wi-fi-data-table.md)**  
Retrieve the device name, access point, and connection date and time for a workplace location. The Workplace Connectors Wi-Fi data checks the occupancy of a workplace location.
-   **[Extension point definition for Wi-Fi data](../task/extension-point-definition-for-wi-fi-data-wsd.md)**  
Create a scripted extension point to process Wi-Fi access log data from the provider and convert it into a standard format. Confirm that each provider implements this extension.

**Parent Topic:**[Configure Workplace Connectors](configure-workplace-connectors.md)

**Previous topic:**[Extension point for occupancy and environment data](../task/extension-point-for-occupancy-environment-data.md)

**Next topic:**[Setup Connector Configuration Wi-Fi data](setup-connector-configuration-wi-fi-data.md)

