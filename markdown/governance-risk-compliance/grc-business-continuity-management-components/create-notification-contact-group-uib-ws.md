---
title: Create notification contact groups
description: Create a notification contact group using the ServiceNow AI Platform groups. Use the group members as the contacts for an emergency notification. Synchronize the group members as the contacts with Everbridge and track the non-synchronized members as exceptions.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup for Everbridge notifications, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create notification contact groups

Create a notification contact group using the ServiceNow AI Platform groups. Use the group members as the contacts for an emergency notification. Synchronize the group members as the contacts with Everbridge and track the non-synchronized members as exceptions.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **Business Continuity** &gt; **Everbridge Contact Configuration** &gt; **Notification Contact Groups**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information, see [Notification Contact Group form](../reference/notification-contact-group-form.md).

4.  Select **Submit**.

5.  To synchronize the group with the groups in Everbridge, select **Sync Groups to Everbridge**.

    Refresh the page to get the synchronized status of the group.

    If a group is not synchronized with Everbridge, then you get an error message.

6.  To view the names of the group members that did not synchronize with Everbridge, select the **Group User Exceptions** related list.


## Example

There are five members in a group, out of which four members are already synced with Everbridge and existing as contacts. When you synchronize the group, a group is created in Everbridge with the four synced group members. However, the unsynchronized single member is logged as an exception displaying a message as to why the syncing failed.

You can synchronize this particular contact first and then the group with Everbridge.

-   **[Notification Contact Group form](../reference/notification-contact-group-form.md)**  
Use the Notification Contact Group form to create a notification contact group.

**Parent Topic:**[Setup for Everbridge notifications](../concept/setup-steps-for-emergency-notification-uib-ws.md)

