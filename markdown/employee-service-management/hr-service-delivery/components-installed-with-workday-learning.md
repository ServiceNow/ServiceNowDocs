---
title: Components installed with workday learning
description: Several types of components are installed with activation of the HR Service Delivery Integration with Workday Learning \(sn\_lrn\_workday\) application, including tables and user roles.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2024-08-12"
reading_time_minutes: 1
breadcrumb: [Reference HR Service Delivery Integration with Workday Learning, HR Service Delivery Integration with Workday Learning, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Components installed with workday learning

Several types of components are installed with activation of the HR Service Delivery Integration with Workday Learning \(sn\_lrn\_workday\) application, including tables and user roles.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR Workday Learning Admin\[sn\_lrn\_workday.admin\]

</td><td>

-   Can access all features and capabilities of the HR Service Delivery Integration with Workday Learning application.

-   Can configure worker profile settings.

</td><td>

\[sn\_lrn\_workday.admin\]

</td></tr></tbody>
</table>## Scheduled flows installed

<table id="table_stc_gkw_fvb"><thead><tr><th>

Scheduled flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger Workday Learning Integration Flow

</td><td>

Pulls data from Workday Learning to ServiceNow. By default the flow is in inactive state. For information on how to activate the flow, see [Activating schedule flows](../task/activate-w-schedule-flow.md).

</td></tr></tbody>
</table>## Tables installed

<table id="table_sn3_vvg_znb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workday Learning Configurations \[sn\_lrn\_workday\_configurations\]

</td><td>

Stores parameters or inputs which help in setting up the todos configuration.

</td></tr><tr><td>

Workday Learning Todos \[sn\_lrn\_workday\_todos\]

</td><td>

Stores todos that are pulled from Workday Learning.

</td></tr><tr><td>

Worker Profile Sync Configuration \[sn\_lrn\_workday\_worker\_profile\_sync\_configuration\]

</td><td>

Stores one-time configuration parameters for the initial setup of the HR Service Delivery Integration with Workday Learning application.

</td></tr><tr><td>

Workday Learning Skills

</td><td>

Fetches all the active skills from Workday Learning.

</td></tr></tbody>
</table>**Parent Topic:**[Reference HR Service Delivery Integration with Workday Learning](reference-workday-learning-intg.md)

**Related topics**  


[Edit a record in HR Service Delivery Integration with Workday Learning](sync-user-activity-form.md)

[Workday learning todos staging form](wdl-todos-form.md)

[Workday learning user course activity staging form](wdl-user-course-activity-form.md)

