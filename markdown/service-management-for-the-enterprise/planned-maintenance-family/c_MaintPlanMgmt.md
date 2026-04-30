---
title: Managing maintenance plans
description: Planned Maintenance allows you to create, maintain, and schedule maintenance for equipment that requires regular maintenance.
locale: en-US
release: yokohama
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Planned Maintenance, Service Management]
---

# Managing maintenance plans

Planned Maintenance allows you to create, maintain, and schedule maintenance for equipment that requires regular maintenance.

The maintenance plan specifies the CI class, product model, or other criteria, such as location, and specifies the maintenance to be performed. The maintenance schedule specifies the timing, by specifying how often and when to perform the maintenance.

For example, you can configure a maintenance plan to inspect and clean all air conditioners for a particular product model. The maintenance schedule specifies that the inspection is performed every six months.

Maintenance plans and schedules also take into consideration service management work orders and facilities requests opened against that equipment.

## Timing the first maintenance

By default, the first planned maintenance is scheduled based on the timing entered in the schedule. For example, if you create a schedule to inspect the air conditioners every six months, the first maintenance occurs six months from the time that you created the schedule.

To schedule the date of the first maintenance:

1.  Navigate to the Maintenance Schedule form.
2.  Click the **Run on demand** related link.
3.  De-select the **Run now** field.
4.  In the **Select next run date** field, use the calendar to select the desired date.
5.  Save the date.
6.  Click **Schedule**. This updates the next run time for the maintenance plan records.

You can update any maintenance schedule as needed. For example, if the regular interval is due next month, you can select an earlier or later date to change when the maintenance occurs.

-   **[Create a maintenance plan](../task/t_CreateAMaintPlan.md)**  
When creating a maintenance plan, options on the form help to determine how and when maintenance should be performed.
-   **[Property settings for Planned Maintenance](../reference/planned-maint-properties.md)**  
You configure Planned Maintenance properties at **Planned Maintenance** &gt; **Properties**.
-   **[Configure a maintenance schedule](../task/t_DefineAMaintSched.md)**  
After creating a maintenance plan, define specific criteria for determining when the plan should be executed.
-   **[Associate a maintenance plan to filtered records](../task/t_AssocMaintPlanToFilterRec.md)**  
You can configure a maintenance plan with filtering criteria. For example, you can apply a maintenance plan to all records containing computers that start with "apple".
-   **[Associate a schedule template to matching records](../task/t_AssocSchedTempToMatchRec.md)**  
The instance adds templates to a maintenance schedule so the appropriate requests and tasks, such as work orders and facilities requests, can be auto-generated when a maintenance schedule runs.
-   **[Run a scheduled job to execute a maintenance schedule](../task/t_RunSchedJobToExecMaintSched.md)**  
Maintenance schedules are executed whenever the meter, duration, script, or condition criteria is met. You can also use the Schedule ad-hoc feature to run a maintenance schedule manually.
-   **[Run a maintenance schedule on demand](../task/t_RunAMaintSchedOnDemand.md)**  
Maintenance schedules are typically run using the scheduled job named Planned Maintenance Nightly Run. However, you may want to run the schedule immediately or change the date when a schedule runs.
-   **[View a maintenance log](../task/t_ViewAMaintLog.md)**  
You can view all maintenance performed on a particular CI, the next scheduled maintenance, and the last time maintenance was performed.

**Parent Topic:**[Planned Maintenance](c_SMPlanMaint.md)

