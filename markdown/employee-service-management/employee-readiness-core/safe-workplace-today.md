---
title: My Safe Workplace
description: Use the ServiceNow My Safe Workplace page to view all of your information and resources for returning to the workplace. Manage your requirement status for workplace entry, update your health status, track workspace reservations, and create requests for PPE or testing.Add or remove widgets that employees can view on My Safe Workplace.
locale: en-US
release: zurich
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# My Safe Workplace

Use the ServiceNow® My Safe Workplace page to view all of your information and resources for returning to the workplace. Manage your requirement status for workplace entry, update your health status, track workspace reservations, and create requests for PPE or testing.

To view My Safe Workplace, navigate to **Employee Health and Safety Status** &gt; **My Safe Workplace**.



<table id="table_vyf_1dp_pnb"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manage your overall status

</td><td>

View whether you're cleared to enter the workplace based on your completion of entry requirementsfor your current location.

</td></tr><tr><td>

Submit an update about your health status

</td><td>

View and update your current health status. Managers can also view and update the health status for their direct reports. For managers, this widget is called **Submit an update about a person's health status**.

</td></tr><tr><td>

Track your reservations

</td><td>

The **Upcoming reservation** tab shows your next workspace reservation. The **All reservations** tab shows your next five reservations. Click **Reserve a space** to create a new reservation to reserve a space for a day.

</td></tr><tr><td>

Things you can request

</td><td>

You can take the following actions.-   Submit a list of daily contacts for contact tracing
-   Submit a user privacy consent form for contact tracing
-   Submit a health verification about your health status and compliance with safety policies
-   Screen a visitor for entry
-   Invite a visitor
-   Request permission to travel
-   Request a COVID-19 diagnostic test or report your test results
-   Request personal protective equipment \(PPE\) such as masks, gloves, or goggles
-   Reserve shifts and workspaces
-   Schedule your arrival time at a workplace

If some ServiceNow® Safe Workplace suite applications are not installed, some requests may not be available.

</td></tr><tr><td>

Tasks

</td><td>

Track the status of your travel, health testing, workspace reservation,and PPE requests.

</td></tr><tr><td>

View your team's status

</td><td>

View whether your direct reports are cleared to enter the workplace. This widget is only displayed for managersand reflects a user's status for their current location.

</td></tr><tr><td>

Key resources

</td><td>

View featured knowledge articles.

</td></tr></tbody>
</table>**Parent Topic:**[Employee Readiness Core](employee-readiness-core.md)

## Set up My Safe Workplace

Add or remove widgets that employees can view on My Safe Workplace.

### Before you begin

Role required: admin

### About this task

My Safe Workplace uses widgets from ServiceNow® Safe Workplace suite applications.

-   The **Submit an update about your health status** widget requires the ServiceNow® Emergency Self Report application.
-   The **Track your reservations** widget requires the ServiceNow® Workplace Core application.

If these applications are not installed, by default there are blank spaces in My Safe Workplace where the corresponding widgets would be displayed. Complete the setup steps to remove any blank spaces.

My Safe Workplace also has widgets for employees to create and track requests. The requests use features from the following Safe Workplace suite applications.

-   ServiceNow® Contact Tracing
-   ServiceNow® Employee Health Screening
-   ServiceNow® Employee Readiness Core
-   ServiceNow® Employee Travel Safety
-   ServiceNow® Health and Safety Testing
-   ServiceNow® Workplace PPE Inventory Management
-   ServiceNow® Workplace Core

If some of these applications are not installed, employees can still use the widgets to create and view requests based on the applications that are installed. Install the remaining applications to give employees access to all request types.

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Click **Designer**.

3.  Search for **Safe Workplace Today**.

4.  Adjust the page layout to remove any blank spaces.

    You can also remove any widgets that you don't want to use, or add new widgets. For detailed instructions, see [Create and edit a page using the Service Portal Designer](https://www.servicenow.com/docs/access?context=t_ConfigureAPage&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).


### What to do next

To complete the setup, make sure that employees have the required roles to view the widgets.

-   The **Submit an update about your health status** widget requires the sn\_imt\_quarantine.crisis\_task\_user role.
-   The **Track your reservations** widget requires the sn\_wsd\_core.workplace\_user role.
-   The **View your team's status** widget is only displayed for managers. The sn\_imt\_monitoring.monitoring\_user role is required for managers to view details about their direct reports.
-   There are no required roles for all other My Safe Workplace widgets.

