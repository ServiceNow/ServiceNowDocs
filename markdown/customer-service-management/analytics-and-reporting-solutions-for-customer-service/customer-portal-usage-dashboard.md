---
title: Customer Portal Usage dashboard
description: The Customer Portal Usage dashboard enables you to understand the user usage of portals by presenting an aggregate count of sessions created every month.
locale: en-US
release: zurich
product: Analytics and Reporting Solutions for Customer Service
classification: analytics-and-reporting-solutions-for-customer-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Portal usage]
breadcrumb: [Customer Service Platform Analytics Solutions, Analytics and reporting, Customer Service Management]
---

# Customer Portal Usage dashboard

The Customer Portal Usage dashboard enables you to understand the user usage of portals by presenting an aggregate count of sessions created every month.

These sessions don’t represent individual users. For example, if you access the portal on two different days, it counts as two separate sessions. For more information about how an aggregate session is counted, see [Portal usage calculation](../reference/csm-portal-user-sessions-timeouts.md).

You can access the dashboard by navigating to **All** &gt; **Self Service** &gt; **Dashboards**. On the dashboard page, search and select `Customer Portal Usage`.

To access more detailed information, place your mouse device over any of the graphical reports. These graphs can be saved as PNG or JPEG files, enabling you to add them to emails or include them in your presentations. Additionally, all graphs can be updated to display the current data. An example of the dashboard layout is shown in the following image.

**Note:** The Customer Portal usage tab is available when the Customer Service \(com.sn\_customerservice\) plugin is activated.

![Customer portal usage dashboard. For descriptions of the reports included on this dashboard, see the Reports section that follows.](../image/customer-portal-usage-dashboard.png "Customer portal usage dashboard")

## End user and roles

<table id="table_csm_base_entities"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Administrator:

 -   Can edit the data
-   Can view the dashboard

</td><td>

admin

</td></tr></tbody>
</table>## Required definitions for Customer Portal Usage dashboard

<table id="table_dcc_th4_1cc"><thead><tr><th>

Definitions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DEFN1003689

</td><td>

Get all the guest portal session counts for yesterday.

 Frequency: Daily

 **Note:** Login pages are excluded from guest usage calculations.

</td></tr><tr><td>

DEFN1003690

</td><td>

Get all the bot portal session counts for yesterday.

 Frequency: Daily

</td></tr><tr><td>

DEFN1003691

</td><td>

Get all the external user portal session counts for yesterday.

 Frequency: Daily

</td></tr><tr><td>

DEFN1003724

</td><td>

Get aggregated chargeable external portal sessions for last month.

 Frequency: Monthly

</td></tr></tbody>
</table>