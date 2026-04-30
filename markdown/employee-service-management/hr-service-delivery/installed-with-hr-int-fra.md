---
title: Components installed with Enterprise Service Management Integrations Framework
description: Several types of components are installed with activation of the Enterprise Service Management Integrations Framework \[sn\_hr\_integre\_fw\], including tables and user roles.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enterprise Service Management Integrations Framework reference, Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Components installed with Enterprise Service Management Integrations Framework

Several types of components are installed with activation of the Enterprise Service Management Integrations Framework \[sn\_hr\_integre\_fw\], including tables and user roles.

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Framework Integrations Admin\[sn\_hr\_integr\_fw.admin\]

</td><td>

Can access and set up Enterprise Service Management Integrations Framework.

</td><td>

Flow Operator\[flow\_operator\]

</td></tr></tbody>
</table>## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Source\[sn\_hr\_integr\_fw\_source\]

</td><td>

Stores source records representing third-party systems which are integrating with your ServiceNow application.

</td></tr><tr><td>

Integration Service\[sn\_hr\_integr\_fw\_service\]

</td><td>

Stores records of integration services. An integration service is created for each entity that is pulled from a third-party system.

</td></tr><tr><td>

Integration Job Tracker\[sn\_hr\_integr\_fw\_job\_tracker\]

</td><td>

Stores source job details, such as start time, run end time, and state. For more information, see [View job tracker details](../task/hr-integration-job-tracker.md).

</td></tr><tr><td>

Integration Service Job Tracker\[sn\_hr\_integr\_fw\_service\_job\_tracker\]

</td><td>

Stores service job details such as start time, end time, and state. For more information, see [View job tracker details](../task/hr-integration-job-tracker.md).

</td></tr><tr><td>

Pulled Integration To-do\[sn\_hr\_integr\_fw\_todo\_inbound\]

</td><td>

Stores tasks that are pulled from the third-party system into Enterprise Service Management Integrations Framework. For more information, see [View tasks of a third-party system](../task/display-todos.md).

</td></tr><tr><td>

External Interface\[sn\_hr\_integr\_fw\_ext\_interface\]

</td><td>

Stores modified records that are pushed from a ServiceNow application into a third-party system.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Service Management Integrations Framework reference](../task/ent-service-mgmt-int-framework-reference.md)

