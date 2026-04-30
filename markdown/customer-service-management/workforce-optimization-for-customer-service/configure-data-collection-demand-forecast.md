---
title: Configure the data collection to forecast the demand for resources
description: Define the data you want to collect for cases, interactions, or any table to forecast the number of agents that you require for your staffing needs.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up Demand Forecast in Workforce Optimization for Customer Service, Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Configure the data collection to forecast the demand for resources

Define the data you want to collect for cases, interactions, or any table to forecast the number of agents that you require for your staffing needs.

## Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

You must have the MetricBase plugin \[com.snc.clotho\] enabled to use Demand Forecast in Workforce Optimization for Customer Service. For more information, see [Requesting the MetricBase product](https://www.servicenow.com/docs/access?context=request-metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Note:**

-   When you change the forecast parameters or resource conversion formula, the new values for resource forecasts will not reflect on the team calendar until the **Forecast resources for future** scheduled job is executed. Your administrator can run the scheduled job on-demand to view the changes in the team calendar.
-   Once the **Historical data collection** job is run for specific data collection definitions, the column **Is historical data collected** in the Forecast Configurations \[sn\_agent\_forecast\_configuration\] table is set to **true**. Hence, the historical data collection will not run even if you add data for the past dates from the back-end. Historical data is stored for 1098 days for forecasts set at daily interval. Beyond three years, historical data is cleaned and cannot be saved.

Role required: sn\_agent\_forecast.admin

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Demand Forecast**.

2.  Define the data you want to collect for forecasting agents to resolve cases.

    1.  Click **Data Collection Definitions**.

        See the [Forecast Configuration table in Scheduling](../reference/components-installed-configurable-wfo-cs.md) for the list of configurations that are available by default.

    2.  Click **New**.
    3.  On the form, fill in the fields:

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

Data Collection Definition type is set to **Collection** by default and collects data using a scheduled job.

</td></tr><tr><td>

Table

</td><td>

Table that is used for collecting data. From the list, do one of the following:

 -   To collect data to forecast cases, select **Cases**.
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
    5.  Create an index for the table you have created using the date field and the conditions you have added to the table. For information on creating a table index, see [Create a table index](https://www.servicenow.com/docs/access?context=t_CreateCustomIndex&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
3.  Add parameters to be defined in the formula to calculate agent count per hour in a day.

    1.  Click **Formula Parameters**.
    2.  In the **Name** field, enter a name for the parameter.
    3.  Do one of the following:

        -   If you need to add a value to be calculated for the formula, in the **Value** field, enter the value.
        -   If you want to use the performance analytics score card API or a custom API, click **Advanced,** and add the script.
        The Average Case Work Time and Average Chat Work Time forecast parameters provided by default are examples of how you can use scripts to add the parameters. For a list of parameters provided by default, see [Forecast Parameters in Scheduling](../reference/components-installed-configurable-wfo-cs.md).

    4.  Click **Submit**.
4.  Configure the resource conversion formula.

    1.  Click **Resource Conversion Formula**.
    2.  Click **New**.
    3.  On the form, fill in the fields.

<table id="table_t1v_wqv_cnb"><thead><tr><th>

Field

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the resource forecast configuration.

</td></tr><tr><td>

Type

</td><td>

Type is set to **Resource Conversion Formula**.

</td></tr><tr><td>

Formula

</td><td>

Formula to calculate the forecasted number of agents that you need.In the Related Links section, do the following:

 -   Click **Browse Forecast Configuration**, select the forecast configuration to add to the formula and click **Add**.
-   Click the Browse Forecast Parameter, select the forecast parameter to add to the formula and click **Add**.

**Note:** **FC** refers to Forecast Configuration and **FP** refers to Forecast Parameter.

</td></tr></tbody>
</table>    4.  Click **Submit**.
5.  Associate an assignment group with a Resource Conversion Formula.

    You can assign a forecast configuration to multiple assignment groups, but an assignment group can have only one forecast configuration.

    1.  Click **Group Forecast Configurations**.
    2.  Click **New** and do the following:
        -   In the **Assignment Group** field, click the search icon and select the group to which you want to associate a forecast configuration.
        -   In the **Forecast Configuration** field, click the search icon and select a **Resource Conversion Formula**.

## What to do next

Run the **Collect historical data for demand forecast data collection definitions** scheduled job. For more information, see [Schedule jobs for Demand Forecast](../reference/components-installed-configurable-wfo-cs.md).

**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for Customer Service](../concept/configuring-demand-forecast-configurable-wfo-cs.md)

**Related topics**  


[Use Demand Forecast](../concept/scheduling-configurable-wfo-cs.md#)

