---
title: Set up Workplace Connectors for Wi-Fi data
description: Configure workplace Wi-Fi data sensors to capture the data from Wi-Fi providers to optimize space usage and efficiently manage workplace operations. You can use Wi-Fi data to determine the occupancy of spaces and attendance of employees in the office.
locale: en-US
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: concept
last_updated: "2024-09-19"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Set up Workplace Connectors for Wi-Fi data

Configure workplace Wi-Fi data sensors to capture the data from Wi-Fi providers to optimize space usage and efficiently manage workplace operations. You can use Wi-Fi data to determine the occupancy of spaces and attendance of employees in the office.

Wi-Fi data integrate with access points, enabling the tracking of device connectivity and disconnection events. For example, laptops, and mobile devices.

**Note:** Workplace Connectors customers are expected to build their own business use cases for using Wi-Fi data records.

-   **[Set up Connector Configuration for Wi-Fi data](../task/wsd-connectorconfig-wifi-data.md)**  
Configure the Connector Configurations table for loading the Wi-Fi data in the target Wi-Fi Access Data table \(sn\_wsd\_wc\_wifi\_access\_data\). The connector configuration table retrieves the data from different Wi-Fi data providers.
-   **[Provider Connector Configuration for Wi-Fi data](../task/wsd-provider-connectorconfig-wifi-data.md)**  
Configure the Provider Connector Configurations table for setting up Wi-Fi data in workplace locations.
-   **[Wi-Fi data table](../task/wsd-setup-wifi-data-table.md)**  
Retrieve the device name, access point, and connection date and time for a workplace location. The Workplace Connectors Wi-Fi data checks the occupancy of a workplace location.
-   **[Extension point definition for Wi-Fi data](../task/wsd-extension-point-definition-for-wifi-data.md)**  
Create a scripted extension point to process Wi-Fi access log data from the provider and convert it into a standard format. Confirm that each provider implements this extension.

**Parent Topic:**[Configure Workplace Connectors](configure-workplace-connectors.md)

**Previous topic:**[Extension point for occupancy and environment data](../task/extension-point-for-occupancy-and-environment-data.md)

**Next topic:**[Set up Connector Configuration for Wi-Fi data](../task/wsd-connectorconfig-wifi-data.md)

