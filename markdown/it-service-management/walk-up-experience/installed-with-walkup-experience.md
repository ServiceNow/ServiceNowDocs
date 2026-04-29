---
title: Components installed with Walk-up Experience
description: Several types of components are installed with activation of the Walk-up Experience plugin, including tables and user roles.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Walk-up Experience reference, Walk-up Experience, IT Service Management]
---

# Components installed with Walk-up Experience

Several types of components are installed with activation of the Walk-up Experience plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

<table id="table_ngk_1jg_zdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Walk-up login\[sn\_walkup.walkup\_login\]

</td><td>

Used to log into the onsite Walk-up Experience portal when needed. For example, at the beginning of the work day for an agent. **Note:** This role is assigned to a user record for purposes of logging into the check-in device, typically a tablet, at the on-site Walk-up Experience portal. It is not an actual human being with an assigned role, but an account used to log into the on-site portal devices. The user record can be assigned only this role in order to access the onsite Walk-up Experience portal. The user record account cannot contain any other associated roles. For security reasons, the Walk-up Experience portal cannot be accessed using the admin role.

</td><td>

None

</td></tr><tr><td>

Walk-up technician\[sn\_walkup.walkup\_technician\]

</td><td>

Works at the Walk-up Experience location to fulfill customer demands, such as IT-related issues and requests.

</td><td>

-   interaction\_agent
-   workspace\_agent
-   awa\_agent
-   sn\_apptmnt\_booking.appointment\_booking\_user

</td></tr><tr><td>

Walk-up manager\[sn\_walkup.walkup\_manager\]

</td><td>

Manages the technicians at the Walk-up Experience location.

 Access the Walk-up Experience Dashboard to oversee and monitor operations and performance.

</td><td>

-   sn\_walkup.walkup\_technician
-   sn\_apptmnt\_booking.appointment\_booking\_manager

</td></tr><tr><td>

Walk-up administrator\[sn\_walkup.walkup\_admin\]

</td><td>

Administers and configures Walk-up Experience modules.

</td><td>

-   sn\_walkup.walkup\_manager
-   inventory\_admin
-   schedule\_admin
-   sp\_admin
-   sn\_apptmnt\_booking.appointment\_booking\_admin
-   awa\_admin

</td></tr></tbody>
</table><table id="table_k2k_bjg_zdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Walk-up Reason for Visit\[wu\_reason\]

</td><td>

Record used to define various common reasons why a user needs walk-up support.

</td></tr><tr><td>

Walk-up context\[wu\_context\]

</td><td>

Record used to configure an online check-in channel for requesters to join a walk-up queue before physically arriving at the walk-up location. Identifies a walk-up requester and the description of the associated interaction.

</td></tr><tr><td>

Walk-up Location Queue\[wu\_location\_queue\]

</td><td>

Record used to configure a walk-up location. Extends the Queue \[awa\_queue\] table.

</td></tr><tr><td>

Walk-up Reason\[wu\_m2m\_location\_queue\_reason\]

</td><td>

Record used to set the order a particular visit reason should be prioritized at a walk-up location.

</td></tr><tr><td>

Walk-up Appointment\[wu\_appointment\]

</td><td>

Record used to configure scheduled appointments. Extends the Task \[task\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Walk-up Experience reference](walk-up-experience-reference.md)

