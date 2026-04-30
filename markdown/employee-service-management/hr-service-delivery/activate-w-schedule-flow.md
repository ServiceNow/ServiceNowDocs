---
title: Activating schedule flows
description: Activate the schedule flow that interacts with Workday to pull worker profile information and tasks into a ServiceNow application.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery Integration with Workday, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Activating schedule flows

Activate the schedule flow that interacts with Workday to pull worker profile information and tasks into a ServiceNow application.

## Before you begin

Role required: sn\_hr\_workday.admin

## Procedure

1.  Navigate to **Flow Designer** &gt; **Designer**.

2.  Open **Run Workday Integration Flow**.

3.  In the Trigger section, specify the time and interval at which you want to automatically run the scheduled flow.

4.  In Actions section, expand **Call Run Workday Service Subflow**.

5.  Select the data that you want to pull.

    You have the following options:

    -   **Department**
    -   **Location**
    -   **Job Profile**
    -   **Worker Profile**
    -   **Effective Worker Profile**
    -   **Future Worker Profile**
    -   **Retrieve All Data**
    -   **Pull To-dos**
    -   **Professional worker profile**
    **Note:**

    -   For a partial pull, deselect the **Retrieve all data** check box. Only modified data \(based on the last successful schedule run time\) is pulled from Workday into the ServiceNow instance. Partial pull is not supported for Department and Location. It is only supported for HR profile and Job Profile.
    -   For a full pull, select the **Retrieve all data** check box. All the data is pulled from Workday into the ServiceNow instance.
    -   The **Retrieve All Data** check box is not supported for **Pull To-Dos**. The first pull will always be a full pull based on the configuration parameter **Initial Load Date time**. The subsequent ones are incremental pulls.
    -   Before you run the flow, turn off reporting: **com.snc.process\_flow.reporting.level**.
6.  Select **Done**.

7.  Select **Activate**.


## Result

The flow is activated after all the trigger conditions are met. The schedule flow pulls data in the following order:

-   Locations
-   Departments
-   Job profile
-   Workers
-   Future workers
-   Effective workers
-   Jobs

Once data is pulled into staging tables, transform maps move data into target tables. For more details, refer to [Use transform maps](../reference/transform-maps-w.md).

