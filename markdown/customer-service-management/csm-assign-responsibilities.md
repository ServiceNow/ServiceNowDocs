---
title: Assign responsibilities
description: Use the responsibility data model to assign responsibilities to an organization member.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-assign-responsibilities.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Assign responsibilities

Use the responsibility data model to assign responsibilities to an organization member.

## Before you begin

Role required: admin

## About this task

Use the responsibility data model to assign multiple responsibilities to a single organization member across different business organizations. For hierarchy responsibilities you can assign the same responsibility to a user at multiple locations. Each assignment has its own assignment point and excluded locations list. The user's effective access is the union of all assignments, minus excluded and restricted locations.

The responsibility data model tracks the relationship between the organization members and their responsibility type in the Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\] table.

**Note:** If the business organization plugin is active, this feature is enabled by default. However, for upgrade customer, the data in the \[sn\_csm\_svc\_org\_member\_responsibility\] table will be auto-populated for existing organization members to confirm that they retain as much access after the upgrade. Any new records created after the Australia release must be created using the following steps.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal/External Organizations**.

2.  Open the business organization \(internal or external\) record.

3.  Open the Organization Member record from the Members related list.

4.  Select **New** to create a record in the Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\] table.

    The Organization Member Responsibility record shows the following fields:

    1.  **Member**: Refers to the \[sn\_csm\_service\_organization\_member\] table and is auto-populated if the record is initiated from the Organization Member related list.
    2.  **Type**: Refers to the \[sn\_customerservice\_related\_party\_configuration\] table
    3.  **Order**: Refers to the sequence in which records are displayed, organized according to business preferences.
    4.  **Excluded Organizations**: Exclude the following child organizations from hierarchy-based access for this user.
    **Note:**

    With the base system, users with a specific role can be assigned a particular type.

<table id="table_wzl_3yr_ptb"><thead><tr><th>

Responsibility

</th><th>

Name

</th></tr></thead><tbody><tr><td>

Location Agent**Note:** This role only applies to the internal business organization.

</td><td>

sn\_customerservice.svc\_location\_agent

</td></tr><tr><td>

Location Consumer Agent**Note:** This role only applies to the internal business organization.

</td><td>

sn\_customerservice.svc\_location\_consumer\_agent

</td></tr><tr><td>

Location Contributor

</td><td>

sn\_customerservice.service\_organization\_contributor

</td></tr><tr><td>

Location Manager Contributor

</td><td>

sn\_customerservice.svc\_location\_manager\_contributor

</td></tr><tr><td>

Location Manager Fulfiller**Note:** This role only applies to the internal business organization.

</td><td>

sn\_customerservice.svc\_location\_manager

</td></tr><tr><td>

Location Relationship Manager**Note:** This role only applies to the external business organization.

</td><td>

sn\_bus\_loc.location\_relationship\_manager

</td></tr><tr><td>

Location Support Agent

</td><td>

sn\_bus\_loc.svc\_location\_support\_agent

</td></tr></tbody>
</table>5.  After you assign the required related party type, select **Submit**.

    A new responsibility is added to the organization member.


