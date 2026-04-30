---
title: Demand Forecast components in Workforce Optimization for ITSM
description: Workforce Optimization for ITSM installs roles to administer ITSM Manager Workspace Demand Forecast, properties to configure default behavior, scheduled jobs to collect data for the configurations, tables to store data, forecast configurations to collect data for incidents and interactions and a retention policy to store metric data.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up Demand Forecast in Workforce Optimization for ITSM, Demand Forecast in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Demand Forecast components in Workforce Optimization for ITSM

Workforce Optimization for ITSM installs roles to administer ITSM Manager Workspace Demand Forecast, properties to configure default behavior, scheduled jobs to collect data for the configurations, tables to store data, forecast configurations to collect data for incidents and interactions and a retention policy to store metric data.

## Forecast configurations

|Name|Description|
|----|-----------|
|Chat Interactions Created|Collects data for chat interactions.|
|Non P1 Incidents Created|Collects data for all incidents that are not tagged as priority 1.|
|P1 Incidents Created|Collects data for priority 1 incidents.|
|Walkup Interactions Created|Collects data for walk up interactions.|

## Metric retention policy

The **WFO Forecast** time series metric retention policy is available by default for all forecast configurations. By default, this retention policy stores data at a one-hour interval for the past three years.

## Formulas to create resource forecast configurations

|Name|Formula to create this resource forecast configuration|
|----|------------------------------------------------------|
|Chat Interactions to Agent Conversion|`([FC:Chat Interactions Created] * [FP:Average Chat Duration]) / [FP:Average Agent Work Time Per Day]`|
|Incident and Interaction Resources|`[FC:Incidents Created to Agent Conversion] + [FC:Chat Interactions to Agent Conversion] + [FC:Walkup Interactions to Agent Conversion]`|
|Incidents Created to Agent Conversion|`(([FC:P1 Incidents Created] * [FP:Average P1 Incident Work Time]) / [FP:Average Agent Work Time Per Day]) + (([FC:Non P1 Incidents Created] * [FP:Average Non P1 Incident Work Time]) / [FP:Average Agent Work Time Per Day])`|
|Walkup Interactions to Agent Conversion|`([FC:Walkup Interactions Created] * [FP:Average Walkup Duration]) / [FP:Average Agent Work Time Per Day]`|

## Forecast parameters

|Name|Description|
|----|-----------|
|Average Agent Work Time Per Day|Average time an agent works in a given day.|
|Average Chat Duration|Average duration of an agent chat for each incident or interaction.|
|Average Non P1 Incident Work Time|Average time an agents spends working on all incidents that are not categorized as Priority 1.|
|Average P1 Incident Work Time|Average time an agents spends working on all incidents that are categorized as Priority 1.|
|Average Walkup Duration|Average duration an agent spends on a walkup interaction.|

If you create forecast parameters for a forecast configuration, the values set in the configuration are used instead of the default forecast parameters listed in the forecast properties section. For information on configuring forecast parameters, see [Modify forecast parameters to visualize forecast data](../task/modify-forecast-parameters-configurable-wfo-itsm.md)

## Forecast properties

<table id="table_nbp_f5x_2nb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

sn\_agent\_forecast.historical\_data\_points

</td><td>

The hourly historical data points to be used for the forecast.

 The maximum allowed data points is 26280. The default value is 8760 and represents the hourly data points for a one year time period \(24 hours x 365 days x 1 year\).

</td><td>

For example: 24 hours x 365 days x 3 years = 26280

</td></tr><tr><td>

sn\_agent\_forecast.seasonal\_frequency

</td><td>

The seasonal frequency of a repeated pattern. The default value is 168.

</td><td>

For example:

-   Daily data pattern = 1\*24 = 24
-   Weekly data pattern = 7 \* 24 = 168
-   Monthly data pattern = 30 \* 24 = 720

</td></tr><tr><td>

sn\_agent\_forecast.forecast\_periods

</td><td>

The number of periods/seasons to forecast. A period is the length of a season.The default value is 5.

</td><td>

For example:

-   If the length of a season is daily which is equal to 24 hours \(1 day\) and the forecast period is 30, then the number of periods to forecast is equal to 24 \* 30 = 720 hours.
-   If the length of a season is weekly which is equal to 168 hours \(1 week\) and the forecast period is 5, then the number of periods to forecast is equal to 168 \* 5 = 840 hours.

</td></tr><tr><td>

sn\_agent\_forecast.number\_of\_historical\_days\_in\_timeseries\_chart

</td><td>

The number of historical days that will be plotted in the time-series chart in Manager Workspace.

</td><td>

For example, if the number is set to 90,then the number of days is counted from the current day to 90 days ago.

</td></tr></tbody>
</table>## Roles for Demand Forecast

<table id="table_jx5_c3c_3nb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Forecast admin \[sn\_agent\_forecast.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) forecast configuration tables.

</td><td>

-   sn\_agent\_forecast.users
-   clotho\_admin

</td></tr><tr><td>

Forecast user \[sn\_agent\_forecast.user\]

</td><td>

Grants read access to forecast configuration tables.

</td><td>

 

</td></tr></tbody>
</table>## Tables for Demand Forecast

|Table|Description|
|-----|-----------|
|Forecast Configuration \[sn\_agent\_forecast\_configuration\]|Define data collection definition and resource conversion formula configurations.|
|Forecast Parameter \[sn\_agent\_forecast\_parameter\]|Define forecast parameters required for the formula.|
|Forecast Configuration group \[sn\_agent\_forecast\_configuration\_m2m\_sys\_user\_group\]|Associate resource conversion formula with assignment groups.|

## Forecast configurations available by default

By default, forecast configurations are available for the following groups:

-   Deskside Support
-   IT Service Desk
-   Application Support
-   Technical Support

## Schedule jobs for Demand Forecast

<table id="table_up4_kj2_1nb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Collect historical data for automated forecast configurations**

</td><td>

-   On-demand job to collect historical data​
-   Collects historical data daily for every hour for the past three years

</td></tr><tr><td>

**Collect daily data for automated forecast configurations**

</td><td>

-   Runs daily at 2 am
-   For each table defined in the Data Collection Definition configuration, it fetches the records from the previous day for each hour for every group and stores it in the MetricBase
-   You can access the time series for the collected data using the MetricBase list command on the Group \[sys\_user\_group\] table
-   Uses the WFO Forecast retention policy for data retention

</td></tr><tr><td>

**Forecast resources for future**

</td><td>

Calculates the forecast resources for the future based on the collected data. -   Runs daily at 3 am
-   Collects hourly data every day for the formula forecast configuration
-   Stores the data in the Agent Forecast metric in MetricBase
-   Uses forecast properties to set the data collection frequency or time period to store the data. The forecast properties will not be used if a [published forecast parameter](../task/modify-forecast-parameters-configurable-wfo-itsm.md) exists for a data collection definition.

</td></tr></tbody>
</table>**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for ITSM](../concept/setting-up-demand-forecast-configurable-wfo-itsm.md)

