---
title: Configure Workplace Connectors
description: Configure Workplace Connectors to complete the installation and setup tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-connectors/configure-workplace-connectors.html
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Configure Workplace Connectors

Configure Workplace Connectors to complete the installation and setup tasks.

1.  [Install Workplace Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/install-workplace-connectors.md)  
Install the Workplace Connectors application from the ServiceNow Store.
2.  [Configure sensor data providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/providers-occupancy.md)  
Configure sensor data providers in Workplace Connectors for retrieving the workplace sensor data from third-party data providers.
3.  [Configure data Sources and schedule imports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/import-data-connector.md)  
Set up the data source for the integration framework \(for example, badging spoke data\) and schedule the import job to retrieve data from the data source periodically.
4.  [Configure badging data choices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/configure-badging-data-choices-table.md)  
The Badging Data Choices table \(sn\_wsd\_wc\_badging\_data\_choice\) contains the badging status details for Swipe-in and Swipe-out event types. You can create multiple badging states and assign the appropriate event type.
5.  [Setup Workplace Connectors for badging data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/setup-workplace-connectors.md)  
As a Workplace Connectors administrator, configure Workplace Connectors to import data from workplace badging data records. For example, employee attendance data from badging spokes.
6.  [Setup Workplace Connectors for occupancy data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/setup-occupancy-connectors.md)  
Configure workplace connectors to provide workplace occupancy data.
7.  [Setup Workplace Connectors for environmental data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/setup-environmental-data-connectors.md)  
Configure the workplace environment data sensors to retrieve and fetch air quality and temperature data for a workplace. Define the units to measure air quality and temperature in the Unit of Measure table \[sn\_wsd\_wc\_unit\_of\_measure\]. The units are added in the Environmental data table.
8.  [Setup Workplace Connectors for Wi-Fi data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/setup-workplace-connectors-for-wi-fi-data.md)  
Configure workplace Wi-Fi data sensors to capture the data from Wi-Fi providers to optimize space usage and efficiently manage workplace operations. You can use Wi-Fi data to determine the occupancy of spaces and attendance of employees in the office.
9.  [Execute the Temperature Beyond Threshold MetricBase trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/execute-the-temperature-beyond-threshold-metricbase-trigger.md)  
Monitor temperature thresholds using the Temperature Beyond Threshold MetricBase trigger, which reads the time-series data from the Occupancy and Environment Data MetricBase data and initiates Workflow Studio flows. This MetricBase Trigger sends the email notification to the concerned person or group when the temperature in a space exceeds the defined threshold.

**Parent Topic:**[Workplace Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/workplace-connectors-landing-page.md)

**Previous topic:**[Exploring Workplace Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/explore-workplace-connectors.md)

**Next topic:**[Install Workplace Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/install-workplace-connectors.md)

