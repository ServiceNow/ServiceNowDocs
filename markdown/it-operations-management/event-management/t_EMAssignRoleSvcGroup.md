---
title: Assign a role to a service group
description: Assign an Event Management role to the application service group to ensure that group members can manage and act on alerts.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Assign a role to a service group

Assign an Event Management role to the application service group to ensure that group members can manage and act on alerts.

## Before you begin

Configure a service group to enable users to manage application services or alert groups.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Services** &gt; **Service Group Responsibilities**.

2.  Click **New**.

3.  In the **Application Service Group** field, select the name of the service group.

4.  In the **Role** field, select an Event Management role:

    -   evt\_mgmt\_admin
    -   evt\_mgmt\_integration
    -   evt\_mgmt\_operator
    -   evt\_mgmt\_user
5.  Click **Submit**.

6.  To find users who are assigned to the role, navigate to **User Administration** &gt; **Users** &gt; **Roles** and search for the role.


**Parent Topic:**[Application services in Event Management](../concept/application-service-event-management.md)

**Related topics**  


[Roles installed with Event Management](../reference/r_InstalledWithEventManagement.md#)

