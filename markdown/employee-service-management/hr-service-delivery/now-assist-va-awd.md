---
title: Now Assist Virtual Agent topics for HR Service Delivery Advanced Integration with Workday
description: You can use the Now Assist Virtual Agent topics in Employee Center to place requests, for example, apply for a time off or update your details from the Workday system in Employee Center.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, HR Service Delivery Advanced Integration with Workday, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Now Assist Virtual Agent topics for HR Service Delivery Advanced Integration with Workday

You can use the Now Assist Virtual Agent topics in Employee Center to place requests, for example, apply for a time off or update your details from the Workday system in Employee Center.

## Virtual Agent topics for HR Service Delivery Advanced Integration with Workday Overview

To access and use the Virtual Agent topics, verify the following:

-   [Configure Virtual Agent topics for HR Service Delivery Advanced Integration with Workday](../task/config-awd-va.md).
-   Have one of the following roles: admin, sn\_hr\_sp.hrsp\_alumni, sn\_hr\_sp.hrsp\_contingent, sn\_hr\_sp.hrsp\_employee, sn\_hr\_sp.hrsp\_contractor, or sn\_hr\_sp.admin

## Available Spoke Subflows for Virtual Agent topics for HR Service Delivery Advanced Integration with Workday

<table id="table_wkg_4nx_r2c"><thead><tr><th>

Virtual Agent Topic

</th><th>

Feature Name

</th><th>

Service Name

</th><th>

Subflow

</th></tr></thead><tbody><tr><td>

Lookup Worker Profile

</td><td>

Worker Management

</td><td>

Get Worker

</td><td>

Workday HR - Lookup Worker Profile

</td></tr><tr><td rowspan="2">

Request Time Off

</td><td rowspan="4">

Leave Management

</td><td>

Time off balance

</td><td>

Workday HR - Get Time off balance

</td></tr><tr><td>

Create Time Off Request

</td><td>

Workday HR - Request Time Off

</td></tr><tr><td>

Get Time Off Balance

</td><td>

Time Off Balance

</td><td>

Workday HR - Get Time Off Balance

</td></tr><tr><td>

Get Holiday Calendar

</td><td>

Holiday Calendar

</td><td>

Workday HR - Get Employee Holiday Calendar

</td></tr><tr><td>

Get Total Rewards

</td><td>

Benefits Management

</td><td>

Total Rewards

</td><td>

Workday HR - Get Total Rewards

</td></tr><tr><td>

Get User Pay Checks

</td><td>

Payroll Management

</td><td>

Get Paychecks

</td><td>

Workday HR - Get Employee Paychecks

</td></tr><tr><td rowspan="2">

-   Update Email Address
-   Update Address
-   Update Phone Number
-   Update Date of Birth
-   Update Blood Type

</td><td>

Human Capital Management

</td><td>

Update Personal Details

</td><td>

Workday HR - Update Personal Details

</td></tr><tr><td>

Worker Management

</td><td>

Get Worker

</td><td>

Workday HR - Lookup Worker Profile

</td></tr></tbody>
</table>## Lookup Worker Profile

The Lookup Worker Profile Virtual Agent topic enables you to view the profile of a coworker. From Employee Center, open a chat window and type in key words, for example, worker profile. After you have specified the details of coworkers, worker profile details of one or more users are displayed.

![Lookup Profile 1](../image/awd-lookup-1.png) ![Lookup Profile 2](../image/awd-lookup-2.png)

## Update Personal Details

You can update personal details in Virtual Agent using one of the following topics in Employee Center from the Workday system.

-   Update Address
-   Update Date of Birth
-   Update Email Address
-   Update Phone Number
-   Update Blood Type

## Get User Paychecks

The Get User Paychecks Virtual Agent topic enables you to view your payslip details. From Employee Center, open a chat window and type in key words, for example, get payslips. After you provide the required details such as start date and end date, your payslip summary, in the form of pay period, gross pay, deductions, and net pay are displayed. A detailed breakdown of deductions is also displayed.

![User Paychecks](../image/awd-paycheck.png)

## Get Total Rewards

The Get Total Rewards Virtual Agent topic enables you to view your rewards. From Employee Center, open a chat window and type in key words, for example, rewards.

![Total Rewards](../image/awd-total-rewards.png)

## Get Time Off Balance

The Get Time Off Balance Virtual Agent topic enables you to view your leave balance. From Employee Center, open a chat window and type in key words, for example, leave balance.

![TimeOff Balance](../image/awd-timeoff-balance.png)

## Request Time Off

The Request Timeoff Virtual Agent topic enables you to apply for leaves. From Employee Center, open a chat window and type in key words, for example, request time off. After you have specified required details such as start date and end date, the time off request is sent to the Workday system.

![TimeOff 1](../image/awd-request-timeoff1.png) ![TimeOff 2](../image/awd-request-timeoff2.png)

## Get Holiday Calendar

The Get Holiday Calendar Virtual Agent topic enables you to view your holiday calendar. From Employee Center, open a chat window and type in key words, for example, holiday calendar. After specifying the calendar year, the holiday calendar appears in the chat.

![Holiday Calendar 1](../image/awd-calendar1.png) ![Holiday Calendar 2](../image/awd-calendar2.png)

**Parent Topic:**[Using HR Service Delivery Advanced Integration with Workday](using-hr-service-delivery-advanced-integration-with-workday.md)

**Related topics**  


[Time off request to Workday](w-timeoff.md)

[Change legal name through Virtual Agent](../task/change-legal-na-awd.md)

[Publish the VA topic template for legal name change](../task/nlu-awd.md)

[Report an issue with your payslip](../task/payslips-awd.md)

[Use HCM AI agents for HR Service Delivery Advanced Integration with Workday](conversational-agents-wd.md)

