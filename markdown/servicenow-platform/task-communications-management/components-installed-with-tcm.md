---
title: Components installed with Task Communications Management
description: Several types of components are installed with the Task Communications Management plugin, including tables and user roles.Provides overall accountability of Task Communications Management.This role has read access to Task Communications Management tables.This role has create and edit access to Task Communications Management instance tables such as Communication Plans, Communication Tasks. Users with this role can send impromptu communications.
locale: en-US
release: zurich
product: Task Communications Management
classification: task-communications-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Activate Task Communications Management, Task Communications Management plugins, Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Task Communications Management

Several types of components are installed with the Task Communications Management plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Tables installed

<table id="table_hbc_kml_2db"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Communication Plan Type Lookup\[comm\_plan\_type\_lookup\]

</td><td>

Stores the communication plan types.

</td></tr><tr><td>

Communication Task Type Lookup\[comm\_task\_type\_lookup\]

</td><td>

Stores the communication task types.

</td></tr><tr><td>

Communication Plan Definition\[comm\_plan\_definition\]

</td><td>

The definition table for the communication plan entity.

</td></tr><tr><td>

Communication Task Definition\[comm\_task\_definition\]

</td><td>

The definition table for the communication task entity.

</td></tr><tr><td>

Communication Channel Definition\[comm\_channel\_definition\]

</td><td>

Main table for channel definitions.

</td></tr><tr><td>

Communication Channel Definition — Email\[comm\_channel\_def\_email\]

</td><td>

Defines email as a channel.

</td></tr><tr><td>

Communication Channel Definition — SMS\[comm\_channel\_def\_sms\]

</td><td>

Defines SMS as a channel.**Note:** This table is available only when you install the Notify plugin \(com.snc.notify\).

</td></tr><tr><td>

Communication Channel Definition — Conference\[comm\_channel\_def\_conference\]

</td><td>

Defines Conference as a channel.**Note:** This table is available only when the Notify plugin \(com.snc.notify\) is installed.

</td></tr><tr><td>

Communication Contact Definition\[comm\_contact\_definition\]

</td><td>

Defines the contacts for sending out communications. Contacts can be users, groups, or recipient lists.

</td></tr><tr><td>

Communication Channel Configuration\[comm\_channel\_config\]

</td><td>

Lists all available channels for an instance.

**Note:** Configuration script for each channel is a script include.

</td></tr><tr><td>

Communication Plan\[comm\_plan\]

</td><td>

Stores the communication plan that outlines the communication activity during an event.

</td></tr><tr><td>

Communication Task\[comm\_task\]

</td><td>

Stores the task to be carried out to communicate with the involved contacts.

</td></tr><tr><td>

Communication Channel\[comm\_channel\]

</td><td>

Main table for channel instances.

</td></tr><tr><td>

Communication Channel — Email\[comm\_channel\_email\]

</td><td>

Stores record that indicate email is used as a communication channel for a communication task.

</td></tr><tr><td>

Communication Channel — SMS\[comm\_channel\_sms\]

</td><td>

Stores record that indicate SMS is used as a communication channel for a communication task.

</td></tr><tr><td>

Communication Channel — Conference\[comm\_channel\_conference\]

</td><td>

Stores record that indicate conference is used as a communication channel for a communication task.

</td></tr><tr><td>

Communication Task Handler\[comm\_task\_handler\]

</td><td>

Lists specific handlers for various task types. Example: For incident, CommunicationManagementIncidentHandler. **Note:** Users with the admin role cannot delete this table.

</td></tr></tbody>
</table>## Roles installed

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Activate Task Communications Management](../task/activate-tcm-plugin.md)

## Communication Plan Admin \[sn\_comm\_management.comm\_plan\_admin\]

Provides overall accountability of Task Communications Management.

### Contains Roles

List of roles contained within the role.

-   Notifications administrator \[notify\_admin\]
-   Publications recipients list user \[sn\_publications\_recipients\_list\_user\]

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

This role has create and edit access to Task Communications Management tables including Communication Plan Definitions and other related records.

## Communication Plan Viewer \[sn\_comm\_management.comm\_plan\_viewer\]

This role has read access to Task Communications Management tables.

### Contains Roles

List of roles contained within the role.

-   Notification viewer \[notify\_view\]
-   Publications recipients list user \[sn\_publications\_recipients\_list\_user\]

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Communication Plan Manager \[sn\_comm\_management.comm\_plan\_manager\]

This role has create and edit access to Task Communications Management instance tables such as Communication Plans, Communication Tasks. Users with this role can send impromptu communications.

### Contains Roles

The Communication Plan Manager \[sn\_comm\_management.comm\_plan\_manager\] role contains the Communication Plan Viewer \[sn\_comm\_management.comm\_plan\_viewer\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

