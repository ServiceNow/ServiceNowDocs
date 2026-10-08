---
title: Quick case and task creation for in-store issues
description: Create lightweight cases and tasks to track everyday in-store issues separately from Store Plans, using Retail Service Portal or Retail Mobile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/c\_adhoc-case-task-creation.html
release: australia
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [adhoc case creation, in-store issue, create work item for store, task creation, case management]
breadcrumb: [Retail]
---

# Quick case and task creation for in-store issues

Create lightweight cases and tasks to track everyday in-store issues separately from Store Plans, using Retail Service Portal or Retail Mobile.

Use the quick case and task creation feature to log and track everyday in-store issues without the formality of Store Plans. This feature is designed for store managers, associates, and area managers to quickly report issues like equipment problems, restock requests, or compliance findings, and assign work to team members.

## Who uses this feature

-   Store associates and store managers: Report issues for their own store and fulfill the cases and tasks assigned to them.
-   Area and region managers: Report issues for any store they're mapped to, and own or monitor cases across those stores. They don't fulfill tasks.

## When to use quick case creation

Quick case creation is best for issues that need rapid response and assignment within a single store or store team:

-   Equipment failures or maintenance needs
-   Inventory or restock requests
-   Store safety or compliance findings
-   Customer experience escalations
-   Any ad-hoc work that requires team coordination

For large, multi-store initiatives with scheduled compliance activities, use [Manage store plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-manage-store-plans.md) instead.

## Cases and tasks

A case is the parent work item that describes the issue. A task is a child work item that breaks the case down into actionable work. When you submit the **Create work item for store** form, the system creates one case and no tasks. You add tasks afterward from within the case.

-   Case states: New when created, Open when someone is assigned, and Closed when closed.
-   Task states: Pending Assignment when created, Accepted when someone is assigned, and Closed Complete when closed.
-   Closing: You can close a case or a task at any time. Open tasks don't block closing the case, and no questionnaire is required.

## Role requirements

The following roles determine what you can do with cases and tasks:

-   `sn_rtl_instore_ops.associate` \(store associate\) and `sn_rtl_instore_ops.manager` \(store manager\): Create cases, add tasks, edit and close cases and tasks, assign cases and tasks, and use **Assign to me**.
-   `sn_rtl_instore_ops.manager_contributor` \(area or region manager\): Create cases, add tasks, and edit and close cases and tasks. Area and region managers can be assigned cases, but they can't assign cases or tasks and don't see **Assign to me**.

For detailed role setup, see [Configure case and task roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_configure-instore-ops-roles.md).

## Available on mobile and portal

Start from the **Create work item for store** catalog item on either surface. The item appears only for users who are mapped to at least one store.

-   **Retail Service Portal:** Desktop-friendly interface for store managers to triage and manage cases
-   **Retail Mobile:** Mobile app for store associates to quickly report issues and view assigned work

-   **[Create work item for store on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_report-issue-portal.md)**  
Create a case on the Retail Service Portal to quickly report an in-store issue, then add tasks to break down the work.
-   **[Add a task to a case on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_add-task-portal.md)**  
Create a task within an existing case to assign specific work to a team member on the Retail Service Portal.
-   **[Work on a quick in-store case on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_work-adhoc-case-portal.md)**  
Assign, edit, add tasks to, and close a case that was created with Create work item for store on the Retail Service Portal.
-   **[Work on a quick in-store task on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_work-adhoc-task-portal.md)**  
Assign, edit, and close a task that belongs to a quick in-store case on the Retail Service Portal.
-   **[Create work item for store on Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_report-issue-mobile.md)**  
Create a case on Retail Mobile to quickly report an in-store issue and assign tasks to team members from your phone or tablet.
-   **[Add a task to a case on Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_add-task-mobile.md)**  
Create a task within an existing case to delegate work to team members on Retail Mobile.
-   **[Work on a quick in-store case on Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_work-adhoc-case-mobile.md)**  
Assign, edit, add tasks to, and close a case that was created with Create work item for store in the Retail Mobile app.
-   **[Work on a quick in-store task on Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_work-adhoc-task-mobile.md)**  
Assign, edit, and close a task that belongs to a quick in-store case in the Retail Mobile app.
-   **[Case and task field and role reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/r_adhoc-case-task-reference.md)**  
Technical reference for case and task field descriptions, role permissions, state transitions, and system components used in the quick case creation feature.

