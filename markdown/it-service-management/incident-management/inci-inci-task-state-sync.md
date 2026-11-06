---
title: Synchronization between an incident and its incident tasks
description: Use incident tasks to collaborate with and request work from other stakeholders. An incident and its tasks are synchronized so that incident task states change based on the state of the incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/inci-inci-task-state-sync.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Synchronization between an incident and its incident tasks

Use incident tasks to collaborate with and request work from other stakeholders. An incident and its tasks are synchronized so that incident task states change based on the state of the incident.

**Note:** The **Close open Incident Tasks when Incident is closed or canceled** property \(**com.snc.incident.incident\_task.closure**\) controls the actions taken on incident tasks based on the state of the incident.

Synchronization between an incident and its open incident tasks works as follows:

-   When an incident is closed, the state of any open incident task is set to **Closed Incomplete**.
-   When an incident is canceled, the state of any open incident task is set to **Closed Skipped**.

