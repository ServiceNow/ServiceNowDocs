---
title: Data model and case generation
description: Retail Store Audit Operations uses two record types—Store Audit Case and Audit Task—and generates them in a deliberate two-step flow: a Plan Author publishes an audit plan and then explicitly triggers generation, which creates one Store Audit Case per selected Retail Organization and one or more Audit Tasks per case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-generation-flow.html
release: australia
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 3
keywords: [store audit case, audit task, case generation, data model, sn\_rtl\_store\_audit\_case, wm\_audit\_task]
breadcrumb: [Retail Store Audit Operations, Explore, Retail]
---

# Data model and case generation

Retail Store Audit Operations uses two record types—Store Audit Case and Audit Task—and generates them in a deliberate two-step flow: a Plan Author publishes an audit plan and then explicitly triggers generation, which creates one Store Audit Case per selected Retail Organization and one or more Audit Tasks per case.

## Record types

The application introduces two tables. No custom fields are added in V1—both rely on inherited fields from their parent tables.

|Display name|sys\_name|Extends|Number prefix|
|------------|---------|-------|-------------|
|Store Audit Case|`sn_rtl_store_audit_case`|`sn_retail_case`|SAC|
|Audit Task|`wm_audit_task`|`wm_task`|SACTK|

Key data relationships:

-   **Store Audit Case → Retail Organization**: `requesting_service_organization` holds the store \(auditee\) being audited; `service_organization` holds the fulfilling organization.
-   **Audit Task → Store Audit Case**: The inherited `wm_task.initiated_from` field references the parent Store Audit Case.
-   **Work Order → Audit Task**: One `wm_order` is created per `wm_audit_task` by a before-insert Business Rule. The `wm_task` table requires a parent `wm_order` to insert successfully.
-   **Template Item → Retail Organization**: Managed via the existing platform table `sn_case_creation_service_org`—no custom junction table is needed.

## Record lifecycle states

**Store Audit Case**: New → Open → Closed

**Audit Task** active states \(the **Close Complete** button is visible\): Draft, Pending Dispatch, Scheduled, Assigned, Accepted, Work In Progress. Terminal state: Closed Complete.

## Generation trigger

Generation is separated from publication by design. Publishing a plan makes it available for generation but does not create records. The Plan Author must explicitly click **Generate Cases/Tasks** to commit to record creation.

The **Generate Cases/Tasks** UI Action is visible on the `sn_task_plan_template` form only when:

-   The plan is in **Published** state.
-   The user has the `sn_rtl_store_audit.plan_author` role.

Generation completes synchronously—all records exist before the Plan Author sees confirmation.

## What generation creates

For each Retail Organization selected on the plan, the system creates:

1.  One **Store Audit Case** in state New, linked to the Retail Organization via `requesting_service_organization`.
2.  One or more **Audit Tasks** per case, based on the plan's Template Item Configurations, each linked to the parent case via `wm_task.initiated_from`.
3.  One **Work Order** per Audit Task, created by the before-insert Business Rule immediately before the task record inserts.

## Generation architecture

The UI Action calls the platform API `sn_task_plan.MultiEntityCreationService .applyTaskTemplateForMultipleEntities()`, which delegates to the `sn_retail.RetailTaskPlanTemplateHelperEP` extension point implemented by this application. The extension point configures one Store Audit Case and its Audit Tasks per Retail Organization; `MultiEntityCreationService` inserts the records; and three Business Rules on `wm_audit_task` complete the WM lifecycle setup.

|Business Rule|Trigger|Purpose|
|-------------|-------|-------|
|Create WO — Audit Task|Before insert|Creates one `wm_order` per task, sets the parent reference before insertion, and syncs description fields on update.|
|Assign work\_configuration|Before insert|Sets `wm_work_configuration` to **Retail Audit default** when the field is empty.|
|Qualify WO — Audit Task|After insert|Calls `AuditTaskService.qualifyWorkOrder()` to activate the Work Order–task link in the WM state machine.|

**Note:** Generation is atomic per store. If generation fails for one store, no partial records are left—either all records for all selected stores are created, or none are.

## Track plan tab

After generation, a **Track plan** related-list tab appears on the plan record, listing all generated Store Audit Cases with case number, created date, due date, and state. The tab is hidden until at least one case has been generated.

**Parent Topic:**[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

**Related topics**  


[Audit plan and playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-plan-playbook.md)

[Create an audit plan and generate cases and tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-t-create-and-generate.md)

[Components installed with Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-reference.md)

