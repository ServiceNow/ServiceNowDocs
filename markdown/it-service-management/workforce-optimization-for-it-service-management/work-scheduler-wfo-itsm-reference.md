---
title: Work Scheduler components in Workforce Optimization for ITSM reference
description: Workforce Optimization for ITSM has properties to configure the Work scheduler default behavior.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work scheduler in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Work Scheduler components in Workforce Optimization for ITSM reference

Workforce Optimization for ITSM has properties to configure the Work scheduler default behavior.

## Properties

Enter **sys\_properties.list** in the Workspace filter navigator and search for the work scheduler properties listed below.

<table id="table_w1x_5k2_jtb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wfo\_work\_sched.allowed\_tables

</td><td>

Defines the list of tables that a Work scheduler admin \(sn\_wfo\_work\_sched.admin\) can use to create configurations for work assignments in the Workforce Optimization for ITSM manager workspace.-   **Type:** string
-   **Default value:** incident,problem,change\_request,change\_task,sc\_task,sc\_request,sc\_req\_item,interaction

</td></tr><tr><td>

sn\_wfo\_work\_sched.shift\_data\_categories

</td><td>

Comma separated sys ids for event categories that display in the Work scheduler calendar in the manager workspace.

 **Type:** string

</td></tr><tr><td>

sn\_wfo\_work\_sched.should\_fetch\_shift\_data

</td><td>

Enables the display of shift spans in Work scheduler in Workforce Optimization for ITSM manager workspace.-   **Type:** true\|false
-   **Default value:** true

</td></tr><tr><td>

sn\_wfo\_work\_sched.recommend\_criteria\_limit​

</td><td>

Defines how many matching criteria can be created for each matching rule in Work scheduler when suggestions are enabled.​-   **Type:**integer
-   **Default value:**10

</td></tr><tr><td>

sn\_wfo\_work\_sched.match\_criteria\_threshold​

</td><td>

Defines which users are shown in Work scheduler when suggestions are enabled and the matching criteria percentage is greater than the value indicated.​-   **Type:** integer
-   **Default value:** 0

</td></tr></tbody>
</table>