---
title: Setup Workplace Connectors for environmental data
description: Configure the workplace environment data sensors to retrieve and fetch air quality and temperature data for a workplace. Define the units to measure air quality and temperature in the Unit of Measure table \[sn\_wsd\_wc\_unit\_of\_measure\]. The units are added in the Environmental data table.
locale: en-US
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Setup Workplace Connectors for environmental data

Configure the workplace environment data sensors to retrieve and fetch air quality and temperature data for a workplace. Define the units to measure air quality and temperature in the Unit of Measure table \[sn\_wsd\_wc\_unit\_of\_measure\]. The units are added in the Environmental data table.

Workplace Connectors Environmental data table \(sn\_wsd\_wc\_space\_environment\) checks for workplace air quality and temperature. It checks for Carbon dioxide and Ozone levels along with temperature, and relative Humidity value at a workplace location.

**Note:** Workplace Connectors customers are expected to build their own environmental data framework for using Environmental sensor data records. For more information about how to implement the Workplace Connectors framework and environmental sensor data, see Workplace Connectors Implementation Guide V1.0 Aug 2024 on the ServiceNow Community.

1.  [Set up Connector Configuration for Environmental sensor data](../task/wsd-connectorconfiguration-environment.md)  
Configure the Connector Configurations table for loading the Environmental data. Connector configuration table retrieves the sensor data from different environmental sensor data providers.
2.  [Provider Connector Configuration for Environmental sensors](../task/wsd-env-provider-connectorconfig.md)  
Configure the provider connector configuration for setting up environmental sensors in workplace locations.
3.  [Set up the Units of measure data table for environmental sensors](../task/wsd-enviromental-unit-measure.md)  
Configure the unit of measure for air quality \(Carbon dioxide and Ozone metric\) and temperature units \(degree celsius and micrograms per cubic meter\) for a workplace location. The Workplace Connectors environmental sensors checks for the air and temperature quality metrics in a workplace location.
4.  [Configure environmental sensor data for a workplace location](../task/config-connectors-env-sensor.md)  
Create environmental sensor data for a workplace location in Workplace Connectors. The Occupancy and Environment Data \(sn\_wsd\_wc\_occ\_env\_data\) table checks for carbon dioxide value, ozone, sound, light, temperature, pressure, and humidity levels at a workplace location. You can also view the time-series data for each value that is retrieved from the MetricBase.
5.  [Extension point for occupancy and environment data](../task/extension-point-for-occupancy-and-environment-data.md)  
Create a scripted extension point to process occupancy and environment data from the provider and convert it into a standard format. Confirm that each provider implements this extension.

**Parent Topic:**[Configure Workplace Connectors](configure-workplace-connectors.md)

**Previous topic:**[Retrieving Space Occupancy Data](../task/space-occupancy-data.md)

**Next topic:**[Set up Connector Configuration for Environmental sensor data](../task/wsd-connectorconfiguration-environment.md)

