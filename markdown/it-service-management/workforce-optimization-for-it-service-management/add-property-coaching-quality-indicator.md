---
title: Configure an indicator to display in the Coaching Overview tab in Workforce Optimization for ITSM
description: Add a system property to display the desired indicator in the Coaching Overview tab in the Coaching application.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Coaching in Workforce Optimization for ITSM, Coaching in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Configure an indicator to display in the Coaching Overview tab in Workforce Optimization for ITSM

Add a system property to display the desired indicator in the Coaching Overview tab in the Coaching application.

## Before you begin

Set the map application scope to **Coaching**. For information on how to set the scope, see [Set map application scope](https://www.servicenow.com/docs/access?context=set-map-application-scope&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Role required: admin

## About this task

Replace the existing indicator with any Performance Analytics indicator that has the Assigned to and Assignment group breakdowns to display in the Coaching Overview tab in the Coaching application.

## Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  Click **New**.

3.  Enter the following field values.

<table id="table_yfh_h3p_f4b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Suffix

</td><td>

sn\_coaching.coaching\_overview\_default\_quality\_indicator

</td></tr><tr><td>

Application scope

</td><td>

Coaching

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Value

</td><td>

\{"title": "&lt;name&gt;", "sys\_id": "&lt;sys id&gt;"\}where &lt;name&gt; is the name of the indicator that you want to display in the Coaching Overview tab and &lt;sys id&gt; is the [unique record identifier](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) \(sys\_id\) of the indicator.

 Example:

-   Name: % of P1 incidents resolved on first call.
-   Sys ID: 0423e59387401010ca99e12397cb0bbb
\{"title": "% of P1 incidents resolved on first call", "sys\_id": "0423e59387401010ca99e12397cb0bbb"\}

</td></tr><tr><td>

Read roles

</td><td>

sn\_coaching.coach

</td></tr></tbody>
</table>4.  Click **Submit**.

    The configured indicator replaces the existing indicator in the Overview tab in the Coaching application in Workforce Optimization for ITSM.

    The image below show an example of the configured indicator displayed in the Coaching Overview tab.![Coaching quality indicator](../image/coaching-quality-indicator-uib.png)


**Parent Topic:**[Setting up Coaching in Workforce Optimization for ITSM](../concept/setup-coaching-configurable-workforce-optimization-itsm.md)

