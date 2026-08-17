---
title: Deal registration tasks
description: Create and manage tasks associated with a deal registration to organize work, track progress, and delegate deal-related activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/deal-registration-tasks.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
breadcrumb: [Deal Registration, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Deal registration tasks

Create and manage tasks associated with a deal registration to organize work, track progress, and delegate deal-related activities.

## Tasks overview

Deal registration tasks provide a centralized way to manage all work items associated with a deal. By creating tasks and assigning them to team members, you can ensure that all deal-related work is tracked, assigned, and completed in a timely manner.

A deal registration task is linked to a specific deal registration record and appears in the **Deal Registration Tasks** related list on the deal form. You can also view all deal registration tasks in a standalone list view and across multiple deals.

Deal registration tasks help your organization by:

-   Organizing and delegating work related to a deal in one centralized location.
-   Tracking action items and their completion status.
-   Assigning tasks to any internal team member, beyond deal agents.
-   Centralizing deal-related work in one system.
-   Maintaining a complete audit trail of deal activities and work performed.
-   Enabling cross-functional collaboration \(operations, finance, sales, and so on\) on deals.
-   Tracking work progress through the approval and deal completion process.

You can create tasks at any time during the deal lifecycle when the deal is in one of these active states:

-   **Submitted**
-   **Under Review**
-   **Pending Approval**
-   **Approved**

Tasks can't be created when a deal is in **Draft**, **Completed**, or **Canceled** state.

## Task states

|State|When to Use|Can Transition To|
|-----|-----------|-----------------|
|**Open**|Default state when a task is first created. Use when a task is assigned but work hasn't started.|In Progress, On Hold, Cancelled|
|**In Progress**|Change to this state when the assigned person begins actively working on the task.|On Hold, Complete, Cancelled|
|**On Hold**|Use when you pause work due to dependencies, waiting for information, approvals, resources, or other blockers.|In Progress, Cancelled|
|**Complete**|Change to this state when the assigned person finishes the task work.|None \(final state\)|
|**Cancelled**|Use if the task is no longer needed and work isn't complete. This may occur due to scope changes, deal cancellation, or changed business priorities.|None \(final state\)|

## Task archival and deletion

Deal registration tasks follow cascade archival and deletion rules:

-   Archival: When a deal registration is archived, all associated tasks \(regardless of state\) are automatically archived.
-   Deletion: When a deal registration is deleted, all associated tasks are automatically deleted.
-   Audit trail: Archived and deleted tasks remain in the system history for audit purposes.
-   State-independent: All tasks are archived or deleted regardless of whether they are Open, In Progress, Complete, or Cancelled.

## Task access by role

The following table shows what deal registration tasks each role can access:

|Role|Permission Level|Which Tasks They See|What They Can Do|
|----|----------------|--------------------|----------------|
|Enterprise Relationship Manager|Read, Create, Update|All tasks associated with deals under their organizational hierarchy|Create tasks, update all tasks, manage team's tasks, view task status|
|Enterprise Contributor|Read, Create, Update|All tasks associated with deals belonging to their channel partner|Create tasks for partner deals, update partner tasks, manage workload|
|B2B Deal Agent|Read, Create, Update|Tasks associated with B2B deals only. Can't see tasks on B2C deals|Create tasks on B2B deals, update B2B tasks|
|B2C Deal Agent|Read, Create, Update|Tasks associated with B2C deals only. Can't see tasks on B2B deals|Create tasks on B2C deals, update B2C tasks|
|Deal Registration admin|Read, Create, Update, Delete|All deal registration tasks across all deals in the system|Full control: create, modify, delete, manage all tasks, view all task history|
|Fulfiller|Read, Update \(Limited\)|Only tasks assigned to them \(automatically assigned when a user is added to task\)|View assigned task, update task state, add work notes, see deal-related information|

## Who can be assigned to tasks

Tasks can be assigned to any internal ServiceNow user, beyond deal agents or people with deal roles. This flexibility allows you to assign tasks to:

-   Deal agents and relationship managers \(core deal personas\)
-   Account managers and customer success representatives
-   Operations and administrative staff
-   Finance, compliance, or legal team members
-   Technical implementation or integration team members
-   Any other internal ServiceNow personnel involved in deal-related work

Automatic role assignment: When you assign a task to a user, the system automatically grants them the Fulfiller role. This means users don't need pre-existing deal permissions to contribute to deal work.

-   **[Create a deal registration task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-deal-registration-task.md)**  
Create a task linked to a deal registration to organize work and assign actions to team members.

**Parent Topic:**[Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-management.md)

