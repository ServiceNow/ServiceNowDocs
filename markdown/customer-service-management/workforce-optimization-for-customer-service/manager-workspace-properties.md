---
title: Manager Workspace properties
description: Modify the Manager Workspace configuration by customizing the system properties to set the Alerts card limit and the widget refresh interval.
locale: en-US
release: yokohama
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Manager Workspace properties

Modify the Manager Workspace configuration by customizing the system properties to set the Alerts card limit and the widget refresh interval.

Navigate to **All****&gt;System Properties****&gt;All Properties**.

Alternatively, in your instance, enter `sys_properties.list` in the filter navigator and view the system properties.

<table id="table_qbv_3d4_pwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_csm\_wfo\_workspa.alerts\_cards\_limit**

</td><td>

Enable or disable interaction creation for a non-matched user.-   Type: Integer
-   Value: 15
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

**sn\_csm\_wfo\_workspa.widget\_refresh\_interval\_long**

</td><td>

Set the inactivity period \(in days\) after which an interaction is closed if no email is received from the customer.-   Type: Integer
-   Value: 120
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

**sn\_csm\_wfo\_workspa.widget\_refresh\_interval\_short**

</td><td>

Set the inactivity period \(in days\) after which an interaction is closed if no email is received from the customer.-   Type: Integer
-   Value: 30
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Workforce Optimization for Customer Service](../concept/setup-configurable-wfo-cs.md)

