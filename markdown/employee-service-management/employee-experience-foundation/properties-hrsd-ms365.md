---
title: Properties installed with HR Service Delivery for Microsoft 365
description: The following properties are installed with the HR Service Delivery for Microsoft 365 plugin.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Properties installed with HR Service Delivery for Microsoft 365

The following properties are installed with the HR Service Delivery for Microsoft 365 plugin.

**Note:** The following properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_hqx_h2w_y1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_now\_teams\_hr.enable\_va\_comment\_notification

</td><td>

Use this property to enable the comment notifications sent by the Virtual Agent sys\_notification.-   Type: true\|false
-   Default value: true

</td></tr><tr><td>

sn\_now\_teams\_hr.hr\_case\_allow\_list\_for\_teams\_chat\_actions

</td><td>

List of HR Case tables for which the **Start Chat** and **Import Messages** UI actions are available. The default list doesn’t include sensitive HR Cases like Employee Relations, Investigation, and Ethics.-   Type: string
-   Default value: sn\_hr\_core\_case,sn\_hr\_core\_case\_benefits,sn\_hr\_core\_case\_compensation,sn\_hr\_core\_case\_corporate\_communication,sn\_hr\_core\_case\_global\_mobility,sn\_hr\_core\_case\_operations,sn\_hr\_core\_case\_payroll,sn\_hr\_core\_case\_performance,sn\_hr\_core\_case\_talent\_management,sn\_hr\_core\_case\_total\_rewards,sn\_hr\_core\_case\_workforce\_admin,sn\_hr\_le\_case

</td></tr><tr><td>

sn\_now\_teams\_hr.chat\_sn\_hr\_core\_task\_fields

</td><td>

List of HR Task table fields that are displayed as recommended participants for the Start Chat feature.-   Type: string
-   Default value: assigned\_to

</td></tr><tr><td>

sn\_now\_teams\_hr.respond\_to\_comment\_notification\_inclusion\_list\_for\_hr

</td><td>

List of HR Case tables for which the Respond to Comment actionable notifications are sent. This default list doesn’t include sensitive HR Cases like Employee Relations, Investigation, and Ethics.-   Type: string
-   Default value: sn\_hr\_core\_case,sn\_hr\_core\_case\_benefits,sn\_hr\_core\_case\_compensation,sn\_hr\_core\_case\_corporate\_communication,sn\_hr\_core\_case\_global\_mobility,sn\_hr\_core\_case\_operations,sn\_hr\_core\_case\_payroll,sn\_hr\_core\_case\_performance,sn\_hr\_core\_case\_talent\_management,sn\_hr\_core\_case\_total\_rewards,sn\_hr\_core\_case\_workforce\_admin,sn\_hr\_le\_case,sn\_hr\_core\_task

</td></tr><tr><td>

sn\_now\_teams\_hr.chat\_sn\_hr\_core\_case\_fields

</td><td>

List of HR Case table fields that are displayed as recommended participants for the Start Chat feature.-   Type: string
-   Default value: opened\_for,subject\_person,collaborators

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow for Microsoft Teams reference](reference-sn-teams.md)

