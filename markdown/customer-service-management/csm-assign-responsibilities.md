---
title: Assign responsibilities
description: Use the responsibility data model to assign responsibilities to a service organization \(SO\) member.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Assign responsibilities

Use the responsibility data model to assign responsibilities to a service organization \(SO\) member.

## Before you begin

Role required: admin

## About this task

Businesses often need staff to work at more than one business location, and they can have different responsibilities at different locations. Using the responsibility data model, an SO member can be assigned multiple responsibilities.

The responsibility data model maintains the relationship between the SO member and the type of responsibility within the Service Organization Member Responsibilities \[sn\_csm\_svc\_org\_member\_responsibility\] table.

**Note:** If the business location plugin is active, this feature is enabled by default. However, for upgrade customers, the data in the \[sn\_csm\_svc\_org\_member\_responsibility\] table will be auto-populated for existing SO members to ensure that they retain as much access after the upgrade. Any new records created after the Xanadu release must be created using the following steps.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Service Organizations** &gt; **Internal/External Business Locations**.

2.  Open the business location \(internal or external\) record.

3.  Open the SO Member record from the Members related list.

4.  Select **New** to create a record in the SO Member Responsibilities \[sn\_csm\_svc\_org\_member\_responsibility\] table.

    The Service Organization Member Responsibility record shows two fields: **Member** and **Type**.

    **Note:** The **Member** field refers to the \[sn\_csm\_service\_organization\_member\] table. This field is auto-populated if the record is initiated from the SO Member related list, while the **Type** field refers to the \[sn\_customerservice\_related\_party\_configuration\] table.

    With the base system, users with a specific role can be assigned a particular type.

<table id="table_wzl_3yr_ptb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_customerservice.svc\_location\_agent

</td><td>

Location Agent**Note:** This role only applies to the internal business location.

</td></tr><tr><td>

sn\_customerservice.svc\_location\_consumer\_agent

</td><td>

Location Consumer Agent**Note:** This role only applies to the internal business location.

</td></tr><tr><td>

sn\_customerservice.service\_organization\_contributor

</td><td>

Location Contributor

</td></tr><tr><td>

sn\_customerservice.svc\_location\_manager\_contributor

</td><td>

Location Manager Contributor

</td></tr><tr><td>

sn\_customerservice.svc\_location\_manager

</td><td>

Location Manager Fulfiller**Note:** This role only applies to the internal business location.

</td></tr><tr><td>

sn\_bus\_loc.location\_relationship\_manager

</td><td>

Location Relationship Manager**Note:** This role only applies to the external business location.

</td></tr><tr><td>

sn\_bus\_loc.svc\_location\_support\_agent

</td><td>

Location Support Agent

</td></tr></tbody>
</table>5.  After you assign the required related party type, select **Submit**.

    A new responsibility is added to the SO member.


