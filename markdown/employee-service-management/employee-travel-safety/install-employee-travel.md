---
title: Install Employee Travel Safety
description: You can install Employee Travel Safety if you have the admin role.Several types of components are installed with Employee Travel Safety, including user roles and tables.
locale: en-US
release: australia
product: Employee Travel Safety
classification: employee-travel-safety
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Employee Travel Safety, Safe Workplace, Health and Safety, Employee Service Management]
---

# Install Employee Travel Safety

You can install Employee Travel Safety if you have the admin role.

## Before you begin

Employee Travel Safety requires the following applications.

-   ServiceNow® Employee Readiness Core
-   ServiceNow® COVID-19 Global Health Data Set

The ServiceNow® Employee Health Screening and ServiceNow® Emergency Outreach applications can optionally be installed to have employees complete a daily health verification before and during travel.

The ServiceNow® Contact Tracing and Emergency Outreach applications can optionally be installed to have employees complete a daily contact log during travel.

Role required: admin

<table id="table_kxr_yz3_blb"><thead><tr><th>

Type

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Commercial on-premise

</td><td>

Visit the ServiceNow® Store to download and install the application.

</td></tr><tr><td>

Federal hosted

</td><td>

See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

Federal on-premise

</td><td>

If you are a federal on-premise customer and you would like to install this application, reach out to your sales representative or open a Now Support or HIWAVE ticket. In the ticket, request to be routed to the SHOT team.

 See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

On-premise

</td><td>

See the [Commercial downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030258\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030258) article in the Store Help Center for more information.

</td></tr></tbody>
</table>If you've subscribed to the Safe Workplace suite and you already have some of the apps installed, refer to the following order of installation for the remaining apps.

-   Emergency Outreach \(sn\_imt\_checkin\)
-   Employee Health Screening \(sn\_imt\_monitoring\)
-   Workplace PPE Inventory Management \(sn\_imt\_ppe\)
-   Employee Readiness Surveys \(sn\_imt\_readiness\)
-   COVID-19 Global Health Data Set \(sn\_imt\_c19datafeed\)
-   Contact Tracing \(sn\_imt\_tracing\)
-   Emergency Self Report \(sn\_imt\_quarantine\)
-   Workplace Core \(sn\_wsd\_core\)
-   Safe Workplace Dashboard \(sn\_imt\_dashboard\)
-   Emergency Response Management for Now Mobile \(sn\_imt\_mobile\)
-   Employee Travel Safety \(sn\_imt\_travel\)
-   Health and Safety Testing \(sn\_imt\_health\_test\)
-   Vaccination Status \(sn\_imt\_vaccine\)

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Employee Travel Safety`.

3.  Click **Install**.

    The Application installation dialog box opens.

4.  Click **Activate**.


**Parent Topic:**[Employee Travel Safety](../concept/employee-travel-safety.md)

## Components installed with Employee Travel Safety

Several types of components are installed with Employee Travel Safety, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Employee Travel Safety admin\[sn\_imt\_travel.admin\]

</td><td>

Role required to set up Employee Travel Safety properties.

</td><td>

sn\_imt\_travel.approver

</td></tr><tr><td>

Travel approver\[sn\_imt\_travel.approver\]

</td><td>

Role required to view and approve travel requests for all employees. This role is assigned to the Travel Approvers group.**Note:** Managers must be assigned the approver\_user role to approve travel for the employees that they supervise. Don't assign managers the sn\_imt\_travel.approver role unless it's acceptable for them to view and approve travel requests for all employees.

</td><td>

approver\_user

</td></tr></tbody>
</table>### Tables installed

<table id="table_udb_2hn_2mb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee Travel Safety Request\[sn\_imt\_travel\_request\]

</td><td>

List of all employee travel requests.

</td></tr></tbody>
</table>