---
title: Configure an indicator to display in the Coaching Overview tab in Workforce Optimization for Customer Service
description: Add a system property to display the desired indicator in the Coaching Overview tab in the Coaching application.
locale: en-US
release: yokohama
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Coaching in Workforce Optimization for Customer Service, Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Configure an indicator to display in the Coaching Overview tab in Workforce Optimization for Customer Service

Add a system property to display the desired indicator in the Coaching Overview tab in the Coaching application.

## Before you begin

**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](request-configurable-wfo-cs.md).

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

    The configured indicator replaces the existing indicator in the Overview tab in the Coaching application in Workforce Optimization for Customer Service.


**Parent Topic:**[Setting up Coaching in Workforce Optimization for Customer Service](../concept/setup-coaching-configurable-wfo-cs.md)

