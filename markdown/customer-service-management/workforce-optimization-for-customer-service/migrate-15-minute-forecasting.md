---
title: Migrate to 15-minute forecasting
description: Migrate to 15-minute demand forecasting that enables managers to view their agent staffing forecast at 15-minute intervals on the team calendar.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Demand Forecast, Configure, Workforce Optimization for Customer Service, Customer Service Management]
---

# Migrate to 15-minute forecasting

Migrate to 15-minute demand forecasting that enables managers to view their agent staffing forecast at 15-minute intervals on the team calendar.

## Before you begin

Role required: admin

## About this task

Starting with the Tokyo release, 15-minute forecasting is the default forecasting feature. Existing customers can migrate from the 60-minute forecasting to 15-minute forecasting using the following procedure.

## Procedure

1.  Set the **sn\_agent\_forecast.forecast\_interval** system property value to `15`.

    1.  Set the application scope to Agent Forecast using the [application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

    2.  Enter `sys_properties.list` in the navigation filter, and then open the **sn\_agent\_forecast.forecast\_interval** property.

    3.  In the **Value** field, enter `15`.

    4.  Click **Update**.

2.  Deactivate the existing demo data definitions.

    1.  Navigate to **All** &gt; **Workforce Optimization** &gt; **Demand Forecast** &gt; **Data Collection Definitions**.

    2.  Set the **Active** value of **Cases Assigned** and **Chat Interaction Created** demo definitions to **false**.

3.  Create new data collection definitions, formula parameters, and group forecast configuration.

    For more info, see [Configure the data collection for resources demands](configure-data-collection-demand-forecast.md).

4.  Run the **Collect historical data** on-demand job to collect historical data at 15-minute interval.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for **Collect historical data** and select it.

    3.  Click **Execute Now**.

5.  Run the **Forecast resources for future** scheduled job for staffing forecast that can be viewed on team calendar.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for **Forecast resources for future** and select it.

    3.  Click **Execute Now**.


**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for Customer Service](../concept/configuring-demand-forecast-configurable-wfo-cs.md)

