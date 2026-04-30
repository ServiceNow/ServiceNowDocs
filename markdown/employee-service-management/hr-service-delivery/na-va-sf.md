---
title: Now Assist Virtual Agent topics for HR Service Delivery Integration with SuccessFactors
description: You can use the Now Assist Virtual Agent topics in Employee Center to place requests, for example, apply for a time off or update your details from the SuccessFactors system in Employee Center.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-03-05"
reading_time_minutes: 3
breadcrumb: [Using HR Service Delivery Integration with SuccessFactors, HR Service Delivery Integration with SuccessFactors, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Now Assist Virtual Agent topics for HR Service Delivery Integration with SuccessFactors

You can use the Now Assist Virtual Agent topics in Employee Center to place requests, for example, apply for a time off or update your details from the SuccessFactors system in Employee Center.

## Virtual Agent topics for HR Service Delivery Integration with SuccessFactors Overview

To access and use the Virtual Agent topics, verify the following:

-   [Configure the Now Assist for HRSD Virtual Agent topics](../task/config-va-topics.md)
-   Have one of the following roles: sn\_hr\_sp.admin , sn\_hr\_sp.esc\_admin

## Available Spoke Subflows for Virtual Agent topics for HR Service Delivery Integration with SuccessFactors

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

SuccessFactors HR - Lookup Worker Profile

</td></tr><tr><td rowspan="2">

Request Time Off

</td><td rowspan="4">

Leave Management

</td><td>

Time off balance

</td><td>

SuccessFactors HR - Get Time off balance

</td></tr><tr><td>

Create Time Off Request

</td><td>

SuccessFactors HR - Request Time Off

</td></tr><tr><td>

Get Time Off Balance

</td><td>

Time Off Balance

</td><td>

SuccessFactors HR - Get Time Off Balance

</td></tr><tr><td>

Get Holiday Calendar

</td><td>

Holiday Calendar

</td><td>

SuccessFactors HR - Get Employee Holiday Calendar

</td></tr><tr><td>

Get Total Rewards

</td><td>

Benefits Management

</td><td>

Total Rewards

</td><td>

SuccessFactors HR - Get Total Rewards

</td></tr><tr><td>

Get User Pay Checks

</td><td>

Payroll Management

</td><td>

Get Paychecks

</td><td>

SuccessFactors HR - Get Employee Paychecks

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

SuccessFactors HR - Update Personal Details

</td></tr><tr><td>

Worker Management

</td><td>

Get Worker

</td><td>

SuccessFactors HR - Lookup Worker Profile

</td></tr></tbody>
</table>## Lookup Worker Profile

The Lookup Worker Profile Virtual Agent topic enables you to view the profile of a coworker. From Employee Center, open a chat window and type in key words, for example, worker profile. After you have specified the details of coworkers, worker profile details of one or more users are displayed.

![Lookup Worker Profile 1](../image/sf-lookup-profile1.png) ![Lookup Worker Profile 2](../image/sf-lookup-profile2.png)

## Update Personal Details

You can update personal details in Virtual Agent using one of the following topics in Employee Center from the SuccessFactors system.

-   Update Address
-   Update Date of Birth
-   Update Email Address
-   Update Phone Number

## Get User Paychecks

The Get User Paychecks Virtual Agent topic enables you to view your payslip details. From Employee Center, open a chat window and type in key words, for example, get payslips. After you provide the required details such as start date and end date, your payslip summary, in the form of pay period, gross pay, deductions, and net pay are displayed. A detailed breakdown of deductions is also displayed.

![Get User Paychecks](../image/sf-get-paychecks.png)

## Get Total Rewards

The Get Total Rewards Virtual Agent topic enables you to view your rewards. From Employee Center, open a chat window and type in key words, for example, rewards.

![Get Total Rewards](../image/sf-get-total-rewards.png)

## Get Time Off Balance

The Get Time Off Balance Virtual Agent topic enables you to view your leave balance. From Employee Center, open a chat window and type in key words, for example, leave balance.

![Get TimeOff](../image/sf-timeoff.png)

## Request Time Off

The Request Timeoff Virtual Agent topic enables you to apply for leaves. From Employee Center, open a chat window and type in key words, for example, request time off. After you have specified required details such as start date and end date, the time off request is sent to the SuccessFactors system.

![Request Time Off 1](../image/sf-requestoff-1.png) ![Request Time Off 2](../image/sf-requestoff-2.png)

## Get Holiday Calendar

The Get Holiday Calendar Virtual Agent topic enables you to view your holiday calendar. From Employee Center, open a chat window and type in key words, for example, holiday calendar. After specifying the calendar year, the holiday calendar appears in the chat.

![Get Holiday Calendar 1](../image/sf-calendar-1.png) ![Get Holiday Calendar 2](../image/sf-calendar-2.png)

**Parent Topic:**[Using HR Service Delivery Integration with SuccessFactors](using-hr-service-delivery-integration-with-success-factors.md)

