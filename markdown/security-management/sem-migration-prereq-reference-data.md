---
title: Migration upgrade reference information
description: Lists and tables of scheduled jobs, table deprecations, and new columns added to existing tables for migration to Security Exposure Management Workspace.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-14"
reading_time_minutes: 5
breadcrumb: [Reference, Unified Security Exposure Management, Security Operations]
---

# Migration upgrade reference information

Lists and tables of scheduled jobs, table deprecations, and new columns added to existing tables for migration to Security Exposure Management Workspace.

## Scheduled jobs

Deactivate the scheduled jobs and scheduled jobs within integration-specific scopes for the Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.

-   Adding vulnerability and test fields for remediation tasks
-   Associate existing AVIs with Auto Exception Rule
-   Associate existing VIs with Auto Exception Rule
-   Calculate Related VI Counts for Application Remediation Task
-   Calculate Related VI Counts for Remediation Task
-   Calculate Related VI Counts for Vulnerabilities
-   Check Risk Mitigation Expiration
-   Check Vulnerable Item and Groups Deferment Expiration
-   Copy customized request exception questionnaire to compensating control
-   Evaluate remediation targets
-   Generate remediation digest
-   Insert classic Remediation tasks Into Unified Remediation Task
-   Migrate the background jobs
-   Populate Approval Source
-   Populate CC Number, Configuration Item and Business criticality into Unified Remediation Task Table
-   Populate Container Number,Configuration and Business criticality into Unified Remediation Task Table
-   Populate risk fields for risk rules
-   Populate Vulnerable CIs table - Delete and Re-populate
-   Populate Vulnerable CIs table - Delete and Re-populate for Test Results
-   Populate Vulnerable CIs table - from Vulnerable CI manifest table
-   Re-open deferred remediation tasks
-   Reapply all vulnerability assignment rules
-   Reassignment count for assignment rules
-   Refresh and resolve duplicate VITs on remediation task
-   Refresh associated Application vulnerable items for non-VGR based VG
-   Refresh associated vulnerable items for non-VGR based VG
-   Remove Duplicate VI Remediation Status
-   Repair erroneous Vulnerable Items Last Opened and Closed
-   Rerun calculators
-   Rolldown state from vulnerability group to vulnerable item
-   Rolldown until date from vulnerability group to vulnerable item
-   Rollup application vulnerable item values to vulnerability and group
-   Rollup VI values to vulnerability, Remediation Task \(RT\), and VI count on RT
-   Run severity calculator after vuln entry promotion
-   Send unassignment notification
-   Set deferral counts
-   Set related CI services for VI
-   Update age closed for VITs and AVITs
-   Update all old tags to remediation task table
-   Update is\_in\_group on Vulnerable Items
-   Update Last Open Detection Value To VITs
-   Update Remediation tasks with rolled up states\(AVR\)
-   Update Remediation tasks with rolled up states\(VR\)
-   Update risk rating for vulnerability solutions
-   Update Ungrouped Vulnerable Items
-   Update Vulnerability on VG
-   Vulnerability Response Age Closed Update
-   Vulnerability Response CI count
-   Vulnerability Response Risk and Remediation Status Upgrade
-   Add default values for last\_opened\_dt\_tm from last\_opened
-   Adding TR's CIs to service m2m table
-   Associate existing Container VIs with Auto Exception Rule
-   Associate existing TRs with Auto Exception Rule
-   Auto-close Rule Processor
-   Auto-Close Stale Test Results
-   Calculate Business Criticality for CVIT
-   Calculate Related CVIT Counts for Vulnerabilities
-   Calculate Related VI Counts for Container Remediation Task
-   Calculate remediation metrics for all the remediation tasks
-   Calculate remediation metrics for all the tests
-   Check Container Vulnerable Item Deferment Expiration
-   Check Remediation Tasks and Test Result Deferment Expiration
-   Delete inactive groupBys
-   Evaluate and notify remediation targets
-   Insert Remediation Tasks Into Unified Remediation Task
-   Populate existing test result fields
-   Process test result manifest records
-   Re-apply CI Lookup Rules on the Changed Discovered items
-   Reapply all assignment rules
-   Reapply CI lookup rules
-   Reassess the state of the remediation tasks
-   Reassignment count for assignment rules - CC
-   Reconcile unmatched discovered items
-   Refresh App related Saved filters
-   Refresh CC related Saved filters
-   Refresh Container related Saved filters
-   Refresh Host related Saved filters
-   Remove Groups from Exception Rules
-   Rollup container vulnerable item values to vulnerability and group
-   Rollup Risk scores to Organization
-   Rollup test result values to remediation task and configuration test
-   Send unassignment notification - CC
-   Set deferral counts
-   Trigger aggregation creation and running for saved filter
-   Update age closed for CC
-   Update age closed for CVITs
-   Update all old tags to compliance remediation task table
-   Update all old tags to container remediation task table
-   Update Awaiting Implementation state on CVITs
-   Update remediation metrics
-   Update remediation status for stale test results
-   Update Remediation tasks with rolled up states \(CC\)
-   Update Remediation tasks with rolled up states \(CVR\)
-   Update Risk Rating for Test Results
-   Update Rollup risk score for all non closed Result groups and Configuration tests
-   Update Saved Filter Aggregations
-   Vulnerability Response Container Count

USEM Data Model changes.

<table id="table_wtr_bpy_hgc"><thead><tr><th>

Deprecated tables

</th><th>

New tables

</th></tr></thead><tbody><tr><td>

Vulnerability Assignment Rule \(sn\_vul\_assignment\_rule\)

</td><td>

Assignment Rule \(sn\_sec\_wf\_assign\_rule\)

</td></tr><tr><td>

Security Classification Group \(sn\_sec\_cmn\_classification\_group\)

 Classification Group \(sn\_vul\_classification\_group\)

</td><td>

Classification Group \(sn\_sec\_wf\_classification\_group\)

</td></tr><tr><td>

Security Classification Rule \(sn\_sec\_cmn\_classification\_rule\)

 Classification Rule \(sn\_vul\_classification\_rule\)

</td><td>

Classification Rule \(sn\_sec\_wf\_classification\_rule\)

</td></tr><tr><td>

Security Calculator Group \(sn\_sec\_cmn\_calculator\_group\)

 Vulnerability Calculator \(sn\_vul\_calculator\_group\)

</td><td>

Risk Calculator \(sn\_sec\_calculator\_group\)

</td></tr><tr><td>

Security Calculator \(sn\_sec\_cmn\_calculator\)

 Vulnerability Calculator Rule \(sn\_vul\_calculator\)

 Vulnerability Risk Rule \(sn\_vul\_calc\_risk\)

</td><td>

Risk Calculator Rule \(sn\_sec\_calculator\_rule\)

</td></tr><tr><td>

Risk rule field \(sn\_vul\_risk\_field\)

</td><td>

Risk rule field \(sn\_sec\_calculator\_risk\_field\)

</td></tr><tr><td>

Vulnerability Remediation Status \(sn\_vul\_m2m\_ttr\_status\)

</td><td>

Remediation Status

 \(sn\_sec\_wf\_m2m\_ttr\_status\)

</td></tr><tr><td>

Remediation Target Rule \(sn\_vul\_ttr\_rule\)

</td><td>

Remediation Target Rules \(sn\_sec\_wf\_ttr\_rule\)

</td></tr><tr><td>

Vulnerability Rollup Calculators \(sn\_vul\_rollup\)

</td><td>

Rollup config \(sn\_sec\_wf\_rollup\_config\)

</td></tr><tr><td>

Remediation Task Rule \(sn\_vul\_grouping\_rule\)

 Remediation Task Rule \(sn\_vulc\_grouping\_rule\)

</td><td>

Remediation Task Rule \(sn\_sec\_rem\_task\_rule\)

</td></tr><tr><td>

Exception Rule \(sn\_vul\_auto\_exception\_rule\)

 Auto Exception Rules \(sn\_vulc\_auto\_exception\_rule\)

</td><td>

Exception Rules \(sn\_sec\_exception\_rule\)

</td></tr><tr><td>

Vulnerability State Change Approval \(sn\_vul\_change\_approval\)

 State Change Approval \(sn\_vulc\_state\_change\_approval\)

</td><td>

Change Approval \(sn\_sec\_exception\_change\_approval\)

</td></tr><tr><td>

Exception Management Configuration \(sn\_vul\_exception\_config\)

 Exception Management Configuration \(sn\_sec\_cmn\_exception\_config\)

</td><td>

Exception Management Configuration \(sn\_sec\_exception\_config\)

</td></tr><tr><td>

Policy Exception Reason Mapping \(sn\_sec\_cmn\_policy\_reason\_mapping\)

 Policy Exception Reason Mapping \(sn\_vul\_policy\_reason\_mapping\)

</td><td>

Policy Exception Reason Mapping \(sn\_sec\_exception\_policy\_reason\_mapping\)

</td></tr><tr><td>

Questionnaire Configuration \(sn\_sec\_cmn\_questionnaire\_config\)

</td><td>

Questionnaire Configuration \(sn\_sec\_exception\_questionnaire\_config\)

</td></tr><tr><td>

Vulnerability Compensating Control relationship \(sn\_vul\_m2m\_entry\_compensating\_control\)

</td><td>

Vulnerability Compensating Control relationship \(sn\_vul\_cmn\_m2m\_entry\_compensating\_control\)

</td></tr></tbody>
</table>## New tables introduced to unify administration features

-   Assignment Rule \(sn\_sec\_wf\_assign\_rule\)
-   Classification Group \(sn\_sec\_wf\_classification\_group\)
-   Classification Rule \(sn\_sec\_wf\_classification\_rule\)
-   Risk Calculator \(sn\_sec\_calculator\_group\)
-   Risk Calculator Rule \(sn\_sec\_calculator\_rule\)
-   Risk rule field \(sn\_sec\_calculator\_risk\_field\)
-   Remediation Target Rules \(sn\_sec\_wf\_ttr\_rule\)
-   Rollup config \(sn\_sec\_wf\_rollup\_config\)
-   Approval configuration \(sn\_sec\_cmn\_approval\_config\)
-   Approver level \(sn\_sec\_cmn\_approver\_level\)
-   Remediation Task Rule \(sn\_sec\_rem\_task\_rule\)
-   Auto-close Rule \(sn\_vul\_cmn\_auto\_close\_rule\)
-   Exception Rules \(sn\_sec\_exception\_rule\)
-   Change Approval \(sn\_sec\_exception\_change\_approval\)
-   Exception Management Configuration \(sn\_sec\_exception\_config\)
-   Policy Exception Reason Mapping \(sn\_sec\_exception\_policy\_reason\_mapping\)
-   Questionnaire Configuration \(sn\_sec\_exception\_questionnaire\_config\)
-   Vulnerability Compensating Control relationship \(sn\_vul\_cmn\_m2m\_entry\_compensating\_control\)
-   Widget Grouping \(sn\_sec\_sem\_widget\_grouping\)
-   Widget Aggregation \(sn\_sec\_sem\_m2m\_widget\_dashboard\)
-   Dashboard \(sn\_sec\_sem\_dashboard\)
-   Dashboard Widgets \(sn\_sec\_sem\_dashboard\_widgets\)

## Security Support Common deprecated tables

-   Security Calculator Group \(sn\_sec\_cmn\_calculator\_group\)
-   Security Calculator \(sn\_sec\_cmn\_calculator\)
-   Security Classification Group \(sn\_sec\_cmn\_classification\_group\)
-   Security Classification Rule \(sn\_sec\_cmn\_classification\_rule\)
-   Policy Exception Reason Mapping \(sn\_sec\_cmn\_policy\_reason\_mapping\)

## Vulnerability Response deprecated tables

-   Vulnerability Assignment Rule \(sn\_vul\_assignment\_rule\)
-   Vulnerability Calculator \(sn\_vul\_calculator\_group\)
-   Vulnerability Calculator Rule \(sn\_vul\_calculator\)
-   Vulnerability Risk Rule \(sn\_vul\_calc\_risk\)
-   Risk rule field \(sn\_vul\_risk\_field\)
-   Classification Group \(sn\_vul\_classification\_group\)
-   Classification Rule \(sn\_vul\_classification\_rule\)
-   Vulnerability Remediation Status \(sn\_vul\_m2m\_ttr\_status\)
-   Remediation Target Rule \(sn\_vul\_ttr\_rule\)
-   Vulnerability Rollup Calculators \(sn\_vul\_rollup\)
-   Exception Rule \(sn\_vul\_auto\_exception\_rule\)
-   Vulnerability State Change Approval \(sn\_vul\_change\_approval\)
-   Exception Management Configuration \(sn\_vul\_exception\_config\)
-   Vulnerability Compensating Control relationship \(sn\_vul\_m2m\_entry\_compensating\_control\)
-   Policy Exception Reason Mapping \(sn\_vul\_policy\_reason\_mapping\)

## Vulnerability Response common workspace deprecated table

Saved Filters \(sn\_vul\_cmn\_ws\_saved\_filter\)

## Configuration Compliance deprecated tables

-   Auto Exception Rules \(sn\_vulc\_auto\_exception\_rule\)
-   State Change Approval \(sn\_vulc\_state\_change\_approval\)

## New columns introduced in findings tables

Vulnerable Item \[sn\_vul\_vulnerable\_item\] table.

-   remediation\_plan
-   remediation\_commitment\_dt\_tm
-   auto\_exception\_rule \(reference=sn\_sec\_exception\_rule\)
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

Application Vulnerable Item \[sn\_vul\_app\_vulnerable\_item\] table.

-   remediation\_commitment\_dt\_tm
-   status
-   age\_duration
-   source\_risk\_score
-   times\_found
-   first\_found\_dt\_tm
-   resolution\_dt\_tm
-   last\_opened\_dt\_tm
-   auto\_exception\_rule \(reference=sn\_sec\_exception\_rule\)
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

Test Result \[sn\_vulc\_result\] table.

-   closed\_by
-   first\_found\_dt\_tm
-   last\_found\_dt\_tm
-   opened\_at
-   opened\_by
-   resolution\_dt\_tm
-   last\_state\_changed\_on
-   sys\_class\_name
-   integration
-   backup\_state
-   backup\_substate
-   business\_criticality
-   short\_description
-   status
-   source\_risk\_score
-   times\_found
-   close\_notes
-   substate
-   state\_inheritance\_count
-   priority
-   reopened
-   remediation\_plan
-   remediation\_commitment\_dt\_tm
-   auto\_exception\_rule \(reference=sn\_sec\_exception\_rule\)
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

Container Vulnerable Item \[sn\_vul\_container\_image\_vulnerable\_item\] table.

-   remediation\_plan
-   remediation\_commitment\_dt\_tm
-   auto\_exception\_rule \(reference=sn\_sec\_exception\_rule\)
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

Remediation task \[sn\_vul\_vulnerability\] table.

-   remediation\_commitment\_dt\_tm
-   remediation\_plan
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

Application Remediation Task \[sn\_vul\_app\_vulnerability\] table.

-   remediation\_commitment\_dt\_tm
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

Remediation task \[sn\_vulc\_result\_group\] table.

-   remediation\_commitment\_dt\_tm
-   remediation\_plan
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

Container Remediation Task \[sn\_vul\_container\_vulnerability\] table.

-   remediation\_commitment\_dt\_tm
-   remediation\_plan
-   change\_approval \(reference=sn\_sec\_exception\_change\_approval\)
-   ignore\_expiration\_for\_risk\_reduction\_dt\_tm
-   ignore\_expiration\_dt\_tm

**Parent Topic:**[Unified Security Exposure Management reference](../concept/unified-security-exposure-management-reference.md)

