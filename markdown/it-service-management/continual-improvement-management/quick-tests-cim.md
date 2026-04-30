---
title: Quick tests for Continual Improvement Management
description: Validate the continued functionality of Continual Improvement Management during application development and after upgrades. Copy and configure these automated tests to identify customizations needing review. All test suites and tests should pass.
locale: en-US
release: zurich
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Continual Improvement Management, IT Service Management]
---

# Quick tests for Continual Improvement Management

Validate the continued functionality of Continual Improvement Management during application development and after upgrades. Copy and configure these automated tests to identify customizations needing review. All test suites and tests should pass.

**Note:** To run CIM automated tests:

-   The Continual Improvement Management Automated Tests \(com.sn\_cim\_atf\) plugin must be enabled.
-   The **sn\_cim.create\_default\_phase** system property must be enabled. For more information, see [Properties installed with Continual Improvement Management](cim-components.md).

<table id="atf-tests-cim"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CIM Parent test suite

</td><td>

Parent test suite that contains multiple child test suites.-   CIM Inbound Integration
-   CIM Outbound Integrations
-   CIM Phase and Task
-   CIM State Flow

 **Note:** There is no dependency between child test suites.

</td></tr><tr><td>

CIM Inbound Integrations

</td><td>

Suite that contains tests to create an improvement initiative from inbound integration applications. -   Problem Management
-   Incident Management
-   Demand Management
-   Coaching
-   Survey Management
-   Assessments

</td></tr><tr><td>

CIM Outbound Integrations

</td><td>

Suite that contains tests for all CIM outbound integrations. -   From an improvement initiative:

Create demand and create project.

-   From an improvement initiative task:

Create knowledge article, change request, coaching opportunity, and story.


</td></tr><tr><td>

CIM Phase and Task

</td><td>

Suite that contains tests for CIM phase and CIM task creation, roll-up tasks, roll up phases, and dates.

</td></tr><tr><td>

CIM State Flow

</td><td>

Suite that contains all CIM state-related tests.

</td></tr><tr><td>

CIM: Create a demand from an improvement initiative

</td><td>

Tests that a user with the Improvement Manager role can create a demand from an improvement initiative.

</td></tr><tr><td>

CIM: Create a project from an improvement initiative

</td><td>

Tests that a user with Project manager and Improvement Manager roles can create a project from an improvement initiative.

</td></tr><tr><td>

CIM: Create a change request from an improvement initiative task

</td><td>

Tests that a user with the Improvement Manager role can create a change request from an improvement initiative task.

</td></tr><tr><td>

CIM: Create a coaching opportunity from an improvement initiative task

</td><td>

Tests that a user with Coaching admin and Improvement Manager roles can create a coaching opportunity from an improvement initiative task.

</td></tr><tr><td>

CIM: Create a knowledge article from an improvement initiative task

</td><td>

Tests that a user with Knowledge admin and Improvement Manager roles can create knowledge article from an improvement initiative task.

</td></tr><tr><td>

CIM: Create a story from an improvement initiative task

</td><td>

Tests that a user with Project manager and Improvement Manager roles can create a story from an improvement initiative task.

</td></tr><tr><td>

CIM: Create a task within a phase

</td><td>

Tests that a task can be created within a phase.

</td></tr><tr><td>

CIM: Improvement Coordinator creates a task and phase

</td><td>

Tests that a user with the Improvement Coordinator role can create a task and phase.

</td></tr><tr><td>

CIM: Improvement Coordinator state flow from Approved to Implement

</td><td>

Tests that a user with the Improvement Coordinator role can change an improvement initiative from Approved state to Implement state.

</td></tr><tr><td>

CIM: Improvement Manager creates a strategic objective

</td><td>

Tests that a user with the Improvement Manager role can create a strategic objective.

</td></tr><tr><td>

CIM: Improvement Manager creates a task and phase

</td><td>

Tests that a user with the Improvement Manager role can create a task and phase.

</td></tr><tr><td>

CIM: Improvement Manager deletes an improvement initiative

</td><td>

Tests that a user with the Improvement Manager role can delete an improvement initiative.

</td></tr><tr><td>

CIM: Improvement Requester cannot create a task or phase

</td><td>

Tests that a user with the Improvement Requester role cannot create a task or phase.

</td></tr><tr><td>

CIM: Improvement Requester creates an improvement initiative

</td><td>

Tests that a user with the Improvement Requester role can create an improvement initiative.

</td></tr><tr><td>

CIM: Inbound integration from Assessments

</td><td>

Tests that a user with the Survey administrator role can create an improvement initiative from an assessment.

</td></tr><tr><td>

CIM: Inbound integration from a coaching opportunity

</td><td>

Tests that a user with the Coaching admin role can create an improvement initiative from a coaching opportunity.

</td></tr><tr><td>

CIM: Inbound integration from Demand Management

</td><td>

Tests that a user with the Demand manager role can create an improvement initiative from a demand.

</td></tr><tr><td>

CIM: Inbound integration from Incident Management

</td><td>

Tests that a user with the itil role can create an improvement initiative from an incident.

</td></tr><tr><td>

CIM: Inbound integration from Problem Management

</td><td>

Tests that a user with the itil role can create an improvement initiative from a problem.

</td></tr><tr><td>

CIM: Inbound integration from Survey Management

</td><td>

Tests that a user with the Survey administrator role can create an improvement initiative from a survey.

</td></tr><tr><td>

CIM: Initiative reject approval state flow from Assess to Accepted

</td><td>

Tests when an improvement initiative in Assess state is rejected by an approver, the state reverts back to Accepted.

</td></tr><tr><td>

CIM: Initiative state flow from Implement to On Hold

</td><td>

Tests that an improvement initiative in Implement state can be changed to On Hold state.

</td></tr><tr><td>

CIM: Initiative state flow from New through Closed

</td><td>

Tests that an improvement initiative in New state can be progressed through states Accepted, Assess, Approved, Implement, Review, to Closed state.

</td></tr><tr><td>

CIM: Initiative state flow from On Hold to Implement

</td><td>

Tests that an improvement initiative in On Hold state can be changed to Implement state.

</td></tr><tr><td>

CIM: Initiative state flow from On Hold to Review

</td><td>

Tests that an improvement initiative in On Hold state can be changed to Review state.

</td></tr><tr><td>

CIM: Initiative state flow from Review to Implement

</td><td>

Tests that an improvement initiative in Review state can be changed to Implement state.

</td></tr><tr><td>

CIM: New phase planned end date check

</td><td>

Tests that the planned end date for a new phase is at least one day later than the planned start date of the improvement initiative.

</td></tr><tr><td>

CIM: Phase creation for a new improvement initiative

</td><td>

Tests that a phase is automatically created when an improvement initiative is created.

</td></tr><tr><td>

CIM: Planned end date always later than planned start date

</td><td>

Tests that the planned end date of the improvement initiative is not earlier than the planned start date of the improvement initiative.

</td></tr><tr><td>

CIM: Roll-up phase to improvement initiative value check

</td><td>

Tests that the phase-level roll-up value for the improvement initiative \(percent complete\) is accurate.

</td></tr><tr><td>

CIM: Roll-up tasks to phase value check

</td><td>

Tests that the task-level roll-up value for the phase \(percent complete\) is accurate.

</td></tr><tr><td>

CIM: Skip approval process flow

</td><td>

Tests that the approval process is skipped when the Enable approval process for Continual Improvement initiatives property is cleared.

</td></tr><tr><td>

CIM: Submit an initiative in Accepted state to Cancel

</td><td>

Tests that an improvement initiative in Accepted state can be submitted for Cancel action.

</td></tr><tr><td>

CIM: Submit an initiative in Approved state for Re-Approval

</td><td>

Tests that an improvement initiative in Approved state can be submitted for Re-Approval action.

</td></tr><tr><td>

CIM: Submit an initiative in Assess state for Revert to Accepted

</td><td>

Tests that an improvement initiative in Assess state can be submitted for Revert to Accepted action.

</td></tr><tr><td>

CIM: Submit an initiative in Implement state for Re-Approval

</td><td>

Tests that an improvement initiative in Implement state can be submitted for Re-Approval action.

</td></tr></tbody>
</table>**Parent Topic:**[Continual Improvement Management reference](cim-reference.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

