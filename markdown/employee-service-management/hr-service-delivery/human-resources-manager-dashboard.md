---
title: Human Resources manager dashboard
description: The dashboard for HR Managers provides insights on how HR teams are meeting expectations. The HR Manager can measure and improve the influence of their team on meeting and exceeding workforce expectations.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-13"
reading_time_minutes: 3
breadcrumb: [HR Performance Analytics Dashboards, Performance Analytics for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Human Resources manager dashboard

The dashboard for HR Managers provides insights on how HR teams are meeting expectations. The HR Manager can measure and improve the influence of their team on meeting and exceeding workforce expectations.

**Note:** This dashboard is available in the Human Resources Scoped App content pack.

![The Overview tab of the HR Manager dashboard that is included in the Performance Analytics Human Resources Scoped App out of the box solution](../../../product/human-resources-global/image/hr-manager-dshbrd-overview.png "Overview tab") ![Bottom of the Overview tab](../../../product/human-resources-global/image/hr-manager-dshbrd-overview-btm.png "Overview tab")

![The Operational tabl of the HR Manager dashboard](../../../product/human-resources-global/image/hr-manager-operational-tab.png "Operational tab")

![The Backlog Monitor tab of the HR Manager dashboard](../../../product/human-resources-global/image/hr-manager-backlog-tab.png "Backlog monitor tab")

## End users and roles

<table id="table_alx_w2h_vdb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

HR Manager: Needs clear visibility into the operations of the shared service center.

</td><td>

sn\_hr\_core.manager

</td></tr></tbody>
</table>## Use case

Organizations need to understand and meet or exceed the expectations of the modern workforce and provide a delightful employee experience. This dashboard provides the HR manager with an overview of the number of HR cases and the time and difficulty in resolving them.

## Indicators

The HR Manager dashboard presents the following key performance indicators:

-   **Average case survey score**

    Measures the average score of the customer satisfaction survey that is sent to the employees after a case is closed. The score should maximize over time.

    The **CSAT** widget on the dashboard presents an average over the last seven days of the average case survey score.

-   **HR Cases Growth**

    Measures the change in volume of your case backlog. This value is calculated from other indicators using the formula `Number of open cases - Number of closed HR cases`.

-   **Number of open cases with breached SLAs**

    Measures the number of open cases that have SLAs greater than 100.

-   **Average age of open cases**

    Measures the average time that a case remains open. This value is calculated from other indicators using the formula `Summed duration of open cases / Number of open cases / 24`.

    On the dashboard, this indicator is labeled **Open Cases Age**.

-   **Average age of closed cases**

    Measures the average amount of time that it takes to close a case. This value is calculated from other indicators using the formula `Summed duration of open cases / Number of open cases / 24`.

    The **Average time to close - Weekly** widget presents an average over the last seven days of the average age of closed cases.

-   **Number of open cases**

    Measures the number of cases that were opened on or before today that have not been closed yet.

    The number of open cases is plotted against the age of open cases.

-   **Average reassignment of open cases**

    Measures the average number of times a case is reassigned. This value is calculated from other indicators using the formula `Summed reassignment of open cases / Number of open cases`.

-   **Number of cases with no updates in last 3 daysNumber of cases with no updates in last 10 days**

    The number of open cases that have gone 3 or 10 days, respectively, without any updates.

-   **Summed duration of open cases**

    Measures how long all open cases have been open for.

-   **Number of reassigned open cases**

    Measures the number of cases that have a reassignment count greater than 0.

-   **Summed reassignment of open cases**

    Measures how many times a case is reassigned.

-   **Number of unassigned open cases**

    Measures number of open cases that are yet to be assigned.

-   **Number of closed HR cases**

    Measures the number of cases that were closed today.

-   **Summed duration of closed cases**

    Measures the time taken to close all cases.

-   **Number of new cases**

    Measures the number of cases that were opened today.


## Breakdowns

-   Age
-   Agent
-   Assignment Group
-   COE
-   HR Service
-   Priority
-   Source
-   State
-   Topic Category

## Data visualizations

The Human Resources Manager dashboard contains the following visualizations:

|Title|Type|
|-----|----|
|\# Breached SLA|Single Score|
|\# Critical Cases|Single Score|
|\# Not updated last 10 days|Single Score|
|\# Unassigned Open Cases|Single Score|
|Approvals Requested|Single Score|
|Open Backlog|Single Score|
|Open Backlog by State|List|
|Open Backlog by State|Horizontal bar|
|Open Cases Distribution|Heatmap|
|Time Spent in Each Group\(last 6 months\)|Multilevel Pivot|
|Unassigned Cases|Single Score|

**Parent Topic:**[HR Performance Analytics Dashboards](human-resources-content-pack.md)

