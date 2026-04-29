---
title: Assigning alert assignment group precedence
description: Assign alert assignment group precedence to make sure that alerts are routed to the appropriate team members.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Alert assignment groups for teams, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Assigning alert assignment group precedence

Assign alert assignment group precedence to make sure that alerts are routed to the appropriate team members.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and search for `sys_properties.list`.

2.  In the **Search** field, enter `evt_mgmt.alert_auto_assignment_field` and select the property record.

    For more information on the property, see [Team-based integration properties](../reference/team-based-integrations-properties.md).

3.  In the **Value** field, enter the assignment group precedence.

    Set the assignment group precedence according to the order of the comma-separated fields such as cmdb\_ci.support\_group, IntegrationGroup.

4.  Select **Update**.


**Parent Topic:**[Alert assignment groups for teams](../concept/alert-assignment-group.md)

**Related topics**  


[Team-based integration properties](../reference/team-based-integrations-properties.md)

