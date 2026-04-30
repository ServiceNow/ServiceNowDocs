---
title: Synchronization between an incident and its incident tasks
description: Use incident tasks to collaborate with and request work from other stakeholders. An incident and its tasks are synchronized such that the state of incident tasks changes depending on the state of the incident.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# Synchronization between an incident and its incident tasks

Use incident tasks to collaborate with and request work from other stakeholders. An incident and its tasks are synchronized such that the state of incident tasks changes depending on the state of the incident.

**Note:** The **Close open Incident Tasks when Incident is closed or canceled** property \(**com.snc.incident.incident\_task.closure**\) is responsible for different actions that take place on incident tasks based on the state of the incident.

The synchronization between an incident and its open incident task is as follows:

-   When an incident is closed, the state of any open incident task is set to **Closed Incomplete**.
-   When an incident is canceled, the state of any open incident task is set to **Closed Skipped**.

