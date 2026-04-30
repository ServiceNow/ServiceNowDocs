---
title: View Maintenance Management metrics
description: Use the Maintenance Management dashboard to get an insight into maintenance cases, their trends, and maintenance plan compliance. These insights enable you to create an efficient maintenance plan to improve workflows and reduce maintenance activities and their related costs.
locale: en-US
release: yokohama
product: Workplace Central
classification: workplace-central
topic_type: concept
last_updated: "2025-09-07"
reading_time_minutes: 6
breadcrumb: [Working with Workplace Analytics, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# View Maintenance Management metrics

Use the Maintenance Management dashboard to get an insight into maintenance cases, their trends, and maintenance plan compliance. These insights enable you to create an efficient maintenance plan to improve workflows and reduce maintenance activities and their related costs.

## Prerequisites for accessing the View Maintenance Management dashboard

-   Ensure that the Workplace Central application is installed. For more information, see [Install Workplace Central](install-workplace-central.md)
-   Ensure that the Workplace Maintenance Management \(sn\_wsd\_maintenance\) application is installed. For more information, see [Install Workplace Maintenance Management](../../workplace-maintenance-management/task/intall-workplace-maintenance-mgmt.md).
-   Create and publish a maintenance plan. For more information, see [Create and publish maintenance plans](../../workplace-maintenance-management/task/create-publish-maintenance-plans.md) and [Workplace maintenance cases](../../workplace-maintenance-management/task/create-maint-cases.md).

    You can also create a maintenance plan record by using the Preventative Maintenance option on the Workplace central home page. Navigate to **All** &gt; **Workplace Central**. Select the Preventative Maintenance icon \(![Preventative Maintenance icon on the context side bar to create a maintenance plan.](../images/icon-preventative-maintenance.png)\) on the context side bar to create a maintenance plan.

-   Ensure that the plugin Performance Analytics \(com.snc.pa\) is installed and that you have the Performance Analytics premium entitlement. For more information, see [Install Performance Analytics Content Pack for Agile 2.0](https://www.servicenow.com/docs/access?context=install-configure-agile-dashboard&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   Ensure that the Workplace Central, Workplace Maintenance Management applications and all of their associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Run the **Workplace Maintenance Case Historical Data Collection** job before viewing the dashboard for the first time. For more information, see [Run the scheduled job for the Maintenance Management dashboard](run-job-for-wmm-dashboard.md).

## Accessing the dashboard

To access the Maintenance Management dashboard, you must have the sn\_wsd\_maintenance.manager or sn\_wsd\_maint.admin role.

-   Access the dashboard using one of the following navigation paths:
    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **Workspaces** &gt; **Workplace Central**
-   Select the **Maintenance Management** tab.

![Workplace Analytics Maintenance Management dashboard](../images/wpa-maintenance-dashboard.png)

## Scorecards

The following default scorecards are available on the dashboard. To see the list of records, select the related card.

-   **PMP \(Planned Maintenance Percentage\)**

    Shows the percentage of planned days spent for preventive cases vs the total planned days for both preventive and corrective maintenance cases. A high percentage value indicates that more time is being spent in planned maintenance activities rather than unplanned activities.

    Calculation:

    `Planned Maintenance Percentage = (Total number of days taken to complete all preventive maintenance cases for a duration / Total number of days taken to complete all maintenance cases for the duration) X 100`


-   **PMC \(Planned Maintenance Compliance\)**

    Shows the percentage of the total number of preventive maintenance cases completed vs the total number of preventive maintenance cases. A high percentage value indicates that maintenance activities are completed as per schedule.

    Calculation:

    `Planned Maintenance Compliance = (Number of preventive maintenance cases completed/ Total preventive maintenance cases) X 100`


-   **MTR \(Mean time to repair\)**

    Shows the average time taken to close a maintenance case. A low value indicates that the processes for maintenance and the necessary skills to handle them are effective.

    Calculation:

    `Mean time to repair = Average age of all the maintenance cases / Total number of maintenance cases`


-   **Number of open cases**

    Shows the total number of open cases. A low number of open cases indicates your maintenance plan and resolution processes are effective.

    Calculation:

    `Total number of preventive and corrective maintenance cases that are not in closed complete, closed incomplete, or canceled state.`


## Reports

The following default reports are available on the dashboard. Select the card to see the list of records.

-   **Corrective vs preventive maintenance case trend**

    Displays the trend of corrective and preventive maintenance cases.

    Benefits:

    Analyze the trend to understand the efficiency of planning and identify any assets that must be retired or replaced.


-   **Average age of maintenance cases**

    Displays the average age of corrective and preventive maintenance cases.

    Benefits:

    Analyze the trend to understand the efficiency of maintenance services and identify the process or assets that cause the increase in the age of maintenance cases. Take steps to reduce the age of cases.

    Formula:

    -   `Average age of corrective maintenance cases = [Sum of ages for all the corrective cases/Total number or maintenance cases]`
    -   `Average age of preventive maintenance cases = [Sum of ages for all the preventive cases/Total number or maintenance cases]`

-   **Planned maintenance percentage trend**

    Displays the percentage trend for the total number of days spent on preventive cases versus the total number of planned days for both preventive and corrective maintenance cases.

    Benefits:

    Analyze the trend to identify problem areas that cause unplanned activities or corrective cases. Modify the process or replace or retire the assets to avoid unplanned activities.

    Formula:

    `Planned maintenance percentage trend = (Total number of planned maintenance days / Total number of maintenance days) X 100`


-   **Planned Maintenance Compliance trend**

    Displays the percentage trend of the total number of preventive maintenance cases completed versus the total number of preventive maintenance cases.

    Benefits:

    Analyze the Planned Maintenance Compliance trend to identify issues that lead to deviation from the plan. Take steps to improve processes that causes inconsistent on-time completion.

    Calculation:

    `Planned Maintenance Compliance trend = [Number of completed preventive maintenance cases/ Total preventive maintenance cases] X 100`


## Indicators

The indicator groups and indicators listed in the following table are used for populating the widgets in the dashboard.

<table id="table_krh_zb2_5wb"><thead><tr><th>

Indicator group name

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Workplace.Maintenance.Case.Closed

</td><td>

-   Workplace Maintenance Case Closed Age Sum Hours
-   Workplace Maintenance Case Closed Corrective Age Sum Hours
-   Workplace Maintenance Case Closed Corrective Count
-   Workplace Maintenance Case Closed Preventive Age Sum Hours
-   Workplace Maintenance Case Closed Preventive Count

</td></tr><tr><td>

Workplace.Maintenance.Case.Opened

</td><td>

-   Number of corrective cases
-   Number of open cases
-   Number of preventive cases
-   Workplace Maintenance Case Opened Preventive Closed Complete Count

</td></tr></tbody>
</table>You can also add new indicators. For more information on how to work with indicators, see [Configure Performance Analytics fundamentals](https://www.servicenow.com/docs/access?context=c_PAWidgetsAndDashboards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

-   **[Run the scheduled job for the Maintenance Management dashboard](run-job-for-wmm-dashboard.md)**  
As an admin, run the scheduled job **Workplace Maintenance Case Historical Data Collection** to collect data for the past year that is used by the Maintenance Management dashboard.

**Parent Topic:**[Working with Workplace Analytics](../concept/working-with-workplace-analytics.md)

**Related topics**  


[View Space Optimization metrics](view-space-opt-analytics.md)

[View Occupancy Dashboard](../../workplace-connectors/task/view-badging-tables.md)

[View Lease Administration metrics](view-lease-admin-analytics.md)

[Manage Workplace Dashboards](workplace-dashboards-wsd-central.md)

