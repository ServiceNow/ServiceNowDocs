---
title: Components installed by CI Lifecycle Management
description: Several types of components are installed by CI Lifecycle Management \(included in the com.snc.cmdb plugin\), including tables, scheduled jobs, and properties.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB CI Lifecycle Management \(legacy\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed by CI Lifecycle Management

Several types of components are installed by CI Lifecycle Management \(included in the com.snc.cmdb plugin\), including tables, scheduled jobs, and properties.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|CI Lifecycle Management - Restore Internal State Management Tables|Continuously checks and maintains the data integrity of all internal CI Lifecycle Management tables.|
|Update life cycle from legacy|Updates CIs **Life cycle stage** and **Life cycle status** fields when legacy status fields change.|
|Update legacy from CSDM”|Updates CIs legacy status fields when life cycle changes.|

## Tables installed

<table id="table_cx2_lc1_d2b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI State Registered Users \[statemgmt\_register\_users\]

</td><td>

All currently active registered users that were created via the **registerOperator** API. You cannot manually add new records to this table.

</td></tr><tr><td>

CI Actions \[statemgmt\_ci\_actions\]

</td><td>

A set of CI actions that can be applied to a CI during its lifetime.

</td></tr><tr><td>

CMDB CI Actions\[statemgmt\_cmdb\_actions\]

</td><td>

Active/inactive CI actions set by a specific requestor for a specific CI. You cannot manually add new records to this table.

</td></tr><tr><td>

Compatible CI Actions\[statemgmt\_compat\_actions\]

</td><td>

Set of rules that define pairs of CI actions that are compatible for a CI and can be applied simultaneously.

</td></tr><tr><td>

Not Allowed CI Actions\[statemgmt\_not\_allow\_actions\]

</td><td>

Set of rules that define specific actions that are not allowed for a CI when its in a specific operational state.

</td></tr><tr><td>

Internal Operational States\[statemgmt\_ops\_state\]

</td><td>

Internal operational states set by a specific active requestor for a specific CI. You cannot manually add new records to this table.

</td></tr><tr><td>

Renew Lease Task\[statemgmt\_renew\_lease\_task\]

</td><td>

Set of tasks that were automatically created to renew the lease of CI actions whose lease has expired. You cannot manually add new records to this table.

</td></tr><tr><td>

Operational State Priorities\[statemgmt\_ops\_state\_pri\]

</td><td>

Priorities of operational states which determine precedence when multiple operational states are set for same CIs by different requestors.

</td></tr><tr><td>

Not Allowed Operational Transitions\[statemgmt\_not\_allow\_ops\]

</td><td>

Set of rules that define specific operational state transitions that are not allowed.

</td></tr></tbody>
</table>## Properties installed

<table id="table_bwc_2gs_d2b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.cmdb.statemgmt.max\_lease\_expired\_days

</td><td>

Maximum number of days that lease expiration can be set with for CI Actions.-   Type: integer
-   Default value: 15
-   Location: System Property \[sys\_properties\] table.

</td></tr><tr><td>

glide.cmdb.statemgmt.max\_bulk\_count

</td><td>

Maximum number of CIs that CI Lifecycle Management can process in a bulk update operation.-   Type: integer
-   Default value: 1000
-   Location: System Property \[sys\_properties\] table.

</td></tr></tbody>
</table>**Parent Topic:**[CMDB CI Lifecycle Management \(legacy\)](../concept/cmdb-ci-lifecycle-mgmt.md)

