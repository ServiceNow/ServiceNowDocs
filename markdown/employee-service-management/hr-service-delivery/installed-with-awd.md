---
title: Components installed with HR Service Delivery Advanced Integration with Workday
description: Several types of components are installed with activation of the HR Service Delivery Advanced Integration with Workday, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Components installed with HR Service Delivery Advanced Integration with Workday

Several types of components are installed with activation of the HR Service Delivery Advanced Integration with Workday, including tables, user roles, and scheduled jobs.

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Advanced Workday Admin\[sn\_hr\_workday\_adv.admin\]

</td><td>

-   Can configure Workday reports.
-   Can customize Total rewards templates.
-   Can configure Legal name change settings.
-   Can import time offs from Workday.
-   Can pull holiday calendars and schedule calendars from Workday.
-   Can pull Workday reference IDs.

</td><td>

-   flow\_operator
-   import\_admin

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time Offs\[sn\_hr\_workday\_time\_offs\]

</td><td>

Stores details of time offs, such as time off ID, and references to time off plan, and time off type.

</td></tr><tr><td>

Time Off Plans\[sn\_hr\_workday\_time\_off\_plans\]

</td><td>

Stores details of time off plans, such as time off plan ID, unit of time, and daily quantity.

</td></tr><tr><td>

Time Off Types\[sn\_hr\_workday\_time\_off\_types\]

</td><td>

Stores details of time offs types, such as time off type ID.

</td></tr><tr><td>

Time Off Reasons\[sn\_hr\_workday\_time\_off\_reasons\]

</td><td>

Stores details on time off reasons such as time off reason ID and reference to time off.

</td></tr><tr><td>

Absence Table\[sn\_hr\_workday\_absence\_table\]

</td><td>

Stores the Absence table ID and Reason required fields.

</td></tr><tr><td>

Absence Table Tiers\[sn\_hr\_workday\_absence\_table\_tiers\]

</td><td>

Stores the combination of leave plans and time offs. For example, combination of time off plan \(USA Sick Plan \(GPS\) and time off USA Sick Time Off GPS\).

</td></tr><tr><td>

Absence Table Reasons\[sn\_hr\_workday\_absence\_table\_reasons\]

</td><td>

Stores reasons of the Absence table.

</td></tr><tr><td>

Holiday Calendar\[sn\_hr\_workday\_holiday\_calendar\]

</td><td>

Stores details of holiday calendars \(such as holiday calendar name, start date, and end date\) that are pulled from Workday.

</td></tr><tr><td>

Work Schedule Calendar\[sn\_hr\_workday\_work\_schedule\_calendar\]

</td><td>

Stores details of work schedule calendars \(such as work schedule calendar name, ID, and pattern start date\) that are pulled from Workday.

</td></tr><tr><td>

Legal Name Change Configuration\[n\_hr\_workday\_adv\_legal\_name\_change\_configuration\]

</td><td>

Stores the configuration options that are set for legal name change.

</td></tr><tr><td>

Workday Reference ID List\[sn\_hr\_workday\_adv\_reference\_id\_list\]

</td><td>

Stores the legal name change document categories and total rewards \(plans\) that are pulled from Workday.

</td></tr><tr><td>

Workday Report Configuration\[sn\_hr\_workday\_adv\_report\_configuration\]

</td><td>

Stores details of reports that are created in Workday. For example, name of the report, owner of the report, and purpose of creating the report.

</td></tr><tr><td>

Total Rewards Section Setup\[sn\_hr\_workday\_adv\_total\_rewards\_section\_setup\]

</td><td>

Stores details of Total Rewards sections with plans associated to it.

</td></tr><tr><td>

Total Rewards Template Setup\[sn\_hr\_workday\_adv\_total\_rewards\_template\_setup\]

</td><td>

Store details of Total Rewards templates with sections and plans associated to it.

</td></tr></tbody>
</table>**Parent Topic:**[Reference](reference-hr-service-delivery-advanced-integration-with-workday.md)

