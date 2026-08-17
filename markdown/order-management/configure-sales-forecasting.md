---
title: Configure Sales Forecasting
description: Use the Sales Forecasting application to project your future sales volumes and revenue based data from opportunities and pipeline analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-sales-forecasting.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Configure Sales Forecasting

Use the Sales Forecasting application to project your future sales volumes and revenue based data from opportunities and pipeline analysis.

## Activate Sales Forecasting

As an admin, you can activate the following plugins to enable users to access Sales Forecasting. For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

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
</table>You need the Sales Quota Application plugin to assign the quota targets to each team and sales agent. You can view and track the targets achieved for each agent and team on the sales forecasting dashboard and the gap remaining to achieve the target.

**Related topics**  


[Using Sales Forecasting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-sales-forecasting.md)

[Sales Forecasting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-forecasting.md)

