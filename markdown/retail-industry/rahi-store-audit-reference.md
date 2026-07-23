---
title: Components installed with Store Audit Operations
description: Reference information for roles, tables, fields, and workspace configuration artifacts for Retail Store Audit Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-reference.html
release: australia
topic_type: reference
last_updated: "2026-06-30"
reading_time_minutes: 1
keywords: [store audit reference, roles, tables, workspace configuration, sn\_rtl\_store\_audit]
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Store Audit Operations

Reference information for roles, tables, fields, and workspace configuration artifacts for Retail Store Audit Operations.

## Plugin dependencies

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Retail Store Audit

 \[sn\_rtl\_store\_audit\] 

</td><td>

The Retail Store Audit plugin enables store teams to plan, execute, and track audit activities. It facilitates the creation and management of audit tasks and allows teams to monitor compliance and progress.

</td><td>

-   com.sn\_retail\_core

-   com.sn\_retail\_mobile

-   com.snc.fsm\_work\_types

-   com.sn\_rtl\_str\_plan\_pb

-   com.sn\_smart\_ast\_csm

-   com.snc.fsm\_smart\_asmt\_questionnaire

-   com.sn\_fsm\_audit


</td></tr></tbody>
</table>## Roles

The application defines six scoped roles. All `sys_name` values are prefixed `sn_rtl_store_audit.`

|Role sys\_name|Display name|Contains roles|
|--------------|------------|--------------|
|`sn_rtl_store_audit.plan_author`|Audit Plan Author|`sn_task_plan.creator`, `sn_task_plan.delete`, `sn_task_plan.report_viewer`, `sn_case_creation.org_editor`, `sn_fsm_smart_asmt.questionnaire_feature_author`, `sn_fsm_audit.author`|
|`sn_rtl_store_audit.auditor`|HQ Auditor|`sn_retail.support_agent`, `questionnaire_user`, `sn_fsm_audit.auditor`|
|`sn_rtl_store_audit.location_auditor`|Location Auditor|`sn_retail.associate_fulfiller`, `questionnaire_user`, `sn_fsm_audit.auditor`|
|`sn_rtl_store_audit.audit_manager`|HQ Audit Manager|`sn_smart_asmt.assessment_reader`, `sn_rtl_store_audit.auditor`|
|`sn_rtl_store_audit.location_audit_manager`|Location Audit Manager|`sn_smart_asmt.assessment_reader`, `sn_retail.manager_fulfiller`, `sn_rtl_store_audit.location_auditor`|
|`sn_rtl_store_audit.admin`|Audit Admin|`sn_task_plan.admin`, `sn_rtl_store_audit.plan_author`, `sn_fsm_planned_wm.planned_work_admin`, `sn_fsm_audit.admin`|

## Tables

|Display name|sys\_name|Extends|Number prefix|
|------------|---------|-------|-------------|
|Store Audit Case|`sn_rtl_store_audit_case`|`sn_retail_case`|SAC|
|Audit Task|`wm_audit_task`|`wm_task`|SACTK|

**Note:** `wm_audit_task` is an out-of-the-box FSM Audit table, not a custom extension introduced by this application.

**Parent Topic:**[Components installed with plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-installed-with-plugins.md)

**Related topics**  


[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

[rahi-store-audit-generation-flow]

[Complete a store audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-t-fulfill-audit.md)

