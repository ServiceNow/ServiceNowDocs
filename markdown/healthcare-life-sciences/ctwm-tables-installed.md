---
title: Tables installed with Care Team Work Management
description: The following tables are installed with Care Team Work Management.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Tables installed with Care Team Work Management

The following tables are installed with Care Team Work Management.

## Care Team Case

The Care Team Case \[sn\_cto\_case\] table generates cases pertaining to care team internal operations at the unit level.

It extends the Healthcare Operations case \[sn\_hco\_case\].

For information on the Healthcare Operations case, see [Healthcare Operations Case overview](../concept/hcls-cto-hco-case.md).

<table id="table_nyq_nvl_1gc"><tbody><tr><td>

**Field**

</td><td>

**Type**

</td><td>

**Description**

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Unique identifier for the case.

</td></tr><tr><td>

Short Description

</td><td>

String

</td><td>

Brief description of the issue in 160 characters.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Detailed description of the issue in 4000 characters.

</td></tr><tr><td>

Category

</td><td>

Integer

</td><td>

Different classifications of issues that are reported.

</td></tr><tr><td>

Healthcare location

</td><td>

Reference

</td><td>

Healthcare location from where the issue is being reported.

</td></tr><tr><td>

Location

</td><td>

Reference

</td><td>

Common location mapped to the healthcare location.

</td></tr><tr><td>

State

</td><td>

Integer

</td><td>

Person assigned to perform the task.

</td></tr><tr><td>

Priority

</td><td>

Integer

</td><td>

Sequence in which the case should be resolved.

</td></tr><tr><td>

Urgency

</td><td>

Integer

</td><td>

Speed at which the case should be resolved.

</td></tr><tr><td>

Impact

</td><td>

Integer

</td><td>

Level of disruption caused. Indicates the size of issue.

</td></tr><tr><td>

Opened by

</td><td>

Reference

</td><td>

The user who submitted the case.

</td></tr><tr><td>

Primary contact

</td><td>

Reference

</td><td>

The user for whom the case is created.

</td></tr><tr><td>

Assignment group

</td><td>

Reference

</td><td>

The assignment group of the user that fulfills and resolved the request/issue.

</td></tr><tr><td>

Assigned to

</td><td>

Reference

</td><td>

The user that fulfills and resolves the request.

</td></tr><tr><td>

Requesting organization

</td><td>

Reference

</td><td>

The service organization of the requestor.

</td></tr><tr><td>

Supporting organization

</td><td>

Reference

</td><td>

The service organization that fulfills the case.

</td></tr><tr><td>

Service

</td><td>

Reference

</td><td>

Service definition linked to the case.

</td></tr></tbody>
</table>## Care team task

The Care Team Task \[sn\_cto\_task\] table generates tasks attached to care team cases.

It extends the Work order task \[wm\_task\] table.

References Healthcare Location \[sn\_hcls\_location\] to associate the relevant healthcare location with tasks for fulfillment.

<table id="table_oyq_nvl_1gc"><tbody><tr><td>

**Field**

</td><td>

**Type**

</td><td>

**Description**

</td></tr><tr><td>

Opened for

</td><td>

Reference

</td><td>

The user who fulfills the care team task.

</td></tr><tr><td>

Parent

</td><td>

Reference

</td><td>

Parent work order.

</td></tr><tr><td>

State

</td><td>

Integer

</td><td>

State of care team task.

</td></tr><tr><td>

Assigned to

</td><td>

Reference

</td><td>

The user that fulfills and resolves the request.

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Short description of the care team task.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Number of care team tasks.

</td></tr><tr><td>

Service

</td><td>

Reference

</td><td>

Service definition linked to the case.

</td></tr></tbody>
</table>## Healthcare orchestration case

The Healthcare healthcare orchestration case \[sn\_hco\_orchestration\_case\] table creates a case to track the progress of work across multiple healthcare organizations with multiple care team cases.

Requires the Healthcare orchestration plugin.

<table id="table_h54_45t_m3c"><thead><tr><th>

Field 

</th><th>

Type 

</th><th>

Description 

</th></tr></thead><tbody><tr><td>

Short description 

</td><td>

String 

</td><td>

Short description of the orchestration case.

</td></tr><tr><td>

Priority 

</td><td>

Choice 

</td><td>

Sequence in which the case should be resolved.

</td></tr><tr><td>

Service definition

</td><td>

Reference 

</td><td>

The service type of case.

</td></tr><tr><td>

Requesting organization 

</td><td>

Reference 

</td><td>

The organization of case requestor

</td></tr><tr><td>

Supporting organization 

</td><td>

Reference 

</td><td>

The organization of the person assigned to fulfill this case.

</td></tr><tr><td>

Assigned to 

</td><td>

Reference 

</td><td>

The person this case should be assigned to.

</td></tr><tr><td>

Requested by

</td><td>

Reference

</td><td>

The person who created this case.

</td></tr><tr><td>

Assignment group

</td><td>

Reference

</td><td>

Assignment group associated with this case.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Case number.

</td></tr><tr><td>

Due date

</td><td>

Date time

</td><td>

Due date for the case.

</td></tr><tr><td>

State

</td><td>

Choice

</td><td>

Options are:-   Open
-   Work in progress
-   Closed
-   Canceled

</td></tr></tbody>
</table>## Healthcare orchestration task table

The Healthcare orchestration task \[sn\_hco\_orchestration\_task\] table creates task to track any work that required for fulfilling an healthcare orchestration case.

**Healthcare orchestration task** \(extended from CSM Task\): the coordinator’s own activities that support the healthcare orchestration case \(e.g., communications, reviews\).

Requires the Healthcare orchestration plugin.

|Label |Type |Details |
|------|-----|--------|
|Short description |String |Short description of this task.|
|Priority |Choice |Sequence in which this task should be resolved.|
|State|Choice |Current state of the task.|
|Assigned to |Reference |The person to who this task is assigned.|
|Requested by|Reference|The person who created this task.|
|Assignment group|Reference|Assignment group associated with this task.|
|Description|Text|A detailed description of this task.|
|Number|String|Task number.|
|Due date|Date time|Due date for this task.|

