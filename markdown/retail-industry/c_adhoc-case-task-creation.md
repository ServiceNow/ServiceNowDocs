---
title: Quick case and task creation for in-store issues
description: Create lightweight cases and tasks to track everyday in-store issues separately from Store Plans, using Retail Service Portal or RSM Mobile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/c\_adhoc-case-task-creation.html
release: brazil
topic_type: concept
last_updated: "2026-07-15"
reading_time_minutes: 2
keywords: [adhoc case creation, in-store issue, report an issue, task creation, case management]
breadcrumb: [Retail]
---

# Quick case and task creation for in-store issues

Create lightweight cases and tasks to track everyday in-store issues separately from Store Plans, using Retail Service Portal or RSM Mobile.

Use the quick case and task creation feature to log and track everyday in-store issues without the formality of Store Plans. This feature is designed for store managers, associates, and area managers to quickly report issues like equipment problems, restock requests, or compliance findings, and assign work to team members.

## Who uses this feature

-   **Store associates:** Identify issues on the store floor and report them for triage
-   **Store managers:** Receive and triage cases, assign tasks, and monitor resolution
-   **Area/region managers:** Report issues spotted during store visits across multiple locations

## When to use quick case creation

Quick case creation is best for issues that need rapid response and assignment within a single store or store team:

-   Equipment failures or maintenance needs
-   Inventory or restock requests
-   Store safety or compliance findings
-   Customer experience escalations
-   Any ad-hoc work that requires team coordination

For large, multi-store initiatives with scheduled compliance activities, use [Manage store plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-manage-store-plans.md) instead.

## Cases and tasks

A case is the parent work item that describes the issue. A task is a child work item assigned to a team member to resolve part of the case. When you report an issue, you create one case. Tasks are added afterward from within the case.

-   **Case state:** Progresses from New \(created\) → Open \(assigned\) → Closed \(resolved\)
-   **Task state:** Progresses from Pending Dispatch → Accepted → Closed Complete
-   **Questionnaire:** If compliance verification is required, a linked questionnaire must be submitted before the task closes

## Role requirements

The following roles determine what you can do with cases and tasks:

-   **Store associate:** Create cases, add tasks, and work on assigned tasks
-   **Store manager:** Create cases, assign and reassign tasks, close cases and tasks
-   **Area/region manager:** Create cases when visiting multiple stores

For detailed role setup, see [Configure case and task roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_configure-instore-ops-roles.md).

## Available on mobile and portal

Create and manage cases and tasks on these surfaces:

-   **Retail Service Portal:** Desktop-friendly interface for store managers to triage and manage cases
-   **RSM Mobile:** Mobile app for store associates to quickly report issues and view assigned work

-   **[Report an issue on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_report-issue-portal.md)**  
Create a new case using the Record Producer to quickly report an in-store issue on the Retail Service Portal, then add tasks and assign work to team members.
-   **[Add a task to a case on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_add-task-portal.md)**  
Create a task within an existing case to assign specific work to a team member on the Retail Service Portal.
-   **[Report an issue on RSM Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_report-issue-mobile.md)**  
Create a case on RSM Mobile to quickly report an in-store issue and assign tasks to team members from your phone or tablet.
-   **[Add a task to a case on RSM Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_add-task-mobile.md)**  
Create a task within an existing case to delegate work to team members on RSM Mobile.
-   **[Case and task field and role reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/r_adhoc-case-task-reference.md)**  
Technical reference for case and task field descriptions, role permissions, state transitions, and system components used in the quick case creation feature.

