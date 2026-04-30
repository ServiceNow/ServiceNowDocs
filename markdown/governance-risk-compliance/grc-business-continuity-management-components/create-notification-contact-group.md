---
title: Create a notification contact group
description: Create a notification contact group using the ServiceNow AI Platform groups. Use the group members as contacts for emergency notification. Synchronize the group members as contacts with Everbridge and track the non-synchronized members as exceptions.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup steps for emergency notification, Integrating Crisis Management with Everbridge, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a notification contact group

Create a notification contact group using the ServiceNow AI Platform groups. Use the group members as contacts for emergency notification. Synchronize the group members as contacts with Everbridge and track the non-synchronized members as exceptions.

## Before you begin

Role required: BCM admin \(sn\_bcm.admin\)

## Procedure

1.  Navigate to **Business Continuity** &gt; **Everbridge Contact Configuration** &gt; **Notification Contact Groups**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_u1t_44f_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group

</td><td>

Reference to the User Group table.

</td></tr><tr><td>

Sync status

</td><td>

Defaults to **New** when the group is created.-   **Success**: The contact group is successfully synchronized with Everbridge.
-   **Error**: If there is an error in syncing.
-   **Updated**: If the contact group is modified.


</td></tr><tr><td>

Last sync on

</td><td>

Auto-populates the date on which the group was last synchronized with Everbridge.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  To synchronize the group with the groups in Everbridge, click **Sync Groups to Everbridge**.

    Refresh the page to get the synchronized status of the group.

    If a group did not synchronize with Everbridge, then you get an error message.

6.  To view the names of the group members that did not synchronize with Everbridge, click **Group User Exceptions** related list.


## Example

There are five members in a group, out of which four members are already synced with Everbridge and existing as contacts. When you synchronize the group, a group is created in Everbridge with the four synced group members. However, the unsynchronized single member is logged as an exception displaying a message as to why the syncing failed.

You can synchronize this particular contact first and then the group with Everbridge.

