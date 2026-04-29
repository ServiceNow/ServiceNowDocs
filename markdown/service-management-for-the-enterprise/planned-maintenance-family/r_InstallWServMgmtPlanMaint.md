---
title: Installed with SM Planned Maintenance
description: The SM Planned Maintenance core plugin also includes demo data.
locale: en-US
release: australia
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate Planned Maintenance, Planned Maintenance, Service Management]
---

# Installed with SM Planned Maintenance

The SM Planned Maintenance core plugin also includes demo data.

## Tables installed with SM Planned Maintenance

<table id="table_u5j_fry_dt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maintenance Plan Record\[sm\_m2m\_maint\_plan\_to\_record\]

</td><td>

Relates a maintenance schedule to a record in the system \(from a document ID\). Also contains information about the last time or value the schedule was run for the record and the next time or value when the schedule will run.

</td></tr><tr><td>

Schedule Template\[sm\_m2m\_schedule\_template\]

</td><td>

Relates a maintenance schedule to service management templates.

</td></tr><tr><td>

Maintenance Plan\[sm\_maint\_plan\]

</td><td>

Defines a maintenance plan, including which table and records the plan applies to.

</td></tr><tr><td>

Maintenance Schedule\[sm\_schedule\]

</td><td>

Defines a schedule that is part of a maintenance plan. A schedule can be duration, meter, condition, or script based.

</td></tr></tbody>
</table>## Roles installed with SM Planned Maintenance

|Role title \[name\]|Description|
|-------------------|-----------|
|plan\_maint\_admin|Administrator for planned maintenance.|

## Script includes installed with SM Planned Maintenance

|Script include|Description|
|--------------|-----------|
|PlannedMaintenanceUtils|Utilities for planned maintenance.|
|PlannedMaintenanceAjax|AJAX entry points into PlannedMaintenanceUtils.|

## Client scripts installed with SM Planned Maintenance

<table id="table_wtf_krf_w3"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update field display - trigger type chg

</td><td>

Maintenance schedule\[sm\_schedule\]

</td><td>

Updates the fields displayed on the maintenance schedule form based on the trigger type selected.

</td></tr><tr><td>

Update field display - repetition chg

</td><td>

Maintenance schedule\[sm\_schedule\]

</td><td>

Updates the fields displayed on the maintenance schedule form based on the repetition selected.

</td></tr><tr><td>

Update table when type changes

</td><td>

Maintenance plan\[sm\_maint\_plan\]

</td><td>

Updates the **table** field based on the selected models \(for model-based plans\).

</td></tr><tr><td>

Validate the every field

</td><td>

Maintenance schedule\[sm\_schedule\]

</td><td>

Verifies that the **every** field is a positive number; else it defaults to 1.

</td></tr><tr><td>

Update table when models change

</td><td>

Maintenance plan\[sm\_maint\_plan\]

</td><td>

Updates the **table** field based on the selected models \(for model-based plans\).

</td></tr></tbody>
</table>## Business rules installed with SM Planned Maintenance

<table id="table_ngl_zwx_dt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update maintenance plan record

</td><td>

Service Order\[sm\_order\]

</td><td>

Updates the maintenance records \[sm\_m2m\_maint\_plan\_to\_record\] once a service order is closed.

</td></tr><tr><td>

Update m2m schedule records

</td><td>

Maintenance schedule\[sm\_schedule\]

</td><td>

Recalculates the next value or next run time when **meter** or **duration** fields change.

</td></tr><tr><td>

Active changes

</td><td>

Maintenance Plan Record\[sm\_m2m\_maint\_plan\_to\_record\]

</td><td>

Handles changes to the active flag for a maintenance plan record.

</td></tr><tr><td>

Active insert

</td><td>

Maintenance Plan Record\[sm\_m2m\_maint\_plan\_to\_record\]

</td><td>

Handles changes to the active flag for a maintenance plan record.

</td></tr><tr><td>

Active changes

</td><td>

Maintenance schedule\[sm\_schedule\]

</td><td>

Handles changes to the active flag for a maintenance schedule.

</td></tr><tr><td>

Active changes

</td><td>

Maintenance plan\[sm\_maint\_plan\]

</td><td>

Handles changes to the active flag for a maintenance plan.

</td></tr><tr><td>

Active Insert

</td><td>

Maintenance schedule\[sm\_schedule\]

</td><td>

Handles changes to the active flag for a maintenance schedule.

</td></tr><tr><td>

Apply plan to new records

</td><td>

Maintenance plan\[sm\_maint\_plan\]

</td><td>

Updates the business rule for applying a plan to new records whenever the **Apply to new records** field changes.

</td></tr></tbody>
</table>## Scheduled jobs installed with SM Planned Maintenance

|Scheduled jobs|Description|
|--------------|-----------|
|Planned Maintenance Nightly Run|Builds maintenance requests based on active maintenance plans.|

**Parent Topic:**[Activate Planned Maintenance](../task/t_ActivatePlanMaint.md)

