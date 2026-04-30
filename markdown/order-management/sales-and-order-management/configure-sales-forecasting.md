---
title: Configure Sales Forecasting
description: Use the Sales Forecasting application to project your future sales volumes and revenue based data from opportunities and pipeline analysis.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-03-31"
reading_time_minutes: 1
breadcrumb: [Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configure Sales Forecasting

Use the Sales Forecasting application to project your future sales volumes and revenue based data from opportunities and pipeline analysis.

## Activate Sales Forecasting

As an admin, you can activate the following plugins to enable users to access Sales Forecasting. For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_o13_hpv_v2c"><thead><tr><th>

Plugin

</th><th>

Description

</th><th>

Dependency

</th></tr></thead><tbody><tr><td>

com.snc\_sales\_forecasting

</td><td>

Project your future sales volumes and revenue based on data from opportunities and pipeline analysis.

</td><td>

-   com.snc\_app-l2c-core
-   com.snc\_app-prd-pm
-   com.snc\_app\_l2c\_oppty\_mgmt
-   com.snc\_app-tmt-core

</td></tr><tr><td>

com.sn\_sales\_quota\_application

</td><td>

Assign the quota targets to the sales reps in the sales team hierarchy.

</td><td>

com.snc\_app\_l2c\_oppty\_mgmt

</td></tr></tbody>
</table>You need the Sales Quota Application plugin to assign the quota targets to each team and sales agent. You can view and track the targets achieved for each agent and team on the sales forecasting dashboard and the gap remaining to achieving the target.

<table id="table_j2b_kqv_v2c"><thead><tr><th>

Role

</th><th>

ID

</th><th>

Functions

</th></tr></thead><tbody><tr><td>

Forecast Administrator

</td><td>

sn\_sales\_forecast.forecast\_admin

</td><td>

-   Setup group hierarchy and sales teams with the managers and sales agents’ information for the organization.
-   Set up Sales forecasting settings and be able to initiate calculate forecasts.
-   Create/edit/view forecast category choices and forecast model details.

</td></tr><tr><td>

Forecast Contributor 

</td><td>

sn\_sales\_forecast.forecast\_contributor

</td><td>

View forecast item entries for the owner and the people under their hierarchy only.

</td></tr><tr><td>

Forecast Analyst

</td><td>

sn\_sales\_forecast.forecast\_analyst

</td><td>

View all forecasts item entries, forecast category, forecast model and associated opportunities.

</td></tr><tr><td>

Sales Quota Admin

</td><td>

sn\_quota\_core.quota\_admin

</td><td>

Create/import/edit/delete quota for different sales teams and individuals.

</td></tr><tr><td>

Sales Quota Manager

</td><td>

sn\_quota\_core.quota\_manager

</td><td>

Edit the sales quota for the groups.

</td></tr><tr><td>

Sales Quota Owner

</td><td>

sn\_quota\_core.quota\_owner

</td><td>

View the Sales quota assigned to the owner.

</td></tr></tbody>
</table>