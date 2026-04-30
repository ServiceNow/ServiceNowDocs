---
title: Resolve an incident related to an alert
description: When you resolve an incident that is associated with an alert, the alert can also close according to the evt\_mgmt.incident\_closes\_alert property.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Resolve an incident related to an alert

When you resolve an incident that is associated with an alert, the alert can also close according to the **evt\_mgmt.incident\_closes\_alert** property.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## Procedure

1.  Open an incident.

2.  Click **Resolve Incident**.

    The corresponding alert is closed, resolved, or left alone as specified by the **evt\_mgmt.incident\_closes\_alert** system property.

    The alert may not close immediately when the incident is closed. Depending on the value of the **evt\_mgmt.alert\_rule\_close\_delay** parameter, the alert may close 5 seconds after the last alert update. This value \(in seconds\) is defined in the parameter. To use the property, you need to create the property with the same name and assign the required value to it. For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).


**Parent Topic:**[Manage and monitor alerts](../concept/c_EMAlert.md)

