---
title: Set up forecast schedule
description: Forecast schedule automatically fetches all the opportunities in the system and generates forecast data.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-04-02"
reading_time_minutes: 1
breadcrumb: [Configure Sales Forecasting, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Set up forecast schedule

Forecast schedule automatically fetches all the opportunities in the system and generates forecast data.

## Before you begin

Create a scheduled job to update or create the forecast data at a specific time or recurring schedule. A default sales forecast scheduler is available with the Sales Forecasting application. You can edit that scheduler according to your requirements.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Job**.

2.  Enter **Sales forecast schedule** in the Search field.

3.  Select **Sales forecast schedule** from the schedule list.

4.  From the Run list, select the option to customize the timing of the scheduler according to your requirements.

    ![Forecast scheduler](../image/forecast-scheduler.png)

5.  Select **Update** to save the settings of your scheduler.

6.  Select **Execute Now** to run the scheduler.

    **Note:**

    You can copy the script provided in the Run this script field to create your own scheduler.


