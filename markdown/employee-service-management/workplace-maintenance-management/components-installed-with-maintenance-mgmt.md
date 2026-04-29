---
title: Components installed with Workplace Maintenance Management
description: Different roles and components or tables are available with the installation of Workplace Maintenance Management.
locale: en-US
release: australia
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workplace Maintenance Management references, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Maintenance Management

Different roles and components or tables are available with the installation of Workplace Maintenance Management.

## Roles installed with Workplace Maintenance Management

Navigate to **All** &gt; **System Definition** &gt; **Roles** &gt; **.**

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_wsd\_wc.manager|Provides read access to all data including Occupancy Dashboard and other dashboards.|sn\_wsd\_wc.user|
|sn\_wsd\_wc.admin|Provides admin access to configure and set up the Workplace Connectors application|sn\_wsd\_wc.manager|
|sn\_wsd\_wc.user|Provides read access to only a few columns and fields. The read access is set up by administrators.|None|

## Tables installed with Workplace Maintenance Management

Navigate to **All** &gt; **System Definition** &gt; **Tables.**

<table id="table_t5k_1kj_qpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Maintenance Plan\[sn\_wsd\_maintenance\_plan\]

</td><td>

Stores preventive maintenance plans.

</td></tr><tr><td>

Workplace Maintenance Plan Items\[sn\_wsd\_maintenance\_m2m\_plan\_maint\_item\]

</td><td>

Stores all the items \(locations or assets\) that are part of a maintenance plan.

</td></tr><tr><td>

Workplace Maintenance Schedule

\[sn\_wsd\_maintenance\_schedule\]

</td><td>

Stores all the schedules \(daily, weekly, monthly and so on\) created for a Maintenance plan.

</td></tr><tr><td>

Create a maintenance case

 \[sn\_wsd\_maintenance\_case\]

</td><td>

Stores information about maintenance cases.

</td></tr><tr><td>

Maintenance Plan Record\[sm\_m2m\_maint\_plan\_to\_record\]

</td><td>

Stores the plan records \(a record for every schedule and maintenance item combined\).

</td></tr><tr><td>

Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\)

</td><td>

Associates workplace services and sets scheduling conditions for a plan record. The schedule job fetches plan records that have a maintenance schedule template for a workplace service to create maintenance cases. For more information, see [Create plan service configuration](../task/create-maint-service-config.md) and [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md).

</td></tr></tbody>
</table>## Workplace Maintenance Management Scheduled Jobs

Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs.**

<table id="table_ylk_m4d_gzb"><thead><tr><th>

Scheduled Job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Planned Maintenance Nightly Run

</td><td>

A scheduled job runs every 48 hours \(2 days\) to fetch plan records and create maintenance cases. For more information, see [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md).

</td></tr><tr><td>

Workplace Maintenance Case Daily Data Collection

</td><td>

This scheduled job collects data and populates it in the Workplace Maintenance Management Dashboard.Collects data as specified in the Relative start and Relative end fields. The collection time is time zone specific.

</td></tr><tr><td>

Workplace Maintenance Case Historical Data Collection

</td><td>

This scheduled job collects historical data and populates it in the Workplace Maintenance Management Dashboard.Collects data as specified in the Relative start and Relative end fields. The collection time is time zone specific.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Maintenance Management references](../concept/workplace-maintenance-mgmt-references.md)

**Previous topic:**[Maintenance plan schedule examples](../concept/maintenance-plan-examples.md)

**Next topic:**[Workplace Lease Administration](../../workplace-lease-administration/concept/workplace-lease-admin-feat.md)

