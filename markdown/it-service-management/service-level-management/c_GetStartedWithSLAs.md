---
title: Service Level Agreement \(Legacy\) engines
description: If you are on an earlier version of the SLA engine, you can upgrade to the 2011 engine to make use of the complete service level management functionality.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Service Level Agreement \(Legacy\) engines

If you are on an earlier version of the SLA engine, you can upgrade to the 2011 engine to make use of the complete service level management functionality.

The SLA engine has three versions:

<table id="table_fjl_jhc_cs"><thead><tr><th>

SLA engine version

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Escalation engine \(pre-2010\)

</td><td>

Tracks only one SLA per task.

</td></tr><tr><td>

The 2010 engine \(the Service level management plugin\)

</td><td>

Supports multiple SLAs per task. Business rules handle the processing of these SLAs while workflows handle notifications. The majority of logic is in a single large business rule called Process SLAs.

</td></tr><tr><td>

The 2011 engine \(also part of the Service level management plugin\)

</td><td>

The 2010 SLA engine functionality is concentrated into a number of script includes.Provides retroactive pause calculations and enables the customization of SLA condition processing through the use of condition rules.

</td></tr></tbody>
</table>-   **[Legacy SLA fields](c_LegacySLAFields.md)**  
Previously, only a single SLA could be attached to a task via the Escalation engine. The information for the SLA was stored in the task table using the **SLA Due**, **Made SLA**, and **Escalation** fields.
-   **[Upgrade SLA to 2011 engine](../task/t_MoveFromThe2010ToThe2011Engine.md)**  
You can upgrade SLA processing to use the 2011 Engine.
-   **[Organize the migration process](../task/t_OrganizeTheConversionProcess.md)**  
There are several ways to convert the old SLAs to the new Task SLAs.
-   **[Convert an SLA to an SLA Definition](../task/t_ConvertAnSLAToATaskSLA.md)**  
You must replicate the default SLA record as a new SLA definition.
-   **[Reactivate escalation engine](../task/t_ReactivateAnOldSLAEngine.md)**  
Escalation engine is replaced with 2011 SLA Engine.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

