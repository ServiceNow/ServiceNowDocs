---
title: Configure an indicator to display in the Coaching Overview tab in Workforce Optimization for Field Service
description: Display any Performance Analytics indicator that has the Assigned to and Assignment group breakdowns to display in the Coaching Overview tab in the Coaching application. The indicators can display the average quality of work in the past 30 days or more.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up coaching in Workforce Optimization for Field Service, Configuring Workforce Optimization for Field Service, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Configure an indicator to display in the Coaching Overview tab in Workforce Optimization for Field Service

Display any Performance Analytics indicator that has the Assigned to and Assignment group breakdowns to display in the **Coaching Overview** tab in the Coaching application. The indicators can display the average quality of work in the past 30 days or more.

## Before you begin

Set the map application scope to **Coaching**. For more information, see [Set map application scope](https://www.servicenow.com/docs/access?context=set-map-application-scope&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Role required: admin

## Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  Click **New**.

3.  Enter the field values in the following table.

<table id="table_yfh_h3p_f4b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

sn\_coaching.coaching\_overview\_default\_quality\_indicator

</td></tr><tr><td>

Application

</td><td>

Coaching

</td></tr><tr><td>

Type

</td><td>

string

</td></tr><tr><td>

Value

</td><td>

\{"title": "&lt;name&gt;", "sys\_id": "&lt;sys id&gt;"\}where &lt;name&gt; is the name of the indicator that you want to display in the Coaching Overview tab and &lt;sys id&gt; is the unique record identifier \(sys\_id\) of the indicator. For more information, see [Unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

 For example:

-   Name: % of P1 incidents resolved on first call.
-   Sys ID: 0423e59387401010ca99e12397cb0bbb
\{"title": "% of P1 incidents resolved on first call", "sys\_id": "0423e59387401010ca99e12397cb0bbb"\}

</td></tr><tr><td>

Read roles

</td><td>

sn\_coaching.coach

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The configured indicator replaces the existing indicator in the **Overview** tab in the Coaching application in Workforce Optimization for Field Service.

