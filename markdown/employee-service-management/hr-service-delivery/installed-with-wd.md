---
title: Components installed with HR Service Delivery Integration with Workday
description: Several types of components are installed with activation of the HR Service Delivery Integration with Workday \(sn\_hr\_workday\) application, including tables and user roles.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference - HR Service Delivery Integration with Workday, HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Components installed with HR Service Delivery Integration with Workday

Several types of components are installed with activation of the HR Service Delivery Integration with Workday \(sn\_hr\_workday\) application, including tables and user roles.

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR Workday Admin\[sn\_hr\_workday.admin\]

</td><td>

-   Can access all features and capabilities of the HR Service Delivery Integration with Workday application.

-   Can configure worker profile settings.

</td><td>

-   flow\_operator
-   import\_admin
-   sn\_hr\_workday.user

</td></tr></tbody>
</table>## Scheduled flows installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run Workday Integration Flow

</td><td>

Pulls data from Workday to ServiceNow. By default the flow is in inactive state. For information on how to activate the flow, see [Activating schedule flows](../task/activate-w-schedule-flow.md).

</td></tr></tbody>
</table>## Tables installed

<table id="table_sn3_vvg_znb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workday Worker Profile Sync Configuration\[sn\_hr\_workday\_configuration\_worker\_profile\_sync\]

</td><td>

Stores one-time configuration parameters for the initial setup of the HR Service Delivery Integration with Workday application. These parameters ensure that worker profile information is pulled from Workday into the ServiceNow application.

</td></tr><tr><td>

Workday Integration Job Tracker\[sn\_hr\_workday\_job\_tracker\]

</td><td>

Tracks every job pull that has been performed from the ServiceNow application to Workday either by schedule job or manual reconciliation process.

</td></tr><tr><td>

Workday Integration Service Job Tracker\[sn\_hr\_workday\_service\_job\_tracker\]

</td><td>

Tracks every service job pull that has been performed from the ServiceNow application to Workday either by schedule job or manual reconciliation process.

</td></tr><tr><td>

Workday Todos\[sn\_hr\_workday\_todo\]

</td><td>

Stores todos that are pulled from Workday.

</td></tr><tr><td>

Workday Configuration Pull To-Dos\[sn\_hr\_workday\_pull\_todo\_config\]

</td><td>

Stores parameters or inputs which help in setting up the todos configuration.

</td></tr></tbody>
</table>**Parent Topic:**[Reference - HR Service Delivery Integration with Workday](hrsd-int-workday-reference.md)

**Related topics**  


[Worker profile synchronization limitations](limit-w-sync.md)

