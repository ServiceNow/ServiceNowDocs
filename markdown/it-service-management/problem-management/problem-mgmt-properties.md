---
title: Problem management properties
description: Problem Management properties are used to control features such as creating problem task on a closed problem and reanalyzing a closed or a canceled problem.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Problem Management, IT Service Management]
---

# Problem management properties

Problem Management properties are used to control features such as creating problem task on a closed problem and reanalyzing a closed or a canceled problem.

These properties are available at **Problem** &gt; **Administration** &gt; **Problem Properties**.

<table id="table_wtc_fkl_pfb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Problem State Transition Properties

</td></tr><tr><td>

Accept Risk moves the Problem to Closed state instead of Resolved stateproblem.acceptrisk.move\_to\_closed

</td><td>

-   Type: true or false
-   Default value: true

</td></tr><tr><td>

Can create a Problem Task on a Closed Problem?problem.closed.can\_create\_tasks

</td><td>

-   Type: true or false
-   Value: true or false
-   Default value: false

</td></tr><tr><td>

Who can Re-analyze a Canceled Problem?problem.closed.role.reanalyze\_from\_canceled

</td><td>

-   Type: choice list
-   Default value: problem\_manager

</td></tr><tr><td>

Who can Re-analyze a Risk Accepted \(Closed state\) Problem?problem.closed.role.reanalyze\_from\_closed\_riskaccepted

</td><td>

-   Type: choice list
-   Default value: problem\_manager

</td></tr><tr><td>

Who can Re-analyze a Completed Problem?problem.closed.role.reanalyze\_from\_completed

</td><td>

-   Type: choice list
-   Default value: problem\_manager

</td></tr><tr><td class="sub-head" colspan="2">

Problem Task State Transition Properties

</td></tr><tr><td>

Cancel open Problem Tasks when closing a Problemproblem.closed.cancel\_open\_tasks

</td><td>

-   Type: true or false
-   Value: true or false
-   Default value: true

</td></tr><tr><td>

Who can Re-assess a Completed or Canceled Problem Task?problem\_task.closed.role.reaassess\_from\_closed

</td><td>

-   Type: choice list
-   Default value: problem\_coordinator

</td></tr><tr><td>

Can Re-Assess a Problem Task on a Closed Problem?problem\_task.closed.can\_reassess\_on\_closed\_problem

</td><td>

-   Type: true or false
-   Default value
    -   Upgrade: true
    -   New instances: false

</td></tr><tr><td class="sub-head" colspan="2">

Problem Related List Properties

</td></tr><tr><td>

List of related task records \(comma-separated\) to track as fixes for this Problem. Used to notify the Coordinator when all the related fix records are Completed or Canceled. E.g. change\_request.parentproblem.fix.records

</td><td>

-   Type: string
-   Default value: change\_request.parent, rm\_defect.parent, rm\_release.parent, rm\_enhancement.parent, sn\_cim\_register.source\_id

</td></tr><tr><td>

List of related task records \(comma-separated\) to move over when a problem is marked as a duplicate of another. E.g. incident.problem\_idproblem.duplicate.records\_to\_move

</td><td>

-   Type: string
-   Default value: incident.problem\_id, sn\_customerservice\_case.problem, problem\_task.problem

</td></tr><tr><td>

Who can relate closed Incidents to a Problem?problem.role.relate\_closed\_incidents

</td><td>

-   Type: choice
-   Default value:
    -   Upgrade: Nobody
    -   New instances: Problem coordinators

</td></tr><tr><td class="sub-head" colspan="2">

Problem Created from Incident Properties

</td></tr><tr><td>

List of attributes \(comma-separated\) that will be copied from the incident to create a new problemcom.snc.problem.create\_from\_incident.attributes

</td><td>

-   Type: string
-   Default value: number, description, short\_description, cmdb\_ci, impact, urgency, priority, company, sys\_domain, business\_service, category, subcategory

</td></tr><tr><td class="sub-head" colspan="2">

Problem Created from Interaction Properties

</td></tr><tr><td>

Create saved problemcom.snc.problem.create\_from\_interaction.save

</td><td>

-   Type: Boolean
-   Default value:
    -   Upgrade customers: No
    -   New customers: Yes

</td></tr><tr><td>

Allow problem creation from interactionglide.problem.interaction.allow\_create

</td><td>

-   Type: true or false
-   Value: true or false
-   Default value: false

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Problem Management](../concept/reference-section-for-problem-management.md)

