---
title: Add staff members to a business location in the Business Location Service Portal
description: Add users as staff members to a business location to support accounts, contacts, consumers, and households.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using the Business Location Service Portal, Customer communication, Use, Customer Service Management]
---

# Add staff members to a business location in the Business Location Service Portal

Add users as staff members to a business location to support accounts, contacts, consumers, and households.

## Before you begin

Role required: admin, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## About this task

Add internal and external members to a business location. You can add both internal users with the snc\_internal role and external users with the snc\_external role as staff members to an external business location.

-   Administrators and customer service managers can add staff members to any business location.
-   Location managers can add staff members to the business locations that they have access to.

**Note:** As a user with the sn\_customerservice.svc\_location\_manager role, you can create both internal and external staff members. However, as a user with the sn\_customerservice.svc\_location\_manager\_contributor role, you can only create external staff members.

## Procedure

1.  Navigate to **Home** &gt; **Busines Location Support** &gt; **Services**.

2.  Select **Register Member at External Business Location** to open the Register Member at External Business Location record.

    You can use the record to register new location staff or move existing staff between locations managed by the Location manager, and assign responsibilities to staff accordingly.

3.  On the form, fill in the fields.

<table id="table_dd4_j55_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

External Business Location

</td><td>

The external business location. This field is automatically generated.

</td></tr><tr><td>

Register Staff

</td><td>

Field used to register new location staff or move existing staff from an external business location hierarchy between locations.-   **New Staff**: Create a user in External Organization Staff \(sn\_csm\_service\_organization\_external\_staff\) table with \(snc\_external\) role.
-   **Existing Staff**: List of staff members already working under the service organization hierarchy.


</td></tr><tr><td>

First Name

</td><td>

First name of the staff member.

</td></tr><tr><td>

Last Name

</td><td>

Family name of the staff member.

</td></tr><tr><td>

User ID

</td><td>

User ID of the staff member.

</td></tr><tr><td>

Email

</td><td>

Email address of the staff member.

</td></tr><tr><td>

Member

</td><td>

Field used to select an external staff member from the list of service organization external staff record.**Note:** The **Member** field appears only when **Existing Staff** is selected from the **Register staff** field.

</td></tr><tr><td>

Member Type

</td><td>

Field used to assign responsibility for the selected business location.-   **None**: Creates a member record.
-   **Listed Member**: Creates a member record. With the member record, a responsibility record is created with the type as Listed Member and the responsibility as empty.
-   **Location Contributor**: Creates a member record. With the member record, a responsibility record is created with the type as Location Contributor and responsibility as the Location Contributor.
 **Note:** Assigning responsibility is applicable to both existing and new staff members.

</td></tr></tbody>
</table>4.  Select **Submit**.

    Additionally, the external business location record is created in the **Service Organization** field of the service organization external staff \[sn\_csm\_service\_organization\_external\_staff\] table.

    A new external staff member record is created for the selected external business location. The admin must assign responsibilities to the staff members. However, if you have selected **None** as a member type, then you must not create a responsibility record.


## Result

Once a staff member is added to a business location, the following details can be accessed from the **Business Location Details** tab:

-   Cases Requested
-   Members
-   Available Services
-   Accounts
-   Consumers
-   Households
-   Child Business Locations
-   Projects

**Related topics**  


[Create cases for a business location in the Business Location Service Portal](report-cases-on-behalf-of-biz-location.md)

[Track cases on the Business Location Service Portal](../concept/track-cases-for-blsp-portal.md)

