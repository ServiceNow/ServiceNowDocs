---
title: Synchronization between an incident and its incident tasks
description: You can use Operational Technology \(OT\) incident tasks to collaborate with and request work from other stakeholders. An OT incident and its tasks are synchronized so that the state of the incident tasks change depending on the state of incident.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Synchronization between an incident and its incident tasks

You can use Operational Technology \(OT\) incident tasks to collaborate with and request work from other stakeholders. An OT incident and its tasks are synchronized so that the state of the incident tasks change depending on the state of incident.

The **com.snc.incident.ot\_incident\_task.closure** property closes open incident tasks when the related incident is closed or canceled. This property is responsible for different actions that take place on OT incident tasks based on the state of the OT incident.

The synchronization between an OT incident and its open OT incident task is as follows:

-   When an OT incident is closed, the state of any open OT incident task is set to **Closed Incomplete**.
-   When an OT incident is canceled, the state of any open OT incident task is set to **Closed Skipped**.

**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)

