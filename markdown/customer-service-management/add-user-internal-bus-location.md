---
title: Add staff members to an internal organization
description: Add users as staff members to an internal organization \(formerly internal business location\) to support accounts, contacts, consumers, and households.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/add-user-internal-bus-location.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add staff members to a business organization, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Add staff members to an internal organization

Add users as staff members to an internal organization \(formerly internal business location\) to support accounts, contacts, consumers, and households.

## Before you begin

Role required: admin, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## About this task

You can add internal users with the snc\_internal role as staff members to an internal organization.

-   Administrators and customer service managers can add staff members to any business organization \(formerly business location\).
-   Location managers can add staff members to the business locations that they have access to.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal Organizations**.

2.  Select the desired internal organizations record.

3.  Select the **Register Member** related link to open the Register Member at Internal Organization \(formerly Register Member at Internal Business Location\) record.

    Use the record to register new location staff or transfer existing internal or external staff between locations managed by the Location Manager, and assign responsibilities accordingly.

4.  On the form, fill in the fields.

<table id="table_j3n_psh_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internal Organization

</td><td>

The automatically generated internal organization.

</td></tr><tr><td>

Member

</td><td>

Field used to select an internal staff member from the list of service organization internal staff record.

</td></tr><tr><td>

Member Type

</td><td>

Field used to assign responsibility for the member selected at the business organization.To learn more about responsibilities, see [Assign responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-assign-responsibilities.md).

</td></tr></tbody>
</table>5.  Select **Submit**.

    A member record with the selected member, member type, and business organization is created. After a member type is selected, the member is assigned to a responsibility automatically.


