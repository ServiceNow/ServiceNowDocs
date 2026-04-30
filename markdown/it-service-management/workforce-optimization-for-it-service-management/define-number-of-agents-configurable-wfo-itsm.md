---
title: Define the minimum and maximum number of agents to forecast demand
description: Set the minimum or maximum number of agents required per hour so that you always have the desired staffing coverage.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure Demand Forecast, Setting up Demand Forecast in Workforce Optimization for ITSM, Demand Forecast in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Define the minimum and maximum number of agents to forecast demand

Set the minimum or maximum number of agents required per hour so that you always have the desired staffing coverage.

## Before you begin

Role required: sn\_agent\_forecast\_admin

## About this task

When you calculate the number of agents for your staffing needs, you have the option of defining how many minimum or maximum number of agents you would need by default per hour using the `Math.min` and the `Math.max` functions.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Demand Forecast** &gt; **Formula Parameters**.

2.  Create a formula parameter to set either the minimum or maximum number of agents you need every hour.

    1.  Click **New**.
    2.  In the **Name** field, enter a unique name for the parameter.
    3.  In the **Value** field, enter the number of agents required when converting resources.
        -   To set the minimum number of agents, enter the lowest number of agents you would require per hour.
        -   To set the maximum number of agents, enter the highest number of agents you would require per hour.
    4.  Click **Submit**.
3.  Create a Resource Conversion formula.

    1.  Click **Resource Conversion Formula**.
    2.  Click **New**.
    3.  in the **Name** field, enter a unique name for the resource conversion formula.
    4.  Right-click the form header and click **Save**.
    5.  In the **Formula** field, do one of the following:
        -   To create a formula for the minimum number of agents required per hour:

            1.  Add the `Math.max` function.
            2.  Click **Browse Formula Parameters** and select the formula you have created to set the minimum number of agents.
            3.  Click **Browse Forecast Configuration** and select the formula you want to use for the forecast configuration.
            When the resource conversion formula is calculated, the higher of the two values is used as the lower limit for the minimum number of agents required per hour.

            For example, let's assume you need a minimum of two agents per hour and you're using the following formula: `Math.max(([FP:Min Number of Agents]), (([FC:Chat Interactions Created] * [FP:Average Chat Duration]) / [FP:Average Agent Work Time Per Day]))`, where,

            -   You've set the `[FP:Min Number of Agents]` value to `2`.
            -   The output value for this formula `[FC:Chat Interactions Created] * [FP:Average Chat Duration]) / [FP:Average Agent Work Time Per Day]` is `0`.
            Although the forecast configuration indicates that no agents are required, because you've set the minimum number of agents to two, that value will be used for resource conversion.

        -   To create a formula for the minimum number of agents required per hour:

            1.  Add the `Math.min` function.
            2.  Click **Browse Formula Parameters** and select the formula you have created to set the maximum number of agents.
            3.  Click **Browse Forecast Configuration** and select the formula you want to use for the forecast configuration.
            When the resource conversion formula is calculated, the lower of the two values is used as the upper limit for the minimum number of agents required per hour.

            For example, let's assume you need a maximum of eight agents per hour and you're using the following formula: `Math.min(([FP:Max Number of Agents]), (([FC:Chat Interactions Created] * [FP:Average Chat Duration]) / [FP:Average Agent Work Time Per Day]))`, where,

            -   You've set the `[FP:Max Number of Agents]` value to `8`.
            -   The output value for this formula `[FC:Chat Interactions Created] * [FP:Average Chat Duration]) / [FP:Average Agent Work Time Per Day]` is `10`.
            Although the forecast configuration indicates that 10 agents are required, because you've set the maximum number of agents to eight, that value will be used for resource conversion.

    6.  Click **Submit**.

**Parent Topic:**[Configure Demand Forecast](configure-data-collection-configurable-wfo-itsm.md)

