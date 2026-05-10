---
title: Configure Demand Forecast
description: Define the data that you want to collect for incidents, interactions, or any table to forecast the number of agents that you require for your staffing needs.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Setting up, Demand Forecast, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Configure Demand Forecast

Define the data that you want to collect for incidents, interactions, or any table to forecast the number of agents that you require for your staffing needs.

## Before you begin

-   You must have the MetricBase plugin \[com.snc.clotho\] enabled to use Demand Forecast in Workforce Optimization for ITSM. For more information, see [Requesting the MetricBase product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/metricbase/request-metricbase.md).
-   You must be in the [Global scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_GlobalScope.md).

Role required: sn\_agent\_forecast.admin

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Demand Forecast**

2.  Define the data that you want to collect for forecasting the number of agents that you need.

    1.  Click **Data Collection Definitions**.

        See the [forecast configuration tables for demand forecast](../reference/configurable-wfo-itsm-demand-forecast-reference.md) for the list of configurations that are available by default.

    2.  Click New.
    3.  On the form, fill in the fields.

<table id="table_bxd_pnr_zmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the collection forecast configuration.

</td></tr><tr><td>

Type

</td><td>

Data Collection Definition type that is set to **Collection** by default and collects data using a scheduled job.

</td></tr><tr><td>

Table

</td><td>

Table that is used for collecting data. From the list, do one of the following:

 -   To collect data to forecast incidents, select **Incidents**.
-   To collect data to forecast interactions, select **Interactions**.


</td></tr><tr><td>

Condition

</td><td>

Conditions that you can set so that you can capture the data that you need.

</td></tr><tr><td>

Date Field

</td><td>

Data that you can add to forecast for the future.

</td></tr></tbody>
</table>    4.  Click **Submit**.

        **Note:** A forecast parameter in **Published** state is automatically created.

    5.  Create an index for the table that you have created using the date field and the conditions that you have added to the table. For information on creating a table index, see [Create a table index](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateCustomIndex.md).
3.  Add parameters for the formula to calculate how many agents you need per hour in a day.

    1.  Click **Formula Parameters**.
    2.  In the **Name** field, enter a name for the parameter.
    3.  Do one of the following:

        -   To add a value to be calculated for the formula, in the **Value** field, enter the value.
        -   To use the performance analytics score card API or a custom API, click **Advanced,** and add the script.
        The Average Chat Duration and Average Walkup Duration forecast parameters that are provided by default are examples of how you can use scripts to add the parameters. For a list of parameters provided by default, see the [forecast parameters in demand forecast](../reference/configurable-wfo-itsm-demand-forecast-reference.md) for the list of configurations that are available by default.

        **Note:** A resource conversion formula uses multiple data collection definitions to calculate the resource conversion. In a data collection definition, if the forecast parameters set for each of the forecast configurations vary, the resource conversion formula uses the lowest parameter values set for a forecast configuration.

        For example, let's assume:

        -   The P1 Incidents Created forecast configuration has the period length set to seven days and periods to forecast set to 2. Therefore, the next number of days for which the forecast would be calculated is 14 days.
        -   The Chat Interactions Created forecast configuration has the period length set to seven days and periods to forecast set to 4. Therefore, the next number of days for which the forecast would be calculated is 28 days.
        When you add both of these forecast configurations to the resource conversion formula, it only considers the lower of the two forecast configuration values, which is 14 days, to calculate the resource conversion.

    4.  Click **Submit**.
4.  Configure the resource conversion formula.

    1.  Click **Resource Conversion Formula**.
    2.  Click **New**.
    3.  On the form, fill in the fields.

<table id="table_t1v_wqv_cnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the resource forecast configuration.

</td></tr><tr><td>

Type

</td><td>

Type that is set to **Resource Conversion Formula**.

</td></tr><tr><td>

Formula

</td><td>

Formula to calculate the forecasted number of agents that you need.In the Related Links section, do the following:

 -   Click **Browse Forecast Configuration**, select the forecast configuration to add to the formula and click **Add**.
-   Click the **Browse Forecast Parameter** related link, select the forecast parameter to add to the formula, and click **Add**.

**Note:** **FC** refers to Forecast Configuration and **FP** refers to Forecast Parameter.

</td></tr></tbody>
</table>    4.  Click **Submit**.
5.  Associate an assignment group with a resource conversion formula.

    You can assign a forecast configuration to multiple assignment groups, but an assignment group can have only one forecast configuration.

    1.  Click **Group Forecast Configurations**.
    2.  Click **New** and do the following:
        -   In the **Assignment Group** field, click the search icon \(![Search icon](../image/search_icon.png)\) and select the group to which you want to associate a forecast configuration.
        -   In the **Forecast Configuration** field, click the search icon \(![Search icon](../image/search_icon.png)\) and select a **Resource Conversion Formula**.

## What to do next

Run the **Collect historical data for automated forecast configurations** scheduled job. For more information, see [scheduled jobs for demand forecast](../reference/configurable-wfo-itsm-demand-forecast-reference.md) .

-   **[Define the minimum and maximum number of agents to forecast demand](define-number-of-agents-configurable-wfo-itsm.md)**  
Set the minimum or maximum number of agents required per hour so that you always have the desired staffing coverage.

**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for ITSM](../concept/setting-up-demand-forecast-configurable-wfo-itsm.md)

**Related topics**  


[Use Demand Forecast](analyze-staffing-demand-forecast-wfo-itsm.md)

