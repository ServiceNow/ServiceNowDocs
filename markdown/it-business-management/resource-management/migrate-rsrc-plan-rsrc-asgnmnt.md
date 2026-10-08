---
title: Migrate resource plans and cost plans
description: Migrate resource plans and cost plans of your projects or demands to resource assignments and attribute-based cost plans. Then, work on the resource allocations and project financials using Project Workspace. The effort table automatically syncs with migrated resource assignments to ensure accurate capacity planning data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/migrate-rsrc-plan-rsrc-asgnmnt.html
release: brazil
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Migration of resource plans and cost plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrate resource plans and cost plans

Migrate resource plans and cost plans of your projects or demands to resource assignments and attribute-based cost plans. Then, work on the resource allocations and project financials using Project Workspace. The effort table automatically syncs with migrated resource assignments to ensure accurate capacity planning data.

## Before you begin

-   Learn more about [Migration of resource plans, operational resource plans, and cost plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/rsrc-plans-rsrc-asgmnts.md).
-   Verify the project or demand have resource plans and cost plans.
-   Verify that the Resource Management Workspace plugin is version 5.5.0 or later for proper effort table synchronization.
-   Role required: resource\_user

## About this task

About resource plans and resource assignments.

Resource plans define resource allocations at a high level using planning attributes such as skills, roles, and resource groups. When you migrate resource plans to resource assignments, the system converts group-level allocations to attribute-based assignments, enabling more granular resource management and accurate capacity planning.

Understanding the effort table and synchronization.

The effort table \(`sn_plng_att_core_cpaam_effort`\) is a database table that maintains aggregated effort estimates by resource group, effort type, and month. This table powers the capacity planning features in the resource management workspace. During migration, resource assignments are created with a resource type of `attribute` \(instead of `group`\), and the system automatically generates corresponding effort estimates.

The effort table synchronizes with resource assignments through the following mechanisms:

-   Automatic sync on create/update: When you create or update a resource assignment after migration, the system triggers an automatic process to generate or update the corresponding effort records in the effort table.
-   Scheduled job sync: The scheduled job *Update Effort Estimates* can be run to resync the effort table for all resource groups, ensuring alignment with resource assignments.
-   Resource type requirement: Effort estimates are generated only for resource assignments with the resource type set to `attribute`. Resource assignments with other resource types \(such as `group`\) will not generate effort records.

During migration, the system performs the following operations:

-   Converts resource plan records to resource assignment records.
-   Sets the resource type to `attribute` for all migrated assignments.
-   Associates each assignment with the appropriate planning attribute based on the original resource plan configuration.
-   Triggers the effort table generation for the migrated assignments.

**Important:** If resource plans are migrated outside of the standard UI migration process, or if custom scripts are used to create resource assignments, verify that the resource type is set to `attribute`. Resource assignments with incorrect resource types will not generate effort estimates, causing data misalignment in the effort table.

## Procedure

1.  Use one of the following options to open a project or a demand.

    -   To open a project, navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All** and open a project.
    -   To open a demand, navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All** and open a demand.
2.  Select the **Migrate resource plans** related link.

    **Note:** This selection triggers the migration of resource plans and cost plans simultaneously.

3.  In the Migrate Resource Plans confirmation window, select **OK**.

    \[Omitted image "rp-ra-migration-confirmation-window.png"\] Alt text: Resource plans migration confirmation window.

    **Tip:** You can [Activate a scheduled job to migrate resource plans and cost plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/migrate-rsrc-plan-cost-plan-scheduled-job.md).

4.  Verify that the migration completed successfully by checking the resource assignment records.

    1.  Navigate to **All** &gt; **Resource Management** &gt; **Resource Assignments**.
    2.  Filter for the resource group that you migrated.
    3.  Confirm that the resource type for all assignments is set to `attribute`.
    4.  Verify that the effort estimates are generated for the migrated assignments by checking the resource management workspace capacity section.

## Result

Resource plans are migrated to resource assignments, cost plans are migrated to attribute-based cost plans. Refresh the project page to view the resource assignments in Resource assignments related list.

What happens during migration:

-   Each resource plan record is converted to one or more resource assignment records, depending on the planning attributes configured.
-   The resource type of all migrated assignments is set to `attribute`.
-   The system automatically generates effort records in the effort table \(`sn_plng_att_core_cpaam_effort`\) for each migrated assignment, aggregated by resource group, effort type, and month.
-   Cost plans are converted to attribute-based cost plans, which reference the migrated resource assignments.

## What to do next

Create resource assignments to manage resource efforts.

Validate the migration:

1.  In the Resource Management Workspace, create a resource card for the resource group that was migrated.
2.  Add filters `User = Active` and `Primary Resource Group = [migrated group]`.
3.  For the Unassigned pane, select `Group = [migrated group]` as a filter.
4.  Select `Hours` as the effort type.
5.  Sum all the efforts displayed for a specific month.
6.  Compare this sum to the effort table by navigating to **All** &gt; **Resource Management** &gt; **Effort Estimates** and filter for the same resource group and month.
7.  The totals should match. If they don't match, the effort table may be out of sync with the resource assignments.

Troubleshooting effort table misalignment:

-   Issue: Effort table shows different totals than the resource management workspace for the same resource group and time period.
-   Cause: Resource assignments with resource type other than `attribute`, or custom scripts that create unassigned resource assignments, may not generate effort records.
-   Resolution: Use the scheduled job [Update Effort Estimates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/migrate-rsrc-plan-cost-plan-scheduled-job.md) to resync the effort table. This job regenerates effort records for all resource groups based on the current resource assignments.

Database tables and effort calculation

Understanding the underlying database structure helps in troubleshooting migration issues. Following are the key tables involved in migration:

-   `sn_plng_att_core_resource_plan` — Source table containing resource plan records. The `resource_type` field indicates whether the plan is group-based or attribute-based.
-   `sn_plng_att_core_resource_assignment` — Destination table containing migrated resource assignment records. For successful effort calculation, this table must have `resource_type = 'attribute'`.
-   `sn_plng_att_core_cpaam_effort` — Effort table that stores aggregated effort estimates. This table includes the following fields:
    -   `combination.group_resource` — References the resource group.
    -   `effort_type` — Type of effort \(hours, percentage capacity, etc.\).
    -   `month_starts_on` — The first day of the month for which effort is estimated.
    -   `estimate` — The aggregated effort value.

Effort calculation process.

1.  When a resource assignment is created or updated with `resource_type = 'attribute'`, a process is triggered to calculate effort estimates.
2.  The system aggregates effort data from all resource assignments for a given resource group, effort type, and month.
3.  The aggregated values are stored in the effort table \(`sn_plng_att_core_cpaam_effort`\).
4.  The capacity planning section of the resource management workspace queries this effort table to display accurate capacity data.

Post-migration validation at database level.

To verify the migration at the database level, system administrators can run the following queries:

-   Verify resource type conversion: Check that all the migrated assignments have `resource_type = 'attribute'` in `sn_plng_att_core_resource_assignment`.
-   Check effort table population: Query `sn_plng_att_core_cpaam_effort` to confirm effort records exist for the migrated resource groups and time periods.
-   Compare totals: Sum effort values from the effort table and compare them to the sum of effort values in resource assignments for the same resource group and month.
-   Identify orphaned assignments: Look for resource assignments with `resource_type != 'attribute'` or unassigned user\_resource fields, which don't generate effort records.

**Warning:** If the effort table is out of sync, use the [Update Effort Estimates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/migrate-rsrc-plan-cost-plan-scheduled-job.md) scheduled job to regenerate effort records. Verify you test this job on a sub-production instance before running it on production, as it updates all effort estimates for all resource groups.

**Parent Topic:**[Migration of resource plans, operational resource plans, and cost plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/rsrc-plans-rsrc-asgmnts.md)

