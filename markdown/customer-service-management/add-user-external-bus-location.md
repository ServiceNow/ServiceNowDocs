---
title: Add staff members to an external business location
description: Add users as staff members to an external business location to support accounts, contacts, consumers, and households.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Add staff members to a business location, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Add staff members to an external business location

Add users as staff members to an external business location to support accounts, contacts, consumers, and households.

## Before you begin

Role required: admin, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## About this task

You can add both internal users with the snc\_internal role and external users with the snc\_external role as staff members to an external business location.

-   Administrators and customer service managers can add staff members to any business location.
-   Location managers can add staff members to the business locations that they have access to.

**Note:** Adding new external staff members to the external business locations must be done using the service organization external staff module.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Service Organizations** &gt; **Business Locations** &gt; **External Business Locations**.

2.  Select the desired external business locations record.

3.  Click the **Register Member** related link to open the Register Member at External Business Location record.

    You can use the record to register new location staff or move existing staff between locations managed by the Location manager, and assign responsibilities to staff accordingly.

4.  On the form, fill in the fields.

<table id="table_dd4_j55_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

External Business Location

</td><td>

The automatically generated external business locations.

</td></tr><tr><td>

Register Staff

</td><td>

Field used to register new location staff or move existing staff from external business location hierarchy between locations.-   **New Staff**: Create a user in Service Organization External Staff \(sn\_csm\_service\_organization\_external\_staff\) table with \(snc\_external\) role.
-   **Existing Staff**: List of staff members already working under the service organization hierarchy.


</td></tr><tr><td>

First Name

</td><td>

First name of the staff member.

</td></tr><tr><td>

Last Name

</td><td>

Last name of the staff member.

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

Field used to select an external staff member from the list of service organization external staff record.**Note:** This field appears only when **Existing Staff** is selected from the **Register** staff field.

</td></tr><tr><td>

Member Type

</td><td>

Field used to assign responsibility for the selected business location.-   **None**: Creates a member record.
-   **Listed Member**: Creates a member record. With the member record, a responsibility record is created with the type as Listed Member and the responsibility is empty.
-   **Location Contributor**: Creates a member record and along with the member record, a responsibility record is created with the type as Location Contributor and the responsibility as Location Contributor.
 **Note:** Assigning responsibility is applicable to both existing and new staff members.

</td></tr></tbody>
</table>5.  Click **Submit**.

    A new external staff member record is created for the selected external business location. The admin must assign responsibilities to the staff members. However, if you've selected **None** as a member type, then you must not create a responsibility record.


