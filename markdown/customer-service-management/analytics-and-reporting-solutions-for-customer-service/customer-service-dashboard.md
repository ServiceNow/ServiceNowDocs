---
title: Service Manager dashboard
description: Use the Service Manager dashboard to track and analyze customer service case data.
locale: en-US
release: xanadu
product: Analytics and Reporting Solutions for Customer Service
classification: analytics-and-reporting-solutions-for-customer-service
topic_type: concept
last_updated: "2025-08-19"
reading_time_minutes: 1
breadcrumb: [Customer Service Platform Analytics Solutions, Analytics and reporting for Customer Service Management, Customer Service Management]
---

# Service Manager dashboard

Use the Service Manager dashboard to track and analyze customer service case data.

To view the Service Manager dashboard, navigate to **Customer Service** &gt; **Overview**.

**Important:** Navigating to Customer Service Overview to display the Service Manager dashboard may result in an error. Users with the admin role can update the link for the Overview module using the following steps:

1.  Select the Edit Module icon on the Overview module.
2.  Select the Link Type tab on the Overview Module record.
3.  Replace the link in the **Arguments** field with the following text:

    `now/platform-analytics-workspace/dashboards/params/edit/false/tab-sys-id/cfd42b49713354023ee53ca6498cb5d7/sys-id/06e36279f3d8b8349c285a79155206f8`

4.  Select **Update**.

The Service Manager dashboard displays four case-related reports, which are created using the Reports application. You can drill down into these reports for more information about the related cases.

![Service Manager dashboard displaying four case-related reports and their pie chart representations to track and analyze customer service case data. For the text description, refer to the Reports section.](../image/service-manager-homepage.png "Service Manager dashboard")

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|Customer service manager: Track status of cases and customer satisfaction.|sn\_customerservice\_manager|
|Customer service agent: Track status of cases and customer satisfaction.|sn\_customerservice\_agent|
|System administrator: Can edit the dashboard.|admin|

## Reports

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cases by SLA stage

</td><td>

Pie Chart![Pie report icon.](../../../reuse/reporting/image/pie-sm.svg)

</td><td>

Displays the number of cases by SLA stage.

</td></tr><tr><td>

Open Cases By Priority

</td><td>

Donut![Donut report icon.](../../../reuse/reporting/image/semi-donut-sm.svg)

</td><td>

Displays the number of open cases by priority.-   Click a priority to show the case list.
-   Click a case from the list to view details.

</td></tr><tr><td>

Customer Satisfaction

</td><td>

Gauge![Dial report icon.](../../../reuse/reporting/image/solid-gauge-sm.svg)

</td><td>

Displays the results of the customer satisfaction survey that a customer is asked to take after a case is closed.

</td></tr><tr><td>

Open Cases By Product

</td><td>

Semi-Donut![Donut report icon.](../../../reuse/reporting/image/semi-donut-sm.svg)

</td><td>

Displays the number of open cases for each product.

</td></tr></tbody>
</table>