---
title: Repair Service Level Agreement \(SLA\)
description: SLA Administrators can repair SLA records to ensure SLA timing and duration information is accurate.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Service Level Management, Service Level Management, IT Service Management]
---

# Repair Service Level Agreement \(SLA\)

SLA Administrators can repair SLA records to ensure SLA timing and duration information is accurate.

Repair of SLAs is useful to determine accurate timing information if your system has SLA records that contain incorrect values. For example, you may need to repair SLA records as a result of:

-   Changing the SLA definition or SLA schedule for any task SLA that is still active.
-   Changing the conditions of the SLA definition for any task SLA that is still active.
-   Some other system anomaly.

The repair function removes the SLA record, then recreates and recalculates it from the start, including recreating the flow. The repair uses the history from the Task and if appropriate will also create new Task SLAs that did not previously exist. For example, a new Task SLA may be needed if a new SLA Definition has been added since an associated Incident was created or updated.

SLA repair does not use the history of dot-walk fields but considers only the final state of the dot-walk fields. For example, if a pause condition is set to an incident dot-walk field as `incident.caller_id.location` and in real time the location is set to London, and later changed to San Diego. Then, when the SLA repair runs, only the final location is considered. So, if SLA is in pause state when the `incident.caller_id.location` is San Diego, repair pauses immediately as it does not consider the previous London location.

You can repair single SLAs from the relevant form or multiple SLAs from relevant lists.

**Note:** SLA repair is not available on SLA definitions, as running a repair operation for an SLA definition could affect large numbers of records on your system, with significant performance impact.

You can also configure and manage SLA repair functions.

-   **[Configure SLA repair](../reference/r_ManageSLARepair.md)**  
Administrators can set SLA repair properties and view repair logs.
-   **[Repair SLA from a form](../task/t_RepairSLAFromAForm.md)**  
You can repair task SLA records from the Task form, or from the task SLA form for an SLA associated to a Task.
-   **[Repair SLAs from a list](../task/t_RepairSLAFromAList.md)**  
You can repair multiple SLA records from a list of task or SLA records.

**Parent Topic:**[Using Service Level Management](using-service-level-management.md)

