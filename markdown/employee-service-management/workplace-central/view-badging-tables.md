---
title: View Occupancy Dashboard
description: Workplace administrators and managers can view the workspace occupancy metrics to plan and optimize the workplace space utilization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/view-badging-tables.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Workplace Analytics, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# View Occupancy Dashboard

Workplace administrators and managers can view the workspace occupancy metrics to plan and optimize the workplace space utilization.

## Before you begin

To view the Occupancy Dashboard report, ensure you have:

-   Installed Workplace Central \(sn\_wsd\_central\) application plugin.
-   Workplace users must have an employee profile created.
-   Workplace users must have a workplace location assigned in the employee profile.

Workplace users with the following roles can access the Occupancy Dashboard report:

-   sn\_wsd\_central.workplace\_analytics\_user
-   sn\_wsd\_wc.manager
-   sn\_wsd\_wc.user

Role required: sn\_wsd\_wc.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

    The Workplace Analytics dashboard is displayed.

2.  Select **Occupancy Dashboard**.

3.  Filter by **Date**, **Region**, **Cost center**, **Department**, or **Workplace entity**.

    \[Omitted image "wsd-occupancy-dashboard-headcount-trends.png"\] Alt text: Occupancy dashboard showing filter options.

4.  Select **Apply** after you’ve selected the required filters.

5.  View the **Total headcount**, **Highest onsite headcount in a day**, and **Average daily onsite headcount** for a selected region, date, and cost center or department.

6.  View occupancy reports based on the following criteria:

    -   Headcount Trends
    -   Available onsite headcount
    -   Total headcount vs online headcount by department
    -   Total headcount vs onsite headcount by workplace entity

        Filter by workplace entity to view space allocations of a building based on workplace entities. Workplace entity-based allocation, enables you to control the space consumption of each business in your organization. For more information, see [Map designated workspaces to user profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/map-employees-to-existing-workplace-locations-wsd.md) and [Attendance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/attendance-analytics.md).

    \[Omitted image "wsd-workplace-entity-total-headcount.png"\] Alt text: Occupancy dashboard showing headcount trends.

7.  The following default scorecards are available on the dashboard:

    Select a scorecard to see detailed reports and metrics:

    -   Total headcount
    -   Highest onsite headcount in a day
    -   Average daily onsite headcount
8.  Select an object on the chart to open the related component page.

    For example, select **Headcount trends** on the chart to open the Headcount trends page. The headcount for a selected region, site, campus, building, cost center, or department is shown.

9.  Select **Export** to export occupancy dashboard data to Excel, JSON, CSV, or a PDF file.

10. After exporting the data, download or email the data.


**Parent Topic:**[Working with Workplace Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/working-with-workplace-analytics.md)

**Related topics**  


[View Space Optimization metrics]()

[View Lease Administration metrics]()

[View Maintenance Management metrics]()

[Manage Workplace Dashboards]()

