---
title: Setup Workplace Connectors for occupancy data
description: Configure workplace connectors to provide workplace occupancy data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-connectors/setup-occupancy-connectors.html
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Setup Workplace Connectors for occupancy data

Configure workplace connectors to provide workplace occupancy data.

Workplace Occupancy data provides real-time insights on workplace space and resource optimization. It uses the occupancy data from the occupancy connectors or sensors installed at a workplace location. The occupancy data is provided by third-party occupancy sensor data providers. For example, Metrikus Spoke is integrated with Flow Designer Integration Hub. The external Ids from Metrikus Spoke are mapped with Workplace Connectors locations to fetch the occupancy data.

**Note:** Customers who aren’t using the Metrikus Spoke must build their own integration to get Occupancy data insights for locations provided in Workplace Connectors locations.

Workplace occupancy connector data provides the following benefits;

-   Automatically checks in a reservation based on the space occupancy data and reservation status. For example, Occupied, unoccupied, reservation is in progress, reservation is canceled, and so on. For more information, see [Configure automatic check-in for reserved spaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-reservation-management/configure-rsv-check-in.md).
-   Provides near-real time occupancy data on floor maps, Employees can reserve spaces based on Occupancy data and reservation data.

1.  [Activate Metrikus Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/install-metrikus-plugin.md)  
Activate the Metrikus Spoke plugin from the ServiceNow Store.
2.  [Integrate Metrikus spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/integrate-metrikus-flowdesigner.md)  
Integrate Metrikus Spoke with Flow Designer Integration Hub to retrieve occupancy data for workplace locations.
3.  [Connector Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/connector-configuration-occupancy.md)  
Configure the Connector Configurations table for loading the occupancy data in the target Space Occupancy Data table \(sn-wsd\_wc\_space\_occupancy\). Connector configuration table retrieves the sensor data from different occupancy data providers.
4.  [Provider Connector Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/provider-connector-config-occupancy.md)  
Register details for the occupancy data provider, the data source type, and connector configuration \(sensor\) details. Filter spaces using a condition builder, and retrieve occupancy data for a workplace location.
5.  [Provider Space Type Mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/provider-space-type-mapping.md)  
This table maps workplace space types or locations with external ids provided by the space occupancy data providers.
6.  [Configure Provider Space Mapping for occupancy data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/provider-space-mappings-occupancy.md)  
The Provider Space Mapping data table stores the workplace locations and external Ids provided by the occupancy data provider.
7.  [Retrieving Action Configurations data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/actions-configurations-occupancy.md)  
Retrieve Actions from occupancy data provider using Flow Designer Integration Hub. Specify the transform definitions and invoke the Sub flow to retrieve Occupancy data. For example, Metrikus Spoke integration. The occupancy sensor data from the Occupancy data provider is transformed to derive space occupancy data in Workplace Connectors.
8.  [Retrieving Space Occupancy Data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/space-occupancy-data.md)  
Retrieve the Space Occupancy Data table for loading workplace occupancy data and space occupancy data insights for a selected workplace location.

**Parent Topic:**[Configure Workplace Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/configure-workplace-connectors.md)

**Previous topic:**[Extension point for badging data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/extension-point-badging-data.md)

**Next topic:**[Activate Metrikus Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/install-metrikus-plugin.md)

