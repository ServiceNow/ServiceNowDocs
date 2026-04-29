---
title: Quick start tests for HR Service Delivery
description: Validate the continued functionality of HR Service Delivery after any configuration change such as an upgrade or after developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [HR Service Delivery, Employee Service Management]
---

# Quick start tests for HR Service Delivery

Validate the continued functionality of HR Service Delivery after any configuration change such as an upgrade or after developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

All test suites and tests should pass on a default implementation. To validate a custom implementation, copy the automated tests and configure them for your customizations.

Quick start tests are disabled and read-only test templates. By default, they only produce a pass result when you run them with the default demo data that is provided with the application or feature plugin.

To make quick start tests produce a pass result when you run them with your instance-specific data, copy and configure them to use your instance data.

The Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) and the Agile Development 2.0 - ATF Tests \(com.snc.sdlc.agile.2.0.atf\) plugins must be enabled.

**Note:** When running, demo data is required.

## Employee Document Management

Employee Document Management quick start tests require activating the Employee Document Management \(com.sn\_employee\_document\_management\) plugin.

|Test|Description|Release version|
|----|-----------|---------------|
|EDM: Create retention period with day offset|Creates a retention period with a one \(1\) day offset and verifies the calculation period in a retention policy.|Rome|

<table id="table_evy_jw2_yjb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

Case Creation Configuration

</td><td>

Validates an HR service has a case creation configuration and is populated into the HR case form when creating an HR case for that HR service.

</td><td>

Yokohama

</td></tr><tr><td>

Create Document template block and block content

</td><td>

Verifies a document template block and document template content are created for block content.

</td><td>

Yokohama

</td></tr><tr><td>

Create HR Employee Document

</td><td>

Creates an employee document and ensures the Attachment \[sys\_attachment\] table points back to the record in the Employee Document \[sn\_hr\_ef\_employee\_document\] table.Verifies that the employee document is accessible from the Employee Center or Employee Center Pro via the employee HR profile.

</td><td>

 

</td></tr><tr><td>

Create Employee Document with Active Document Type

</td><td>

Validates the creation of:-   One active document type
-   One inactive document type
-   Employee file with active document type

 **Note:** Human Resources Scoped App: Core \(com.sn\_hr\_core\) and Employee Document Management \(com.sn\_employee\_document\_management\) must be activated.

</td><td>

Yokohama

</td></tr><tr><td>

\[Delegation\] Admin - Adding a delegation rule with delegator and delegate user criteria

</td><td>

Verifies that user criteria for a delegation rule works correctly,

</td><td>

San Diego

</td></tr><tr><td>

E2E test for Bulk Case Creation

</td><td>

Verifies that bulk cases can be created for selected users in a specific user segment.

</td><td>

San Diego

</td></tr><tr><td>

ER: Case Restriction

</td><td>

Verifies that restricted cases are only viewable by users with the sn\_hr\_er.confidential role.

</td><td>

San Diego

</td></tr><tr><td>

HR: Case updates visible to employees

</td><td>

Cases created and updated by an HR agent are visible to the Opened for or Subject person

</td><td>

Quebec

</td></tr><tr><td>

HR: Creation of 401k enrollment case from portal

</td><td>

Creates a 401\(k\) enrollment case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

Madrid

</td></tr><tr><td>

HR: Creation of Employee Relations case from ESC portal

</td><td>

Creates a Disciplinary Issue case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

New York

</td></tr><tr><td>

HR: Creation of Employment Verification Letter case from ESC portal

</td><td>

Creates an Employment Verification Letter case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

Madrid

</td></tr><tr><td>

HR: Creation of Payroll case from ESC portal

</td><td>

Creates a direct deposit payroll setup case from the Employee Center or Employee Center Pro.Verifies that the case creates successfully.

</td><td>

New York

</td></tr><tr><td>

HR: Creation of Tuition Reimbursement request from portal

</td><td>

Creates a Tuition Reimbursement Request case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

Madrid

</td></tr><tr><td>

HR: Fulfillment Instructions

</td><td>

Verifies that fulfillment instructions are created for a specific condition for an opened for user. Also verifies the fulfillment instructions change when the details of the case changes.

</td><td>

Orlando

</td></tr><tr><td>

HR: Fulfillment Instructions conditions for COE specific fields

</td><td>

Verifies the conditions for COE specific fulfillment instruction.Fulfillment instructions update on an HR case based on the conditions defined in the fulfillment instructions.

</td><td>

Quebec

</td></tr><tr><td>

HR: General Benefits Inquiry Case Creation

</td><td>

Creates a General Benefits case using the native UI.It also verifies that the case opens and can be updated after case creation.

</td><td>

Madrid

</td></tr><tr><td>

HR: Payroll Discrepancy Case Creation

</td><td>

Creates a Payroll Discrepancy case using the native UI.It also verifies that the case opens and can be updated after case creation.

</td><td>

Madrid

</td></tr><tr><td>

HR: Reclassify Case Transfer

</td><td>

Tests when an HR case transfers from one COE \(HR service\) to a different COE using the reclassify \(HR case number remains the same\) method.

</td><td>

Orlando

</td></tr><tr><td>

HR: Response Template Configuration

</td><td>

Creates a response template for a payroll case and pastes the response in the worknotes.

</td><td>

Quebec

</td></tr><tr><td>

HR: Search catalog items &amp; KBs in ESC

</td><td>

Verifies the search functionality in the Employee Center or Employee Center Pro.

</td><td>

Orlando

</td></tr><tr><td>

HR: Standard Case Transfer

</td><td>

Tests an HR case transfers from one COE \(HR service\) to a different COE using the standard \(creates HR case number and deletes old number\) case transfer.

</td><td>

Orlando

</td></tr><tr><td>

HR: Suspend Case Flow

</td><td>

Tests the ability to suspend an HR case and later resume the case.

</td><td>

Rome

</td></tr><tr><td>

HR: Tuition Reimbursement Case Creation

</td><td>

Creates a Tuition Reimbursement HR case.

</td><td>

Orlando

</td></tr><tr><td>

HR: Workforce Administration Case Creation

</td><td>

Creates a Workforce Administration case, signs an employee verification letter, and generates the letter.

</td><td>

Orlando

</td></tr><tr><td>

JA: Publish &amp; edit plan details

</td><td>

Verifies the ability to delete an existing to-do in an action plan.

</td><td>

San Diego

</td></tr><tr><td>

Journey Designer: Create stage and edit stage

</td><td>

Verifies that the user can create a new stage, add a task template to the stage, edit the stage name, and delete the stage.

</td><td>

Vancouver

</td></tr><tr><td>

Journey Designer: Add task templates from scratch and edit

</td><td>

Verifies that the user can add a task template using the Build from scratch option, then edit the task template.

</td><td>

Vancouver

</td></tr><tr><td>

Journey Designer: Add existing task templates and remove task template

</td><td>

Verifies that a task template can be added to a Journey template with the Use template option, and then removed.

</td><td>

Vancouver

</td></tr><tr><td>

Learning Core Task Assignment

</td><td>

Verifies a learning task from a learning catalog can be assigned to a user.

</td><td>

San Diego

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|Configure HR Service for Auto Case Closure|Verifies that Lifecycle event cases are automatically closed.|Orlando|
|Create Employee request and associate it to LE case|Creates and validates that an employee request appears in the Lifecycle Event case action list.|Rome|
|Create Employee request for old ticket page|Validates if employee requests can be created from the legacy ticket page.|Yokohama|
|\[Delegation\] Admin - Adding a delegation rule with delegator and delegate user criteria|Verifies user criteria is working for delegation rules for a delegator and delegate user.|Yokohama|
|HR Lifecycle: Access Ticket page for a NewHire Onboarding Case in Employee Service Center|Verifies creation of a new hire and can access the Ticket page of the Employee Service Center.|Orlando|
|HR Lifecycle: Access ESC ticket page and todos page and complete assigned todos|Creates a Tuition Reimbursement Request case from Employee Service Center and the Complete NDA to-do from the subject person.|Orlando|
|HR LifeCycle: Request Onboarding Case Creation|Creates a Request Onboarding case using the native UI and updates the case after creation.|Madrid|
|HR Lifecycle: Trigger Rescind Workflow|Triggers the Rescind workflow for a New Hire Onboarding Lifecycle Event case.|Quebec|
|HR Lifecycle: Verify Requests page for Open and Closed cases|Verifies open and closed cases on the Requests page.|Orlando|
|HR Lifecycle: Verify search in Requests Page|Verifies the search functionality on the Requests page for open and closed cases.|Orlando|
|\[LE\]: Add Ad hoc task|Verifies an ad hoc task can be added for a Lifecycle Event case.|Yokohama|

**Note:** Requires the following plugin activation:

-   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
-   Employee Center \[com.sn\_hr\_service\_portal\]
-   Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]
-   Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\]

|Test|Description|Release version|
|----|-----------|---------------|
|Create knowledge block and attach block to article|Creates a knowledge block, publishes the block, and attaches the block to a knowledge article.|New York|
|Preview Knowledge Articles with Knowledge Blocks|Tests for preview of knowledge article that contains knowledge blocks.|New York|

Requires the following plugin activation: Human Resources Scoped App: Core \[com.sn\_hr\_core\]

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

